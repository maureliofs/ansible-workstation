# ansible-workstation
Playbook ansible usado para configurar meu ambiente de trabalho Fedora ou Ubuntu/Debian.

## Pré-requisitos:
* Python

* Ansible
  
1. Instalação do Ansible no Fedora via dnf:
```shell
sudo dnf install ansible
```

2. Instalação do Ansible no Ubuntu via apt:
```shell
sudo apt install ansible
```

3. Instalação do Ansible via pip:
```shell
pip install ansible
```

* Git
1. Instalação do Git no Fedora:
```shell
sudo dnf install git
```

2. Instalação do Git no Ubuntu:
```shell
sudo apt install git
```

### Execução do Playbook

1. Clone o repositório usando o comando:

```shell
git clone https://github.com/maureliofs/ansible-workstation
```

2. Entre na pasta do projeto:

```shell
cd ansible-workstation
```

Para editar os pacotes a serem instalados basta ir no arquivo `roles/fedora/defaults/main.yml`, caso a distribuição seja o Fedora ou  `roles/ubuntu/defaults/main.yml`, caso seja Ubuntu/Debian e adicionar ou remover os pacotes desejados.

No arquivo `playbook.yml` edite o valor da variável `ansible_user_id` para o nome do seu usuário do sistema.

Caso não queira instalar alguma das roles, basta remover da lista no arquivo `playbook.yml`

3. Execute o playbook com permissão de superusuário:
```shell
sudo ansible-playbook playbook.yml -i hosts
```
