# Ruby on Rails for Platform.sh

<p align="center">
<a href="https://console.platform.sh/projects/create-project?template=https://raw.githubusercontent.com/platformsh/template-builder/master/templates/rails/.platform.template.yaml&utm_content=rails&utm_source=github&utm_medium=button&utm_campaign=deploy_on_platform">
    <img src="https://platform.sh/images/deploy/lg-blue.svg" alt="Deploy on Platform.sh" width="180px" />
</a>
</p>

This template builds Ruby on Rails 5 on Platform.sh.  It includes a bridge library that will auto-configure most databases and services.

Rails is an opinionated rapid application development framework written in Ruby.

## Services

* Ruby 2.6
* PostgreSQL 11

## Customizations

The following changes have been made relative to a `rails new` generated project.  If using this project as a reference for your own existing project, replicate the changes below to your project.

* The `.platform.app.yaml`, `.platform/services.yaml`, and `.platform/routes.yaml` files have been added.  These provide Platform.sh-specific configuration and are present in all projects on Platform.sh.  You may customize them as you see fit.
* The Platform.sh [Rails helper library](https://github.com/platformsh/platformsh-rails-helper) has been installed via Bundler.  It provides automatic configuration of most databases and services out fo the box.
* We remove the `production` section from  `config/database.yml` the `platformsh-rails-helper` gem will auto-configure the correct credentials.
* In `configt/boot.rb` we set the cache path to the system `/tmp` volume.
* We remove .ruby-version Platform.sh manages the minor version, so it should not be locked.



## References

* [Ruby on Rails](https://rubyonrails.org/)
* [Ruby on Platform.sh](https://docs.platform.sh/languages/ruby.html)
