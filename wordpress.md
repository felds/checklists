# Wordpress

> Boas práticas para criação de temas e seus ambientes de desenvolvimento.

### Instalação

+ [ ] Acionar debug

  ```php
  define('WP_DEBUG', true);
  ```
  
+ [ ] Configurar permissões

  Na pasta raiz do Wordpress:
  
  ```sh
  chmod -R ugo=rwX .
  ```  
  
  No `wp-config.php`:
  
  ```php
  define('FS_CHMOD_DIR', (0777 & ~ umask()));
  define('FS_CHMOD_FILE', (0666 & ~ umask()));
  ```
  
+ [ ] Configurar atualizações locais

  No `wp-config.php`:
  
  ```php
  define('FS_METHOD', 'direct');
  ```


### + Jetpack

+ [ ] Habilitar debug no ambiente de desenvolvimento

  ```php
  define('JETPACK_DEV_DEBUG', true);
  ```


### + ACF

+ [ ] Mover para dentro do tema
+ [ ] Habilitar salvamento em JSON
+ [ ] Criar link na pasta de plugins na instalação de debug para fazer atualizações

***

## Deploy

### Plugins importantes

+ [ ] Jetpack

### Nginx

+ [ ] HTTPS + HTTP2

### PHP

+ [ ] Aumentar limite de upload de arquivos
+ [ ] Instalar extensões:
  + [ ] GD

### Segurança e permissões

+ [ ] Desabilitar execução nas pastas de uploads
+ [ ] Permitir atualização pelo admin
+ [ ] Conectar ao Wordpress.com pelo Jetpack
+ [ ] Instalar firewall (fail2ban) para evitar ataques DDoS no `xmlrpc.php`






