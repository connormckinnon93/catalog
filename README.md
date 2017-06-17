# Udacity Linux Server Project

This project was built as part of the Udacity Linux Server Project and cuses the following specifications.

It also contains the modified item catalog application used on the server.

**Program**: Udacity Fullstack Web Developer Nanodegree

**Project 7:** Linux Server

**Languages/Frameworks:** Python 2.7.x, SQLite, SQLAlchemy, Flask, Google Credentials Manager

**Methodology:** OOP

## Dependencies

This project runs inside the a modified version of the Fullstack Nanodegree VM.

Libraries included in this project are:
- Source code from for Fullstack Nanodegree VM: (https://github.com/udacity/fullstack-nanodegree-vm)
- Git: (https://git-scm.com/downloads)
- VirtualBox: (https://www.virtualbox.org/wiki/Downloads)
- Vagrant: (https://www.vagrantup.com/downloads.html)
- Python 2.7.x: (https://www.python.org/)
- SQLAlchemy: (http://www.sqlalchemy.org/)
- SQLite: (https://www.sqlite.org/)
- Flask: (http://flask.pocoo.org/)

## IP Address and URL

- **Public IP Address**: 52.14.24.188
- **Private IP Address**: 172.26.1.36
- **URL**: ec2-52-14-24-188.compute-1.amazonaws.com

## Software Installed

The following is the installation list pased off the vagrant file for the item catalog project.

```
	sudo apt-get -qqy update
    sudo apt-get -qqy upgrade
    sudo apt-get -qqy install make zip unzip postgresql

    sudo apt-get -qqy install python3 python3-pip
    sudo pip3 -H install --upgrade pip
    sudo pip3 -H install flask packaging oauth2client redis passlib flask-httpauth
    sudo pip3 -H  install sqlalchemy flask-sqlalchemy psycopg2 bleach

    sudo apt-get -qqy install python python-pip
    sudo pip2 -H  install --upgrade pip
    sudo pip2 -H  install flask packaging oauth2client redis passlib flask-httpauth
    sudo pip2 -H  install sqlalchemy flask-sqlalchemy psycopg2
    bleach
```

## Configurations Made

Used postgres to setup a database called catalog using user grader.

Used ufw under with the following setup:
```
	sudo ufw default deny incoming
	sudo ufw allow 2200
	sudo ufw allow 123
	sudo ufw allow 80
	sudo ufw enable
```

## Accessing the Server

`ssh grader@52.14.24.188 -i ~/.ssh/linuxProject -p 2200`
