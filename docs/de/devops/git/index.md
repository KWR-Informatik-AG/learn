# Git

Wenn man mit einer kleinen Gruppe in einem Projekt zusammenarbeitet, funktioniert das möglicherweise ganz in Ordnung. Doch wie soll es weiter gehen, wenn das Projekt wächst und noch mehr Leute mitarbeiten müssen? Hierkommt Git ins Spiel

Git ist ein **DevOps Werkzeug**, welches für die **Quell Code Verwaltung** benutzt wird. Es bietet Funktionen zur Versionalisierung und Zusammenarbeit in großen Gruppen. Damit ermöglicht es schnellere iteration der Software und unterstützt somit das [DevOps](../index.md) Konzept.

## Installation

Hilfe: [https://git-scm.com/book/de/v2/Erste-Schritte-Git-installieren](https://git-scm.com/book/de/v2/Erste-Schritte-Git-installieren)

<!-- Help: [https://git-scm.com/book/en/v2/Getting-Started-Installing-Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) -->

Mit dem Befehl ```git --version``` kann auf eine bestehende Installation geprüft werden.

=== "Linux"

    Unter Linux ist Git in der Regel vorinstalliert.

    Sollte das nicht der fall sein, kann Git in der Regel über einen Paketmanager installiert werden:

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

    Der Installationsmanager mit Anleitung findet sich unter [https://git-scm.com/downloads](https://git-scm.com/downloads).

    Unter Windows ist es leichter, mit Linux über das WSL zu entwickeln.
