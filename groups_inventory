--example groups inventory


[dev]
173.121.34.21

[test]
173.123.36.23

example if hosts 'dev' below example reference 
---
- name: first playbook
  hosts: dev
  become: yes
  tasks:
    - name: install httpd software
      yum:
        name: httpd
        state: latest
    - name: start web server
      service:
        name: httpd
        state: started

example if host 'all' means 'dev+test'

---
- name: first playbook
  hosts: all
  become: yes
  tasks:
    - name: install httpd software
      yum:
        name: httpd
        state: latest
    - name: start web server
      service:
        name: httpd
        state: started
