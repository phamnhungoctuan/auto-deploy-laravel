# auto-deploy-laravel
Auto deploy source with Laravel Envoy

# Install Envoy:

```composer global require laravel/envoy```

# Update env PATH

- export PATH="$PATH:~/.composer/vendor/bin"
- source ~/.bashrc
- edit $gitRepo

# Update virtual host: add *current* path

+ Nginx:

        root /home/tuanpham.dev/public_html/current/public;
	
+ Apache: 

	``DocumentRoot /www/tuanpham.dev/public_html/current/public``

# Deploy

``envoy run deploy --branch=master``
