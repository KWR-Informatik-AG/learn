# Git Flow

```mermaid
%%{init: {

'logLevel': 'debug',
'theme': 'default',

'themeVariables': {
    'git0': '#203f65',
    'git1': '#284a73',
    'git2': '#305581',
    'git3': '#396190',
    'git4': '#416c9f',
    'git5': '#4979ae',
    'git6': '#5185bd',
    'git7': '#5a91cc'
},
'gitGraph': {
    'showCommitLabel': true
} } }%%

gitGraph TB:
    commit id: "initial commit"
    branch develop order: 3
    commit id: "develop"
    checkout develop

    branch feature/f1 order: 4 %% Create f1 Branch
    checkout feature/f1
    commit
    commit
    checkout develop %% Create f2 Branch
    branch feature/f2 order: 5
    checkout feature/f2
    commit
    checkout feature/f1
    commit
    checkout feature/f2
    commit
    commit
    checkout develop %% Merge f2 into Develop
    merge feature/f2

    checkout feature/f1 %% Merge latest features into f1 branch
    merge develop
    commit id: "Merge dev"

    branch release/v0.1.0 order: 2 %% Create release/v0.1.0 branch
    checkout release/v0.1.0
    merge develop tag:"v0.1.0"
    commit id: "Bugfix 1"
    checkout develop
    merge release/v0.1.0
    checkout feature/f1
    merge develop

    checkout release/v0.1.0
    commit id: "Bugfix 2"
    checkout main
    merge release/v0.1.0 tag: "v0.1.0"
    checkout develop
    merge release/v0.1.0
    checkout feature/f1
    merge develop

    checkout main
    branch hotfix/hf1 order: 1
    checkout hotfix/hf1
    commit
    commit
    checkout main
    merge hotfix/hf1 tag: "v0.1.1"

    checkout develop
    merge main
    checkout feature/f1
    merge develop
    checkout develop
    merge feature/f1

    

```

## Branches/Zweige

### Main

Der **main branch** (früher **master**) wird für production-releases verwendet. Fehler werden in **hotfix branches** behoben.

### Develop

Der **develop branch** wird vom **main branch** erstellt und enthält alle stabilen features für den nächsten release.

### Releases

**Release branches** werden verwendet, um Releases zu **isolieren und stabilisieren**. Fixes im Release Branch werden wieder in dem Develop Branch zusammengeführt

### Features

**Feature branches** werden **mit dem develop Branch zusammengeführt**, sobald sie **stabil und getested** sind. Es können **beliebig viele** feature branches erstellt werden. Änderungen auf dem Develop Branch müssen wieder mit den feature branches zusammengeführt werden.

### Hotfixes

**Hotfix branches** werden erstellt, um Fehler im **main branch** zu beheben.

## Tagging

```mermaid
%%{init: {

'logLevel': 'debug',
'theme': 'default',

'themeVariables': {
    'git0': '#203f65',
    'git1': '#284a73',
    'git2': '#305581',
    'git3': '#396190',
    'git4': '#416c9f',
    'git5': '#4979ae',
    'git6': '#5185bd',
    'git7': '#5a91cc'
},
'gitGraph': {
    'showBranches': false,
    'showCommitLabel': true
} } }%%
gitGraph LR:
    commit tag:"v1.0.0" id:"Major Release A"
    commit tag:"v1.1.0" id:"Minor Release A"
    commit tag:"v1.1.1" id:"Hotfix A"
    commit tag:"v2.0.0" id:"Major Release B"
    commit tag:"v2.1.0" id:"Minor Release B"
    commit tag:"v2.0.1" id:"Hotfix B"
    commit tag:"v3.0.0" id:"Major Release C"
    commit tag:"v3.1.0" id:"Minor Release C"
    commit tag:"v3.1.1" id:"Hotfix C"
```
