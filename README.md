# HHLab Hypercard  webapi

## activate

ruby 2.2+ ~
rails 5.0.2
postgress


- git clone 
- cd webapi-react-hypercard

## How to run
*Clone source from github: `git@github.com:ntamvl/rails_5_api_tutorial.git`*
```
cd
git clone https://github.com/johntips/webapi-react-hypercard.git && cd webapi-react-hypercard 
bundle install
```
*Edit `config/database.yml`*

```
default: &default
  adapter: postgresql
  encoding: unicode
  template: template0
  pool: <%= ENV.fetch("RAILS_MAX_THREADS") { 5 } %>
  host: localhost
  port: 5432
  username: postgres
  password: password
  development:
  <<: *default
  database: filter_api_development
```
*Create a new user to get token, type command `rails c`*
                    
```ruby
u = User.create({name: "Tam Nguyen", email: "ntamvl@gmail.com"})
ap u
```
                    
*next typing*
```
rails s
```
*then run in `Terminal`*
```ruby
# with [token] that taken on rails console
curl -H "Authorization: Token token=[token]" http://localhost:3000/v1/users
```

*example*
```
curl -H "Authorization: Token token=3Hu9orST5sKDHUPJBwjbogtt" http://localhost:3000/v1/users
                    
```

## Conclusion

Enjoy creating HHLab hypercard api !!
