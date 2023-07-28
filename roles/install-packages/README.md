# install-packages

Пример использования:
```yml
- name: Install packages
  hosts: localhost
  become: true
  gather_facts: true
  roles:
  - role: install-packages
      packages:
        - name: apt-transport-https
        - name: ca-certificates
        - name: cups
        - name: curl
        - name: wget
        - name: whois
        - name: wireguard
        - deb: https://downloads.realvnc.com/download/file/viewer.files/VNC-Viewer-6.22.315-Linux-x64.deb
        - deb: https://go.skype.com/skypeforlinux-64.deb
        - deb: https://dl.google.com/linux/deb/pool/main/g/google-chrome-stable/google-chrome-stable_100.0.4896.127-1_amd64.deb
        - deb: https://downloads.mongodb.com/compass/mongodb-compass_1.31.1_amd64.deb
        - deb: https://github.com/jgraph/drawio-desktop/releases/download/v17.4.2/drawio-amd64-17.4.2.deb
```