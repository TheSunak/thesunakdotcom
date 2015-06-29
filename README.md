## Swoonatra

New to the **Sinatra DSL // Ruby Web Framework**?
Check out the website **[HERE](http://www.sinatrarb.com/)** and **[GitHub Repo](https://github.com/sinatra/sinatra)**.

At a high level, this template comes with the following features:

- A **modular** Sinatra app using **Ruby 2.1.5** built in to get you started fast.
- Local development, testing and production use **PostgreSQL** for easy Heroku integration.
- Support for **ActiveRecord** model inheritance and database migrations.
- Debugging tools like **Better Errors**, **Pry Debugger**, and **Sinatra Reloader**.
- **RSpec Integration** for testing your application, models, and concerns.
- **Authentication Support** for **API**, **OAuth Keys**, or any sensitive information.

In-line *comments* explain the code base. Feel free to delete as necessary.
This template *does not* come with any UI in place. Styling is up to you.

---

This project is made with <3 and uses a collection of tips and tricks.
Let me know if you have any suggestions via comments via pull request!

### { Getting Started with Swoonatra }

Here are a few sections on how you can get started with this template.

#### >>> GET UP AND RUNNING

In order to use this template:

1.  Clone the repository via: `git clone git@github.com:CarlosPlusPlus/swoonatra.git`
2.  `cd` into the repository and remove the .git folder: `rm -rf .git`
3.  Initialize folder as a Git repository and push up to a created repository on GitHub:
  	- `git init`
	- `git add .`
	- `git commit -m "First commit."`
	- `git remote add origin git@github.com:[**Username**]/[**Repository Name**].git`
	- `git push -u origin master`
4.  Ensure you have **PostgreSQL** installed on your machine.
	- If not installed and on a MAC, use Homebrew via Terminal: `brew install postgresql`
5. Run a `bundle install` to install all gem dependencies.
6. Run `rackup` to start your local server.
7. Visit `localhost:9292` in your favorite browser.

All set and good to go for local development.

Don't forget to update `README.md` with your project specific information!

#### >>> DATABASE SETUP

The `config/database.yml.sample` file contains an example configuration for your local development and test databases. Please run `cp config/database.yml.sample config/database.yml` to get setup locally, and make sure to change the database names as you see fit.

In **production**, the database will automatically connect with the Heroku **postgreSQL** database.

### { Deployment to Heroku }

If you've never used Heroku before, follow this **[Quick Start Guide](https://devcenter.heroku.com/articles/quickstart)** to get setup.
For more technical detail, take a look **[HERE](https://devcenter.heroku.com/articles/getting-started-with-ruby)**.

Once you are ready to launch your application, perform the following steps:

- `heroku create` to create an application on Heroku.
- `heroku addons:add heroku-postgresql:dev` to initialize a Heroku postgreSQL database.
- `heroku config` to see the `[HEROKU_POSTGRESQL_COLOR_URL]`, needed for the next step.
- `heroku pg:promote [HEROKU_POSTGRESQL_COLOR_URL]` to set primary database.
- `git push heroku master` to push your application up to Heroku.
- `heroku open` to open the application and view it on Heroku.

**NOTE** - don't forget to **[create an SSH key](https://devcenter.heroku.com/articles/keys)** for Heroku if you haven't already.

**NOTE** - if you're using ActiveRecord models, you need to run database migrations on Heroku:

- `heroku run rake db:migrate` in your project's root directory.


### { Addtional Informtion }

Here is some additional and important information you should know when using **Swoonatra**.

#### >>> SECURITY & AUTHENTICATION

This template allows you to safeguard against checking in sensitive information into GitHub!

In order to use **API Keys**, **OAuth Keys**, or **sensitive information** in your application:

- In the root directory: `cp config/authentication.example.rb config/authentication.rb`
- Add your information to `config/authentication.rb` as shown in the file.

This will allow you to access them everywhere via the `ENV` hash in your application.


#### >>> GEMFILE

Here are the gems included with this template:

**Framework**

- [activerecord](http://guides.rubyonrails.org/active_record_querying.html)
- [pg](https://github.com/ged/ruby-pg)
- [rake](http://rake.rubyforge.org/)
- [sinatra](http://www.sinatrarb.com/)
- [sinatra-activerecord](https://github.com/bmizerany/sinatra-activerecord)
- [sinatra-contrib](https://github.com/sinatra/sinatra-contrib)
- [sinatra-flash](https://github.com/SFEley/sinatra-flash)
- [sinatra-redirect-with-flash](https://github.com/vast/sinatra-redirect-with-flash)

---

**Development / Debug**

- [better_errors](https://github.com/charliesome/better_errors)
- [binding_of_caller](https://github.com/banister/binding_of_caller)
- [jazz_fingers](https://github.com/plribeiro3000/jazz_fingers)
- [tux](https://github.com/cldwalker/tux)

---

**Test**

- [capybara](www.test.com)
- [factory_girl](www.test.com)
- [rspec](www.test.com)


### { Code Status }

**Code Climate**  
[![Code Climate](https://codeclimate.com/github/CarlosPlusPlus/swoonatra.png)](https://codeclimate.com/github/CarlosPlusPlus/swoonatra)

**Travis CI**  
[![Build Status](https://travis-ci.org/CarlosPlusPlus/swoonatra.png?branch=master)](https://travis-ci.org/CarlosPlusPlus/swoonatra)