# nginx
Nginx tips &amp; tricks


## Redirect from non www site to www

    # non-www to www redirect
    if ($host !~* ^www\.)
    {
      rewrite  ^/(.*)$  http://www.$host/$1  permanent;
    }
    
## Reload config

    sudo service nginx reload
