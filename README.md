# nginx
Nginx tips &amp; tricks


## Redirect from non www site to www

    # non-www to www redirect
    if ($host !~* ^www\.)
    {
      rewrite  ^/(.*)$  http://www.$host/$1  permanent;
    }
    
or 
    
    # redirect non-www to www
    server { 
        server_name mysite.com; 
        return 301 http://www.$host$request_uri; 
    }
    
## Reload config

    sudo service nginx reload
