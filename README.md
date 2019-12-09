# Monster Shop

## Description

Monster Shop is an eCommerce platform that simulates a user shopping on a modern eCommerce web application. This application features five main user roles with some sort of associated CRUD functionalities for each role. Visitors to the site can register, add items to their carts, and then go through a checkout process. Merchant users can then see a list of pending orders for their items and fulfill or cancel the orders. Admin users can then activate and deactivate merchants and their associated items. This project featured 52 user stories and was completed as a four member team over a two week sprint.

## Purpose

The purpose of this project is to use Object Oriented Programing and Test Driven Development principles to build an application that simulated an online shopping experience from five different user roles.

### Installation

To install this application on your local machine follow these instructions in your terminal;

1. Clone down the repo into a directory of your choice  `git clone https://github.com/BabsLabs/monster_shop_1908.git`
1. Install all required gems `bundle install`
1. Create database and migrate `rails db:create`,`rails db:migrate`.
1. Start local server `rails s`
1. Open browser and navigate to your local host.
1. Enjoy Monster Shop!

## Focus Areas
- Test Driven Development
- Object Oriented Programing
- Restful routing
- Namespacing and authorization
    - Limiting user functionality
    - Filters (ex. `before_action`)
- Build relationships between models
     - Use those relationships to build out features
- Use of cookies and sessions to store user data
    - Login and Logout / Cart functionality
- ActiveRecord and SQL queries
    - Join multiple tables of data
    - Calculate statistics
- Database management
    - Database designer
- Application deployment
    - Uses Heroku
- Password Hashing

## Technologies / Framework
- Ruby on Rails 5.1.7
- Postgresql
- Postico
- Rspec
- Capybara
- Launcy
- Pry
- Simplecov
- Shouldamatchers

## Screenshots

### Homepage

<img src="https://github.com/BabsLabs/monster_shop_1908-1/blob/master/app/assets/images/monster-shoppe-herokuapp-welcome.png?raw=true"
     alt="Homepage"
     style="float: left; margin-right: 10px;" />

### Registration Page

<img src="https://github.com/BabsLabs/monster_shop_1908-1/blob/master/app/assets/images/monster-shoppe-herokuapp-register.png?raw=true"
     alt="Registration Page"
     style="float: left; margin-right: 10px;" />

### Login Page

<img src="https://github.com/BabsLabs/monster_shop_1908-1/blob/master/app/assets/images/monster-shoppe-herokuapp-login.png?raw=true"
     alt="Login Page"
     style="float: left; margin-right: 10px;" />

### Merchant Index Page

<img src="https://github.com/BabsLabs/monster_shop_1908-1/blob/master/app/assets/images/monster-shoppe-herokuapp-merchants.png?raw=true"
     alt="Merchants Page"
     style="float: left; margin-right: 10px;" />

### Items Index Page

<img src="https://github.com/BabsLabs/monster_shop_1908-1/blob/master/app/assets/images/monster-shoppe-herokuapp-all-items.png?raw=true"
     alt="Items Index Page"
     style="float: left; margin-right: 10px;" />

### Items Show Page

<img src="https://github.com/BabsLabs/monster_shop_1908-1/blob/master/app/assets/images/monster-shoppe-herokuapp-item.png?raw=true"
     alt="Items Show Page"
     style="float: left; margin-right: 10px;" />

### Cart Show Page

<img src="https://github.com/BabsLabs/monster_shop_1908-1/blob/master/app/assets/images/monster-shoppe-herokuapp-cart.png"
     alt="Cart Show Page"
     style="float: left; margin-right: 10px;" />

### User Profile

<img src="https://github.com/BabsLabs/monster_shop_1908-1/blob/master/app/assets/images/monster-shoppe-herokuapp-profile.png?raw=true"
     alt="Cart Show Page"
     style="float: left; margin-right: 10px;" />

### Merchant Dashboard

<img src="https://github.com/BabsLabs/monster_shop_1908-1/blob/master/app/assets/images/monster-shoppe-herokuapp-merchant-dashboard.png?raw=true"
     alt="Cart Show Page"
     style="float: left; margin-right: 10px;" />

### Admin Dashboard

<img src="https://github.com/BabsLabs/monster_shop_1908-1/blob/master/app/assets/images/monster-shoppe-herokuapp-admin-dashboard.png?raw=true"
     alt="Cart Show Page"
     style="float: left; margin-right: 10px;" />

### Admin User Dashboard

<img src="https://github.com/BabsLabs/monster_shop_1908-1/blob/master/app/assets/images/monster-shoppe-herokuapp-admin-users.png"
     alt="Cart Show Page"
     style="float: left; margin-right: 10px;" />

## Database / Schema Diagram

<img src="https://github.com/BabsLabs/monster_shop_1908-1/blob/master/app/assets/images/Monster%20Shop%20Database%20Schema.png?raw=true"
     alt="Cart Show Page"
     style="float: left; margin-right: 10px;" />

## User Roles

- Visitor - is using our website but not logged in.
- Regular User - this user is registered and logged in. Can place items in a cart and checkout to create an order.
- Merchant Employee - works for a merchant. Can fulfill orders for their merchant. Also has same abilities as regular user.
- Merchant Admin - works for a merchant and has additional permissions, like updating merchant information.
- Admin User - has "Super-access" to all areas of Monster Shop.

## Order Status
- 'pending' - a registered user has placed items in the cart and checked out but a merchant has not fulfilled or cancelled that order.
- 'packaged' - the items in the order have all been fulfilled by a merchant user but the item has not moved to the shipped phase.
- 'shipped' - the order has been approved by an admin user and processed as shipped. The order cannot be cancelled by a user at this point.
- 'cancelled' - the order has been cancelled by a user, merchant, or admin. Orders with a 'shipped' status cannot be cancelled.


## Testing

Testing for Monster Shop is done with RSpec. The test suite can be run by running the command `rspec` from your terminal. Feature tests can be run with the command `rspec features` and model tests can be run with the command `rspec models`. Individual test suites can be run with the command format `rspec spec/<path>`. Extensive sad path and failure testing has been done to ensure the best possible user experience.