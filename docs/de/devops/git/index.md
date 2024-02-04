# Git

Wenn man mit einer kleinen Gruppe in einem Projekt zusammenarbeitet, funktioniert das möglicherweise ganz in Ordnung. Doch wie soll es weiter gehen, wenn das Projekt wächst und noch mehr Leute mitarbeiten müssen? Hierkommt Git ins Spiel

Git ist ein **DevOps Werkzeug**, welches für die **Quell Code Verwaltung** benutzt wird. Es bietet Funktionen zur Versionalisierung und Zusammenarbeit in großen Gruppen. Damit ermöglicht es schnellere iteration der Software und unterstützt somit das [GitOps](../index.md) Konzept.

## Installation

Hilfe: [https://git-scm.com/book/de/v2/Erste-Schritte-Git-installieren](https://git-scm.com/book/de/v2/Erste-Schritte-Git-installieren)

<!-- Help: [https://git-scm.com/book/en/v2/Getting-Started-Installing-Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) -->

=== "Linux"

    Unter Linux ist Git in der Regel vorinstalliert
    Mit dem Befehl ```git --version``` kann das überprüft werden geprüft werden.

    === "apt"

        ```bash
        sudo apt install git-all
        ```

    === "dnf"

        ```bash
        sudo dnf install git-all
        ```

=== "Windows"

    Der Installationsmanager findet sich unter [https://git-scm.com/downloads](https://git-scm.com/downloads).
