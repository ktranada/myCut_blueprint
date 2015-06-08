# Schema Information

## barbers
column name | data type | details
------------|-----------|-----------------------
id          | integer   | not null, primary key
shop_id     | integer   | not null, foreign key (references shops)
name        | string    | not null

## Pictures

column name   | data type | details
--------------|-----------|-----------------------
id            | integer   | not null, primary key
imageable     | references| polymorphic: true, index: true 


## Reviews

column name   | data type | details
--------------|-----------|-----------------------
id            | integer   | not null, primary key
author_id     | integer   | not null, foreign key (references users)
shop_id       | integer   | not null, foreign key (references shops)
rating        | integer   | not null
body          | string    | not null



## shops
column name | data type | details
------------|-----------|-----------------------
id          | integer   | not null, primary key
moderator_id| integer   | not null, foreign key (references users)
title       | string    | not null
address     | integer   | not null
city        | string    | not null
state       | string    | not null
zip         | integer   | not null
phone       | integer   | not null
ord         | float     | not null

## tags
column name | data type | details
------------|-----------|-----------------------
id          | integer   | not null, primary key
label       | string    | not null, unique

## taggings
column name | data type | details
------------|-----------|-----------------------
id          | integer   | not null, primary key
shop_id     | integer   | not null, foreign key (references shops)
tag_id      | integer   | not null, foreign key (references tags)

## users
column name     | data type | details
----------------|-----------|-----------------------
id              | integer   | not null, primary key
email           | string    | not null, unique
password_digest | string    | not null
session_token   | string    | not null, unique

