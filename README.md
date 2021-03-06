![](https://img.shields.io/badge/Microverse-blueviolet)

# Ruby on Rails

> Learn Ruby on Rails from scratch.


## Built With

- Ruby

## Getting Started

- You will need to have Ruby installed.

- Clone this repo [Ruby on Rails](https://github.com/Emmy-github-webdev/ruby-on-rails).

## Run Ruby on Rails

- cd the directory
- Run rails server

## Things to be cover:

* Ruby version

* System dependencies

* Configuration

* Database creation
> Create Table
- articles table
- Run rails generate migration create_articles
- Go to the migrate folder in db and add the neccessary filed (t.string :title t.text :description)
- Run rails db:migrate
- check the schema file and be sure the table is created

> Drop a table if there is a mistake
- Run rails db:rollback
- Update the table and repeat the step 3 in Create table
> Alternatively, this is the best approach than dropping the table
- Run rails generate migration add_description_to_articles. This will generate a new migration file
- In the new migration file, add the missing fileds e.g
add_column :articles, :description, :text
add_column :articles, :created_at, :datetime
add_column :articles, :updated_at, :datetime
- Run rails db:migrate

> Create Model
- Right click the model folder and create a file article.rb
- In the article.rb add the class
class Article < ActiveRecord::Base

end
- On the CMD run rails console
- Check the article connection: Article.all
- Run Articles - It should display are the fileds in the db
- Instantiate the article - article = Article.new
- User setter to create new article - article.title = "Title one" enter, article.description = "Article description" enter
- Run article - This will display your created article
- Run article.save - To save the data
- Article.all
> Alternatively, all of these can be done in one line of code
- article = Article.new(title: "Title two", description: "Description two")
- article.save

> The 3rd option - This create and save directly to the databse
- Article.create(title: "Title two", description: "Description two")


> Note: Following the casing

> Edit
- Run command article = Article.find(1). # Where 1 id the id of the item you want to delete
- article.title = "This is an edited article title"
- article.save

> Delete
- article = Article.find(1)
- article.destroy

> Validation - Update your article model with the validation expression below
- class Article < ActiveRecord::Base
  validates :title, presence: true, length: {minimum: 3, maximum: 50}
  validates :description, presence: true, length: {minimum: 3, maximum: 50}
end

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions


## Authors

???? **Emmanuel Ogah**

- GitHub: [GitHub](https://github.com/Emmy-github-webdev).
- Twitter: [Twitter](https://twitter.com/OgaemmanuelOga).
- LinkedIn: [Linkedin](https://www.linkedin.com/in/emmanuel-oga-16171584/).


## ???? Contributing

Contributions, issues, and feature requests are welcome!

Feel free to check the [issues page](https://github.com/Emmy-github-webdev/ruby-on-rails/issues).

## Show your support

Give a ?????? if you like this project!


