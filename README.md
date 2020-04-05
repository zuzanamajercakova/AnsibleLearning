# AnsibleLearning


# playbook.yml
---
- hosts: ${target}
  sudo: yes

  tasks:
  - name: Copy file
    copy: src=../files/test.py dest=/opt/test.py owner=howardsandford group=admin mode=755

  - name: Execute script
    command: /opt/test.py
