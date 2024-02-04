# Git Workflows

!!! info
    Für einzelne Entwickler

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
    commit id: "Initial commit"
    commit id: "Feature"
    commit id: "Bugfix"

```

!!! info
    Für 2-10 Entwlicker

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
    commit id: "Initial commit"

    branch feature-a
    checkout feature-a
    commit id: "Implement A"
    commit id: "Bugfix A"
    checkout main
    merge feature-a
    commit id: "Merge Feature A"

    branch feature-b
    checkout feature-b
    commit id: "Implement B"
    commit id: "Bugfix B"
    checkout main
    merge feature-b
    commit id: "Merge Feature B"

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
