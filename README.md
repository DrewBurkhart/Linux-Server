# Linux-Server

> Steps to build my Linux Server Configuration
> that runs apache and serves a python web app.
> This server is hosted on Amazon Web Services
> using the Lightsail platform. It also implements
> standard security measures to defend it from
> common attacks.

The server can be accessed by visiting LINK HERE

##  Logging In

A grader user has been created and given sudo privelages.
This user can ssh into the system using the following command:

```
ssh grader@IP ADDRESS -p 2200
```

## Available Packages

Package | Description
------- | -----------
apache2 | HTTP Server
finger | Displays user info
libapache2-mod-wsgi | Serves Python app
postgresql | Database
git | Version control
python-setuptools | Helps to install Python
sqlalchemy | ORM tools for database
flask | Framework for Python Web Apps
python-psycopg2 | Python PSQL adapter
oauth2 | Auth tools for logging in
glances | Monitoring for bugs

## Configuration Changes
