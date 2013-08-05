# Heroku buildpack: Rails + Unicorn + Nginx

### Usage

* Add it to your Heroku config:

  `$ heroku config:add BUILDPACK_URL=https://github.com/joelcogen/heroku-buildpack-rails-unicorn-nginx`
    
* Require unicorn in your `Gemfile`:

    ```ruby
    group :production do
      gem "unicorn"
    end
    ```

* Deploy!

### Customize

You can change the number of Unicorn threads (defaults to 3) by setting the `WEB_CONCURRENCY` environment variable:

    $ heroku config:set WEB_CONCURRENCY=5

See the documentation for the dependencies below for other options to set. Anything you used with the default Ruby buildpack still works.

### Credits

Uses

* [heroku/heroku-buildpack-ruby](https://github.com/heroku/heroku-buildpack-ruby)
* [ryandotsmith/nginx-buildpack](https://github.com/ryandotsmith/nginx-buildpack)

Based on [ddollar/heroku-buildpack-multi](https://github.com/ddollar/heroku-buildpack-multi)
