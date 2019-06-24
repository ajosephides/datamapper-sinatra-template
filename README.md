Sinatra, Data Mapper, Postgres and RSpec project template
----------------

Intro
------
A template for a simple app to use Sinatra and DataMapper.
There is some manual setup (see below). In future versions this could be improved with a Rakefile.
The template consists of a file structure and test setup so that both _development_ and _test_ can be run locally on a `postgres` database.

Technology Used
---------------
- [Sinatra](http://sinatrarb.com/)
- [Postgres](https://www.postgresql.org/)
- [DataMapper](https://datamapper.org)
- [Database Cleaner](https://github.com/DatabaseCleaner/database_cleaner)
- [RSpec](https://rspec.info/)

Setup
-----
- Please start by forking this repo.
- In a terminal run `psql`
- Create your databases - test and development:

```
CREATE DATABASE [YOUR_APP_NAME]_test;
CREATE DATABASE [YOUR_APP_NAME]_development;
```
- Set app name in `./app/app.rb`
- In `config.ru` add your app name
- Set app name in `./spec/.spec_helper.rb` for Capybara
- In `data_mapper_setup` add your app name that corresponds to your database
- As app develops add the `require_relative '../lib/[MODEL]` into `./db/data_mapper_setup.rb`
