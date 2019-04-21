# Rails app

## Details
* Ruby 2.5.1 (x86_64-linux)
* Rails 5.2.3

## Considerations
* This project uses `.env` file to set the `ENV` variables. You should use it as well.
* The `config/database.yml` file is not ignored since it's values won't be visible. If for some reason you need to modify something about it, then use an `ENV` variable.
    * The database names in the `.env` doesn't add the `_development` prefix. You shouldn't add it as well.
* The `APP_HOME` variable that is being set on `Dockerfile` is not added to the `.env` file since it is not needed outside of the docker container and also ~~won't~~ shouldn't be used in any way for the app.
