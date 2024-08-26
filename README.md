# Lab 4

## Create your first ruby and rails models

In this evaluation, you will be asked to create the first models of your web application `Writter` using Ruby on Rails.

## Instructions

### 1. Create models and database tables

You will have to create 3 independent models (and tables). Later on the course we will
see how to create associations between models, for the moment all models will be independent from each other.

#### 1.1. Creation the `User` model and database table

Create the `User` model and respective database tables with the following attributes:

* `email` (of type `string`)
* `first_name` (type `string`)
* `last_name` (type `string`)
* `created_at` (type `datetime`)
* `updated_at` (type `datetime`)

#### 1.2. Creation the `Post` model and database table

Create the `Post` model and respective database tables with the following attributes:

* `title` (of type `string`)
* `content` (of type `text`)
* `published` (of time `integer`)
* `created_at` (type `datetime`)
* `updated_at` (type `datetime`)
* `author` (type `string`)

#### 1.3. Creation the `Comment` model and database table

Create the `Comment` model and respective database tables with the following attributes:

* `content` (of type `text`)
* `created_at` (type `datetime`)
* `updated_at` (type `datetime`)
* `author` (type `string`)

All attributes must be `NOT NULL` at the database level.

In the `Post` and `Comment` model the attribute `author` will be used to enter the email address of the user that created the `Post` and `Comment` respectively.

### 2. Model validations

Add the necessary validations at the model level:

* All attributes must be present.
* For `Post`'s the content must be longer than 140 characters.
* For `Post`'s the title must be shorter than 100 characters.
* For `Post`'s the published attribute must be an `enum` with 2 options: `published` or `unpublished`.
* For `User`'s email must be unique.
* For `Post` and `Comment` the `author` attribute must be the email of an existing user in the `User` model. For this you will have to create a [Custom Validator](https://guides.rubyonrails.org/active_record_validations.html#performing-custom-validations)

### 3. Create dummy data

Populate the `seeds.rb` file with at least 10 instances of each model.

### Submission

#### 1. Create a repository

Use your existing repository from lab-02 (the one where you created the `Writter` app)

#### 2. Submit the repository link

Upload the repository link to Canvas.
