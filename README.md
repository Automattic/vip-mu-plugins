# VIP (WPCOM) mu-plugins

## Usage

Install this directory to `wp-content/mu-plugins` in your local development environment. Full setup instructions can be [found here](http://wp.me/p9nvA-75T).

## Differences

This repo will help bridge the gap between WordPress.com VIP and your local development environment but will not provide a 1:1 setup. Some known missing pieces include:

* Protected Embeds
* ...

## Concatention

To enable nginx-http-concat, you'll need to define the `QUICKSTART_ENABLE_CONCAT` constant in `wp-config.php` and add the relevant configuration to your webserver. For example, in Nginx:

```
location /_static/ {
        fastcgi_pass unix:/var/run/fastcgi.sock;
        include /etc/nginx/fastcgi_params;
        fastcgi_param SCRIPT_FILENAME $document_root/wp-content/plugins/http-concat/ngx-http-concat.php;
}
```
