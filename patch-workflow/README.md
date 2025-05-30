## FortiGate Patch Automation Workflow

This playbook set automates the firmware patch process for FortiGate:

1. `check_for_patches.yml`: Detect available patch version from FortiGuard.
2. `request_approval.yml`: Email IT and wait for approval.
3. `apply_patch.yml`: Apply the patch if approved.
4. `notify_result.yml`: Email the result.

### Requirements:
- Fortinet FortiOS collection
- SMTP server for email notifications
- Python & Ansible >= 2.11

### Usage:
```bash
ansible-playbook check_for_patches.yml
ansible-playbook request_approval.yml
ansible-playbook apply_patch.yml
ansible-playbook notify_result.yml
```
