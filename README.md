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

### 1. Create New User

1. Create new user with sudo permissions

```
sudo adduser grader
```

Verify using finger

```
sudo apt-get install finger
finger user
```

2. Give the new user sudo permissions

```
sudo visudo
```

Below the line that reads:
```
root ALL=(ALL:ALL) ALL
```
Add:
```
grader ALL=(ALL:ALL) ALL
```

Save changes

3. Update and Upgrade All Currently Installed Packages

Update all packages using

```
sudo apt-get update
```

providing a list of packages to be upgrade to newer version. We will update those with

```
sudo apt-get upgrade
```

4. Configure SSH

1. Change the SSH config file