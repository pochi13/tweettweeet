# README

## users テーブル

| Column              | Type   | Options     　|
| ------------------  | ------ | ----------- 　|
| nickname            | string | null: false 　|
| email               | string | null: false, unique: true |
| encrypted_password  | string | null: false 　|

### Association
has_many :tweets
has_many :comments


## tweetsテーブル

| Column              | Type   | Options     |
| ------------------  | ------ | ----------- |
| user                | reference | foreign_key:true |
| text                | text   | null: false |
| image               | string | null: false 　|
### Association
has_many :comments
belongs_to :user



## comments テーブル

| Column              | Type     | Options     |
| ------------------  | ------   | ----------- |
| name                | string   | null: false |
| text                | text     | null: false |
| tweet               | reference | foreign_key:true |
| user                | reference | foreign_key:true |

### Association
belongs_to :user
belongs_to :tweet


This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
