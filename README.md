#Store products.


## 1 - Database diagram schema


## 2 - Generating a Ruby on Rails Application
````
	- gem install rails
	- rails new Rails-Store 
	- cd Rails-Store

	Structure 
	├── app
	│   ├── assets
	│   │   ├── images
	│   │   ├── javascripts
	│   │   └── stylesheets
	│   ├── controllers
	│   │   └── concerns
	│   ├── helpers
	│   ├── mailers
	│   ├── models
	│   │   └── concerns
	│   └── views
	│       └── layouts
	├── bin
	├── config
	│   ├── environments
	│   ├── initializers
	│   └── locales
	├── db
	├── lib
	│   ├── assets
	│   └── tasks
	├── log
	├── public
	├── test
	│   ├── controllers
	│   ├── fixtures
	│   ├── helpers
	│   ├── integration
	│   ├── mailers
	│   └── models
	├── tmp
	│   └── cache
	│       └── assets
	└── vendor
	    └── assets
	        ├── javascripts
	        └── stylesheets


````
## 3 - Create the Store table model and migrations:
Adding Users Authentication with Devise Module
[Device install command](http://guides.railsgirls.com/devise/)
````
	- rails g migrate users name:string tel:string address:string email:string:uniq level:integer
	- rails g model newsletters body:text date_newsletter:datetime nb_email:string
	- rails g model orders order_date:datetime id_client:integer 
	- rails g model order_product order_id:integer product_id:integer quantity:integer
	- rails g model products name:string margin_product:decimal 'price:decimal{5,2}'
	- rails g model recipes product_id:integer ingredient_id:integer
	- rails g model ingredients name:string
	- rails g model ingredients_history ingredient_id:integer 'price_ingredient:decimal{5,2}' year:integer
````
## 4 - Create the table Associations:
