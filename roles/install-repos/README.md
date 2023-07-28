# install-repos

Пример использования:
```yml
- name: Install repositories
  hosts: localhost
  become: true
  gather_facts: true
  roles:
    - role: install-repos
      apt_repositories:
        - repo: 'deb [arch=amd64 signed-by=/etc/apt/trusted.gpg.d/packages.microsoft.gpg] https://packages.microsoft.com/repos/code stable main'
          key: 'https://packages.microsoft.com/keys/microsoft.asc'
          filename: 'vscode'
          keyring: '/etc/apt/trusted.gpg.d/packages.microsoft.gpg'
        - repo: 'deb [arch=amd64 signed-by=/etc/apt/trusted.gpg.d/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu focal stable'
          key: 'https://download.docker.com/linux/ubuntu/gpg'
          filename: 'docker'
          keyring: '/etc/apt/trusted.gpg.d/docker-archive-keyring.gpg'
        - repo: 'deb https://dbeaver.io/debs/dbeaver-ce /'
          key: 'https://dbeaver.io/debs/dbeaver.gpg.key'
          filename: 'dbeaver'
        - repo: 'deb https://packages.clickhouse.com/deb stable main'
          keyserver: 'hkp://keyserver.ubuntu.com:80'
          id: '8919F6BD2B48D754'
          filename: 'clickhouse'
        - repo: 'deb https://download.sublimetext.com/ apt/stable/'
          key: 'https://download.sublimetext.com/sublimehq-pub.gpg'
          filename: 'sublime-text'
        - repo: deb [arch=amd64] https://download.virtualbox.org/virtualbox/debian bullseye contrib
          key: 'https://www.virtualbox.org/download/oracle_vbox_2016.asc'
          filename: 'vbox'
        - repo: 'deb [arch=amd64] https://apt.releases.hashicorp.com bullseye main'
          key: 'https://apt.releases.hashicorp.com/gpg'
          filename: 'hashicorp'
        - repo: deb [signed-by=/etc/apt/trusted.gpg.d/kubernetes-archive-keyring.gpg] https://apt.kubernetes.io/ kubernetes-xenial main
          key: 'https://packages.cloud.google.com/apt/doc/apt-key.gpg'
          keyring: '/etc/apt/trusted.gpg.d/kubernetes-archive-keyring.gpg'
          filename: 'kubernetes'
        - repo: 'deb https://baltocdn.com/helm/stable/debian/ all main'
          key: 'https://baltocdn.com/helm/signing.asc'
          filename: 'helm'
```