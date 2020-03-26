# Role de provisionamento do rundeck junto com o LDAP.

## Observação:

Por padrão existe algumas variaveis de configuração dentro de **/rundeck-with-ldap/roles/rundeck/defaults/main.yml** onde eleas podem ser substituidas pela playbook usando o parametro **vars**

## Exemplo:

```bash
---
- name: install rundeck in a maachine centos
  hosts: centos2
  vars:
    - framework_server_name: 'batata'
    - framework_server_hostname: 'batata.com'
    - framework_server_port: '4440'
    - framework_server_url: 'http://batata.com:4440'
    - grails_serverURL: 'http://batata.com:4440'

  roles:
    - rundeck
```
