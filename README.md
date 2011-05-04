# Jquery-rails

This gem adds a single generator to Rails 3, jquery:install. Running the generator will remove any Prototype JS files you may happen to have, fetch jQuery and the jQuery-ujs driver for Rails, and (optionally) fetch jQuery UI.

The gem will also hook into the Rails configuration process, removing Prototype and adding jQuery to the javascript files included by the `javascript_include_tag(:defaults)` call. While the plugin downloads minified and un-minified versions of jQuery and jQuery UI, only the minified versions are included in :default.

### Installation

In your Gemfile, add this line:

    gem "jquery-rails", "~> 0.2"

Then, run `bundle install`. To invoke the generator, run:

    rails generate jquery:install #--ui to enable jQuery UI --version to install specific version of JQuery (default is 1.5)

You're done! Don't forget to output `csrf_meta_tag` somewhere inside your `<head>` tag in your layout!

### Rails 3.1

If you're using Rails 3.1, you need jquery-rails 1.0 or newer. You can specify that by changing your Gemfile line to `gem "jquery-rails", "~> 1.0"`.