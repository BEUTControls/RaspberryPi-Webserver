# RaspberryPi-Webserver
Setting up Apache

Information pulled from:

https://www.raspberrypi.org/documentation/remote-access/web-server/apache.md

We will setup a page to display a simple webpage.

Get the updates for the raspberry pi

```sudo apt-get update```

Install the updates for the raspberry pi

```sudo apt-get upgrade```

Install Apache2

```sudo apt install apache2 -y```

After the install you should be able to see the Apache2 Debian Default page. 

Goto ```http://YOUR RPI IP ADDRESS```

Now we will copy the index.html page, delete and create a new index.html file

```cd /var/www/html```

```cp index.html index-orginal.html```

```sudo rm index.html```

```sudo nano index.html```

```
<!DOCTYPE html>
<html>
  <head>
    <title>Simple page</title>
  </head>
  <body>
    You now have your own webpage
    <p></p>
    <a href="main.html">Link to your second webpage</a>
  </body>
</html>
```

Now create another webpage in the same folder. We will call this main.html. We should still be in /var/www/html

```
<!DOCTYPE html>
<html>
  <head>
    <title>This is your second webpage</title>
  </head>
  <body>
    This is the body of main.html
  </body>
</html>
```

Now navigate to web browser and enter ```http://YOUR RPI IP ADDRESS```

You should see the first webpage you created with a link to the second page.
