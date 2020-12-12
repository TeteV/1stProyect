# PHP Lumen RestFul
It's a simple backend CRUD make with:

[Lumen](https://lumen.laravel.com/) Laravel Website.


## First of all
When you clone this repositorie open the terminal and type
```
composer install
```

## General instructions
In your DB gestor create a new database for this project.
```
create database DBNAME;
```

To use this backend you must to clone this repositorie.

Rename ".env.example" to .env and change some things in archive like you have in your DB 
```
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=DBNAME
DB_USERNAME=USERNAME
DB_PASSWORD=USERPSWD
```
## To migrate Database
```
php artisan migrate
```

Once you're in your favorite IDE or not, go to the Terminal and go to the project path
and run with this command
```
php -S yourIp:8000 -t ./public
```

## To add a user
You need a user to do some things like the crud
```
Open postman and type the url http://yourIp:8000/api/signin with POST method
Select form-data
Add: 
key: dni value: 12345678X
key: email value: youremail@email.com
key: name value: yourname
key: password value: yourpassword
and if you want
key: url_image (type file) value: select file
```
Then , when you create the user , go to:
```
http://yourIp:8000/api/login with POST method
Select x-www-form-urlencoded
Add: 
key: email value: youremail@email.com
key: password value: yourpassword
```
And it generate a token, save it.

## To add a room
With the saved token you must to
```
Open postman and type the url http://yourIp:8000/add-room with POST method
Select form-data
key: num value: 345 (for example)
key: num_ppl value: 3
key: size value: 24
key: avaible value: 0
key: api_token value: yourSavedToken
and if you want
key: url_image (type file) value: select file
```

# Kotlin Restful
## Table of Contents
1. [General Info](#general-info)
2. [Data Model](#data-model)
2. [Appearance](#appearance)
3. [Documentation](#docs)
4. [Made with](#technologies)
### General Info
***
A very simple booking management for my hotel in Gran Canaria. \
Is under construction but I put all my energy into it.

## Data Model

In database have the following tables, \
Users Have: Id, Dni, Name (Complete), email, password(codified), api_token, url_img(Thumbnail)\
Rooms Have: num (Room Number), num_ppl (Numbers of people can stay), size, avaible,url_img(Photos of the room), user_Id(FK)\
Booking Have: Check-in, Check-out, Diet, num_room(FK), user_id(FK)\

### RelationShips
A user can only book a room that's available
A user can book  many rooms

A room only can book to one User

### E/R Diagram
![Image text](https://github.com/TeteV/1stProyect/blob/master/img/eR.JPG)

### Relational Model
![Image text](https://github.com/TeteV/1stProyect/blob/master/img/relational.JPG)

### Use Case
![Image text](https://github.com/TeteV/1stProyect/blob/master/img/CassoUso.jfif)

A non Reg Person can only see the available rooms.\
A registered person can see available rooms and book it.

## Appearance
***
There's the login windows, you can log with Facebook/Google Auth or with a basic auth with user and password
![Image text](https://github.com/TeteV/1stProyect/blob/master/img/log-wind.JPG)

***
Here's Sign-in and Sign-up window so simple\
![Image text](https://github.com/TeteV/1stProyect/blob/master/img/sign-in.JPG)
![Image text](https://github.com/TeteV/1stProyect/blob/master/img/sign-up.JPG)
***

There's all the rooms avaible in the hotel, and when you click in your favorite room you see some look like that\
![Image text](https://github.com/TeteV/1stProyect/blob/master/img/search.JPG)
![Image text](https://github.com/TeteV/1stProyect/blob/master/img/searchead.JPG)

***
Here the details of the room: photos and a form where you check/put your info.\
![Image text](https://github.com/TeteV/1stProyect/blob/master/img/deatils.JPG)

***
Here your user details to change/delete your account things\
![Image text](https://github.com/TeteV/1stProyect/blob/master/img/user-deatils.JPG)

### Docs
* [Documentation PDF](https://github.com/TeteV/hotelDocs/blob/master/docs/Documentacion.pdf) (Spanish)


## Made with
[Php Storm](https://www.jetbrains.com/es-es/phpstorm/) Website.

[Postman](https://www.postman.com/) To check the backend works well.

[Adobe XD](https://www.adobe.com/es/products/xd.html)

Readme.md template by [Villanuevand](https://gist.github.com/Villanuevand/6386899f70346d4580c723232524d35a)

---
💻 with 💜 by [TeteV](https://github.com/TeteV) 🐦

