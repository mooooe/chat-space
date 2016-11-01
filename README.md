# data base design

## overview
* users can message other users
* users can create chat groups

## tables

### messages
|user_id|group_id|text|image|
|:---:|:---:|:---:|:---:|
|integer|integer|text|text|

### groups
|group_name|
|:---:|
|integer|

### group_users
|user_id|group_id|
|:---:|:---:|
|integer|integer|

## asociation

### message
* belongs_to :user
* belongs_to :group

### group
* has_many :user
* has_many :messages
* has_many :group_users

### group_user
* belongs_to :user
* belongs_to :group
