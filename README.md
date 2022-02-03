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
1 - Run rails generate migration create_articles
2 - Go to the migrate folder in db and add the neccessary filed (t.string :title t.text :description)
3 - Run rails db:migrate
4 - check the schema file and be sure the table is created

> Drop a table if there is a mistake
1 - Run rails db:rollback
2 - Update the table and repeat the step 3 in Create table
- Alternatively, this is the best approach than dropping the table
1 - Run rails generate migration add_description_to_articles. This will generate a new migration file
2 - In the new migration file, add the missing fileds e.g
add_column :articles, :description, :text
add_column :articles, :created_at, :datetime
add_column :articles, :updated_at, :datetime
3 - Run rails db:migrate

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions


## Authors

👤 **Emmanuel Ogah**

- GitHub: [GitHub](https://github.com/Emmy-github-webdev).
- Twitter: [Twitter](https://twitter.com/OgaemmanuelOga).
- LinkedIn: [Linkedin](https://www.linkedin.com/in/emmanuel-oga-16171584/).


## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

Feel free to check the [issues page](https://github.com/Emmy-github-webdev/ruby-on-rails/issues).

## Show your support

Give a ⭐️ if you like this project!


