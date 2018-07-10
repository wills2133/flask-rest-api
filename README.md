# Flask Restful API Template with Mysql

### Install Mysql

`sudo apt-get install mysql-server-5.6`


### Install Required

```
sudo apt-get install python2
sudo apt-get install python-pip
sudo apt-get install python-mysqldb
sudo pip install virtualenv
```

In case Ubuntu  
`sudo apt-get install python-mysql.connector`

or 

In case Mac  
`brew install mysql-connector-python`



### Use Virtualenv

```
virtualenv venv
. venv/bin/activate
pip install -r requirements.txt
```

### Create Database

```
mysql> create database <database_name>;
```


### save environment setting

```
echo 'export APP_ORM_CONFIG=<mode>'>>~/.bashrc
echo 'export APP_DEVELOPMENT_DATABASE_URI=<mysql_uri>'>>~/.bashrc

source ~/.bashrc
```
* \<mode\> = 'development' ('production', 'development', 'testing', 'default')
* \<mysql_uri\> = `mysql://<username>:<password>@<host_ip:host_port>/<database_name>`



### Create database at the first

`echo 'db.create_all()' | ./manage.py shell`


### Run server

`./manage.py runserver  --host 0.0.0.0 --port 5000`


### Test Browser

Try `http://localhost:5000/api/v1/spaces`
