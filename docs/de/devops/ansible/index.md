# Ansible

!!! info "Was ist Ansible"
    Ansible ist ein Automatisierungswerkzeug für Admins, die ihre Aufgaben gerne durch Automatisierung erleichtern würden.

## Installation und Updates

Ansible ist in Python geschrieben. Die Installation findet dementsprechend über [`pipx`](../../languages/python/pipx/index.md) statt.

### Installiere Ansible

=== "Komplette installation (Empfohlen)"

    Volles Ansible Paket:

    ```bash
    pipx install --include-deps ansible
    ```

=== "Minimale installation"

    Nur `ansible-core` installieren:

    ```bash
    pipx install ansible-core #(1)!
    ```

    1. Mit `pipx install ansible-core==$VERSION` kann eine bestimmte Version installiert werden, beispielsweise `pipx install ansible-core==2.12.3`.
