# ansible-workstation
Playbook ansible usado para configurar meu ambiente de trabalho Fedora ou Ubuntu.

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

> A role `fedora` e `ubuntu` tem como objetivo instalar todos os programas necessários dependendo da distribuição usada.

>  A role `zsh` instala e configura o `zsh` que é uma alternativa ao `bash` e o `Oh-My-Zsh` usado para gerenciar os temas e plugins.

> Para editar os pacotes a serem instalados basta ir no arquivo `roles/fedora/defaults/main.yml`, caso a distribuição seja o Fedora ou  `roles/ubuntu/defaults/main.yml`, caso seja Ubuntu e adicionar ou remover os pacotes desejados.

> No arquivo `playbook.yml` edite o valor da variável `ansible_user_id` para o nome do seu usuário do sistema.

>Caso não queira instalar alguma das roles, basta remover ou comentar a role da lista no arquivo `playbook.yml`


3. Execute o playbook com permissão de superusuário:
```shell
sudo ansible-playbook playbook.yml -i hosts
```
## Testes

Este projeto foi testado no **Ubuntu 18.04 LTS** e **Fedora 31** usando o **Ansible 2.9.5**. 