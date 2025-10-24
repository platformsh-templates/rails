> [!WARNING]
> **This repository is no longer maintained by our internal teams.**  
> The template is provided *as is* and will not receive updates, bug fixes, or new features.  
> You are welcome to contribute on it or fork the repository and modify it for your own use.
> To deploy this template on [Upsun](https://www.upsun.com), you can use the command [upsun project:convert](https://docs.upsun.com/administration/cli/reference.html#projectconvert)
> on this codebase to convert the existing `.platform.app.yaml` configuration file to the [Upsun Flex format](https://docs.upsun.com/create-apps/app-reference/single-runtime-image.html).

# Ruby on Rails for Platform.sh

This template builds Ruby on Rails 5 on Platform.sh.  It includes a bridge library that will auto-configure most databases and services, and ships with PostgreSQL out of the box.  Otherwise it is the same as the result of running "rails new".

Rails is an opinionated rapid application development framework written in Ruby.

## Features

* Ruby 2.6
* PostgreSQL 11
* Automatic TLS certificates
* Bundler-based build

## Customizations

The following changes have been made relative to a `rails new` generated project.  If using this project as a reference for your own existing project, replicate the changes below to your project.

* The `.platform.app.yaml`, `.platform/services.yaml`, and `.platform/routes.yaml` files have been added.  These provide Platform.sh-specific configuration and are present in all projects on Platform.sh.  You may customize them as you see fit.
* The Platform.sh [Rails helper library](https://github.com/platformsh/platformsh-rails-helper) has been installed via Bundler.  It provides automatic configuration of most databases and services out fo the box.
* The `config/database.yml` file has been moved to `config/database.yml.example`.  It is not needed as the database will be configured by the helper gem.  For local development you can create a `database.yml` file to configure as needed.  It has been added to `.gitignore` so it won't get committed to Git.

## References

* [Ruby on Rails](https://rubyonrails.org/)
* [Ruby on Platform.sh](https://docs.platform.sh/languages/ruby.html)
