


## How to use

```
docker-compose up -d --build
```

Go to http://localhost:8883

If you deploy this on a server, make sure to change the port of the web service, if more than one project uses
this boilerplate. You must edit the docker-compose.yml to do so. See the documentation for Docker Compose.

You should change the environment variables in the docker-compose.yml
One thing that is really important, is that if you write some client-side JavaScript code, either to GET HTTP
requests using a relative path, or use the full domain name for the server where it's installed.
Hence, when you deploy it to a server, **you should change the value of CONFIG_BACKEND_HOST to match the IP address**
of your server.

Happily, you can simply edit the files under www, and the changes will be reflected in your application.

This docker-compose.yml file also provides some SQL management tools. Note that they are quite unsecure, since
the password for your MySQL user are exposed in cleartext in the docker-compose.yml, and anyone can then change
the contents of your database easily.

Do not use as is in production!
