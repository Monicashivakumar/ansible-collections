# AIDE - Advanced Intrusion Detection Environment

Advanced Intrusion Detection Environment (AIDE) is an application that uses various tools to detect changes to particular files on a system and report on them so that you can maintain baseline file integrity and detect unauthorized changes and potential tootkits.
AIDE takes a "snapshot" of the state of the system, this "snapshot" is used to build a database. When an administrator wants to run an integrity test, AIDE compares the database against the current status of the system. Should a change have happened to the system between the snapshot creation and the test, AIDE will detect it and report it

# Playbooks

`installaide.yaml`:

The install and configure playbook will perform the following:
- Become the superuser.
- Check if the AIDE database exists. This is needed for idempotency, and will fail if the AIDE database exists.
- Install the AIDE package.
- Initialize AIDE, create a baseline, and enable the database.

