# Wordpress

Boas práticas para criação de temas e seus ambientes de desenvolvimento.

## Desenvolvimento

* [ ] Acionar debug

  ```php
  // wp-config.php
  define('WP_DEBUG', true);
  ```

* [ ] Configurar permissões

  Na pasta raiz do Wordpress:

  ```sh
  chmod -R ugo=rwX .
  ```  

  ```php
  // wp-config.php
  define('FS_CHMOD_DIR', (0777 & ~ umask()));
  define('FS_CHMOD_FILE', (0666 & ~ umask()));
  ```

* [ ] Configurar atualizações locais

  ```php
  // wp-config.php
  define('FS_METHOD', 'direct');
  ```
  
* [ ] Carregar snippet do Livereload quando em modo debug
  
	```php
	// functions.php
  	add_action('wp_enqueue_scripts', function () {
	  	if (constant('WP_DEBUG')) {
			wp_enqueue_script('livereload', "//{$_SERVER['HTTP_HOST']}:35729/livereload.js?snipver=1", [], null, true);
	  	}
  	});
	```
 


### + Jetpack

* [ ] Habilitar debug no ambiente de desenvolvimento

  ```php
  // wp-config.php
  define('JETPACK_DEV_DEBUG', true);
  ```


### + ACF

* [ ] [Mover plugin para dentro do tema](https://www.advancedcustomfields.com/resources/including-acf-in-a-plugin-theme/)

* [ ] [Habilitar salvamento em JSON](https://www.advancedcustomfields.com/resources/local-json/)  
  (a pasta onde o JSON é salvo deve ter as permissões `0777` ou `ugo=rwX`)

* [ ] Criar link na pasta de plugins na instalação de debug para fazer atualizações
  
  ```sh
  cd wp-content/plugins/
  ln -sf "../themes/$TEMPLATE_NAME/acf" .
  ```

* [ ] Caso haja a licensa do ACF PRO, habilitar o plugin e inserir a chave


## Deploy

### Plugins importantes

* [ ] Jetpack

### Nginx

* [ ] HTTPS + HTTP2
* [ ] Varnish

### PHP

* [ ] Aumentar limite de upload de arquivos
* [ ] Instalar extensões:
  * [ ] GD

### Segurança e permissões

* [ ] Desabilitar execução nas pastas de uploads
* [ ] Permitir atualização pelo admin
* [ ] Conectar ao Wordpress.com pelo Jetpack
* [ ] Instalar firewall (fail2ban) para evitar ataques DDoS no `xmlrpc.php`
