# Autenticação em servidor LDAP com Laravel
Esta aplciação utiliza as seguintes bibliotecas `php`

- php7.2-ldap
- php7.2-sqlite

## Como utilizar

1. Vá no arquivo `.env` e altere as configurações abaixo de **# LDAP Connection settings** e altere com as configurações do seu servidor `ldap`.
2. após isto vá no arquivo `config/adldap.php` e configure o arquivo com as informações do seu servidor DLAP. É necessário fazer isso devido a um bug no pacote 'adlap2/adldap2'
3. Por fim, faça o teste com um usuário do seu servidor AD.

## Observações 

Para utilizar do jeito como está o app, siga o seguinte procedimento:
1. Clone o repositório
```
git clone https://github.com/NeroOficial/laravel-ldap-sample.git laravel-ldap  
cd laravel-ldap  
composer install  
```
2. Configure seu arquivo .env da seguinte forma
```
# Database Connection Settings  
DB_CONNECTION=sqlite  
# LDAP Connection settings  
ADLDAP_CONNECTION=ldap  
ADLDAP_CONTROLLERS=ldap.forumsys.com  
ADLDAP_BASEDN=dc=example,dc=com  
ADLDAP_USER_ATTRIBUTE=uid  
ADLDAP_USER_FORMAT=uid=%s,dc=example,dc=com  
```
3. Execute o servidor do `artisan` no seu projeto e tente fazer login com as credenciais desta página  
[https://www.forumsys.com/tutorials/integration-how-to/ldap/online-ldap-test-server/](https://www.forumsys.com/tutorials/integration-how-to/ldap/online-ldap-test-server/)

4. Caso nenhuma das dicas funcione, eu segui o tutorial abaixo, faça o mesmo hehehe

[https://github.com/jotaelesalinas/laravel-simple-ldap-auth](https://github.com/jotaelesalinas/laravel-simple-ldap-auth)