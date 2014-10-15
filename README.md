flaskblog
=========

Learn python and flask,just a tony blog system  
It is same as [SpringBlog](https://github.com/defshine/SpringBlog),but implemented differently  
  
###Version:v0.2-dev  

##Use:    
  
###Backend:  

  1. [Flask](http://flask.pocoo.org/)
  2. [Flask-SQLAlchemy](https://pythonhosted.org/Flask-SQLAlchemy/) ORM for mysql  
  3. [Flask-WTF](https://flask-wtf.readthedocs.org/en/latest/)
  4. [Flask-Login](https://flask-login.readthedocs.org/en/latest/)  
  5. [Flask-Admin](http://flask-admin.readthedocs.org/en/latest/)  
  6. [Flask-Script](http://flask-script.readthedocs.org/en/latest/)

###Web:  
  
  1. [Bootstrap-3.2.0](http://getbootstrap.com/)    
  2. [CKEditor](http://ckeditor.com/)

##Finish:   
  
1. Review python code and change project directory structure  
2. The basic function of blog:  
  
> Post:read,write,edit,delete  
> Category:read,add,edit,delete  

##Todo   

1. Develop restful api    
2. Develop simple android app

##Deploy    
 
Create Schema on MySql,edit database setting in config.py  
Run script to init database table:  
 
> python manage.py create_db

Create blog admin:  
 
> python manage.py create_user -u admin -p 123456 

###Deploy on virtualenv  
  
Install virtualenv on Ubuntu  
 
> $ sudo install virtualenv
  
Then clone code and setup  

> $ mkdir www  
> $ cd www  
> $ git clone https://github.com/defshine/flaskblog.git  
> $ cd flaskblog  
> $ virtualenv venv  
  
Setup virtualenv  
  
> $ . venv/bin/activate
  
Install packages:  

> $ pip install -r requirements.txt  
> $ pip install -I gunicorn  

Run:  
  
> $ gunicorn -b 0.0.0.0:8005 wsgi_gunicorn:app  

Visit:  
  
Access on http://0.0.0.0:8000  
Admin on http://0.0.0.0:8000/admin  

###Deploy on Ubuntu directly

Use gunicorn and supervisor to deploy this project on Ubuntu  
Install packages:    

> $ pip install -r requirements.txt    

Install gunicorn and supervisor:  

> $ sudo pip install gunicorn  
> $ sudo pip install supervisor  

Copy supervisor config file:  

> $ sudo cp flaskblog.conf /etc/supervisor/conf.d/ 

Restart supervisor and start flaskblog:  
  
> $ sudo supervisorctl reload  
> $ sudo supervisorctl start flaskblog  

Look status:  

> $ sudo supervisorctl status  

Visit:    
    
Access on http://0.0.0.0:8000  
Admin on http://0.0.0.0:8000/admin  

## Version  

v0.2  
v0.1    
 
##Connect me  

Life is short,you need python!
If you are interested in this project, Join us!  

## License  

This project is licensed under the [MIT license](http://opensource.org/licenses/MIT), see `LICENSE` for more details.
