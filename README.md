# Requirements & Project starter

[![forthebadge](https://forthebadge.com/images/badges/built-with-wordpress.svg)](https://forthebadge.com)

First install docker & docker-compose on your VPS

Copy your `wp-content` in the `wp-content` directory

Edit the `.env` file and :

```
    docker-compose -f docker-[env] up -d
```

# Access Database from your local env

In the docker compose file , we have exposed the port 3306, You can log in with your favorite tool like sequel pro or with the adminer instance on port 10000 ( DEV ONLY ).

If you don't need direct access, remove : 

```
    ports:
       - "3306:3306"
```

## Stop the Server : 

```
    docker-compose -f docker-[env] stop
```

## Remove Caddy Container & Image : 

```
    docker rm CADDYCONTAINERID -f
    docker rmi CADDYIMAGEID -f
    docker system prune
```

# Licence

The MIT License

Copyright (c) 2018 JUST1B

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
