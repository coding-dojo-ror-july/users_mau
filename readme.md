# users_mau

vagrant up
vagrant ssh
cd /vagrant
cd projects
ruby new hello
rails server -b 0.0.0.0 or rails s -b 0.0.0.0
ctrl+c
bundle installed
rails generate rails_footnotes:install

# console
rails c
Hirb.enable
quit

# ActiveRecord ORM = Object Relational Mapping
rails generate model User first_name:string last_name:string email:string age:integer
rake db:migrate
User.create(first_name: "Diana", last_name:"Rua", email:"diana@rua.com", age:"36")
user = User.new
user.first_name = "Mau"
user.save
user
user.find(first_name: "Mau")
user.find_by(first_name: "Mau")
user.where(first_name: "Mau").select(:first_name,:last_name)
User.all
User.first 
User.last 
User.second.update(age: 37)
user.destroy
user = User.find(1)
user = User.first.destroy # However, destroy allows callbacks to be executed where delete does not
user = User.last.delete
user.valid?
user.errors
user.errors.full_messages
User.order(:first_name)
User.order(first_name: :asc)
User.find(3).destroy

git remote add origin https://github.com/coding-dojo-ror-july/users_mau.git
git push -u origin master