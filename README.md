# auto-deploy-laravel
Auto deploy source with Laravel Envoy


# Required:
+ Node
+ Yarn
+ Composer

# Install Envoy:

```composer global require laravel/envoy```

# Update env PATH

- export PATH="$PATH:~/.composer/vendor/bin"
- source ~/.bashrc
- edit $gitRepo in Envoy.blade.php
- Move Envoy.blade.php to laravel source (not public path)

# Update virtual host: add *current* path

+ Nginx:

        root /home/tuanpham.dev/public_html/current/public;
	
+ Apache: 

	``DocumentRoot /www/tuanpham.dev/public_html/current/public``

# Deploy

``envoy run deploy --branch=master``
