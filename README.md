# blog-engine
A simple blog engine created using Django, based upon a relational database.

Trello board: https://trello.com/b/tQiJsd0p/django-blog

Installing necessary dependencies:

	pip install -r requirements.txt

Setting up the latest database version:

	cd sql_scripts
	mysql -u <username> -p < django-blog.sql
	
Making migrations for ORM:

	mysql -u root -p
	<Either make sure that your password is '12345', or edit appropriate entries in 'settings.py'>
	create database django_blog_db
	python manage.py makemigrations
	python manage.py migrate

Creating user groups:

    python manage.py create_groups
	
Backing up the database:

	mysqldump -u root -p django_blog_db > backup.sql
	
The e-mails generated by the mailing service are stored in /sent_emails folder, which is not under version control.
	