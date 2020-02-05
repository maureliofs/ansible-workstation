# ansible-workstation
Ansible playbook for configure my fedora workstation

## Pré-requisitos:
* python
* ansible
* git

Clone o repositório usando o comando:

```shell
git clone https://github.com/maureliofs/ansible-workstation
```

Entre na pasta do projeto:

```shell
cd ansible-workstation
```

Execute o playbook com permissão de superusuário:
```shell
sudo ansible-playbook playbook.yml -i hosts
```