# ansible-workstation
Playbook ansible usado para configurar meu ambiente de trabalho fedora.

## Pré-requisitos:
* Python
```shell
$ dnf install python
```
* Ansible
```shell
$ dnf install ansible
        ou
$ pip install ansible
```
* Git
```shell
$ dnf install git
```
1. Clone o repositório usando o comando:

```shell
git clone https://github.com/maureliofs/ansible-workstation
```

2. Entre na pasta do projeto:

```shell
cd ansible-workstation
```

Para editar os pacotes a serem instalados basta ir no arquivo `roles/programas/defaults/main.yml` e adicionar ou remover os pacotes desejados.

No arquivo `playbook.yml` edite o valor da variável `ansible_user_id` para o nome do seu usuário do sistema.

Caso não queira instalar alguma das roles, basta remover da lista no arquivo `playbook.yml`

3. Execute o playbook com permissão de superusuário:
```shell
sudo ansible-playbook playbook.yml -i hosts
```