#Readme

This is Docker Debian based image for web development with php5.6.4

##Usage
Build image firstly

```bash
sudo docker build --rm -t `whoami`/debian:jessie.php56 .
```

Start your container with share local folder

```bash
echo "<?php phpinfo(); ?>" > /tmp/index.php
sudo docker run -d --name web -p 80:80 -v /tmp/index.php:/var/www/index.php jdoe/debian:jessie.php56
```

And browse: [http://localhost/index.php](http://localhost/index.php). You must see phpinfo() as result.