# README

## Install Docker
Please install docker desktop or docker cli. After installation run following code in your shell
```
docker run -d --name postgres -h "localhost" -p 5432:5432 -v local_postgres:/var/lib/postgresql/data -e POSTGRES_USER=postgres -e POSTGRES_PASSWORD=postgres postgres:16.1
```

## Install Ruby
Before you install Rails, you should check to make sure that your system has the proper prerequisites installed. These include:

```
Ruby
```
Verify that you have a current version of Ruby installed

```
ruby --version
ruby 2.7.0
```

create .env file in project root and add this lines:
```
DATABASE_NAME=postgres
DATABASE_USER=postgres
DATABASE_PASSWORD=postgres
DATABASE_PORT=5432
DATABASE_HOST=localhost
```
To enforce Ruby to know the .env files,
add this line to the top of your application's Gemfile:

```
gem 'dotenv', groups: [:development, :test]
```
then run this to install postgres connector and bkeepers dotenv
```
bundle add pg
bundle install
```

## Installing Rails
To install Rails, use the gem install command provided by RubyGems:
```
gem install rails
```
To verify that you have everything installed correctly
```
$ rails --version
Rails 7.1.0
```

Clone this repo and run it :
```
bin/rails server
```
and access url from your shell with browser
```
http://127.0.0.1:3000
```


### Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions
