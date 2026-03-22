# Ansible playbooks for setting up a multi node Technitium DNS cluster

This may need more more testing/modification for your environment.

My environment:

* 3 x ODROID-C2 SBCs running Fedora 43
* Technitium running in rootless podman as a dedicated user
* Firewalld redirects traffic on low ports (53/tcp,udp) to container high ports (5053/tcp,udp)
* Virtual IP created by Keepalived, health check included on each node

To-do:

* Automate SSL certificate for management interface
* Replace shell commands with modules where available
* Improve documentation, particularly on configuring the Technitium app itself
* Refactor code, modules, etc.
* More testing