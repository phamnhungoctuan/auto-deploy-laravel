# Auto deploy Laravel source with Envoy 
Laravel Envoy provides a clean, minimal syntax for defining common tasks you run on your remote servers. Using Blade style syntax, you can easily setup tasks for deployment, Artisan commands, and more. Currently, Envoy only supports the Mac and Linux operating systems.


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
