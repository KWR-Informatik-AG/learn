# Git

If you are working with a small group on a project, this may work quite well. But what happens when the project grows and more people need to work on it? This is where Git comes into play

Git is a **DevOps tool**, which is used for **source code management**. It offers functions for versioning and collaboration in large groups. This enables faster iteration of the software and thus supports the [DevOps](../index.md) concept.

## Installation

Help: [https://git-scm.com/book/en/v2/Getting-Started-Installing-Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

The command `git --version` can be used to check for an existing installation.

=== "Linux"
Under Linux Git is usually pre-installed

    If this is not the case, git can usually be installed via a package manager


    === "apt"

        ```bash
        sudo apt install git-all
        ```

    === "dnf"

        ```bash
        sudo dnf install git-all
        ```

    === "brew"

        ```bash
        brew install git
        ```

=== "Mac"

    === "Homebrew"

        ```bash
        brew install git
        ```

    === "MacPorts"

        ```bash
        sudo port install git
        ```

=== "Windows"
You can find the Installationmanager with the manual under
[https://git-scm.com/downloads](https://git-scm.com/downloads).

    Under Windows it's easier to develop with Linux over WSL.
