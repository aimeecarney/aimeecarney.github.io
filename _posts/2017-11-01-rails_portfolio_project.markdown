---
layout: post
title:      "Rails Portfolio Project"
date:       2017-11-01 17:57:18 +0000
permalink:  rails_portfolio_project
---


For inspiration for my projects, I always think of something that I would find useful. After recently getting married, my mind was still in planning mode and organization. With so many events leading up to the wedding, I found it difficult to organize all the guest lists. The app I created does just that. Wedded List allows you to create lists for events which allows you to upload contacts to. You can then view all the contacts individually which lists their contact information as well as all the events they are invited to. The user is also able to view all the local contacts within the list. 

I set up the associations and models as such:

```
class User < ApplicationRecord
has_many :lists
has_many :contacts, through: :lists
end

class List < ApplicationRecord
belongs_to :user
has_many :list_contacts
has_many :contacts, through: :list_contacts
end

class Contact < ApplicationRecord
has_many :list_contacts
has_many :lists, through: :list_contacts
end

class ListContact < ApplicationRecord
belongs_to :list
belongs_to :contact
end

```

With a ListContact join table, contacts are able to have many lists and lists are able to have many contacts.

I created the user and the user functionality with help from Devise. I was amazed at how little code I could write and Devise would handle the rest for me. For example, I wanted to have the user edit their information, with just the simple path and link in the header view:
```
<%= link_to('View Account', edit_user_registration_path) %>
```

Devise generated a complete edit user page with teh ability to edit email, password and to cancel the account.

After setting up the models and migrations I was able to focus on views, links and having the correct routes. As I’m finding, it is a lot of trial and error; and seeing what works and what breaks. And when it breaks I found binding.pry is my best friend to debug.

This application was by no means a walk in the park. Not only was I worried when I first started that I had retained nothing from all the labs and lessons, but I didn’t even know where to begin with my associations. One thing that helped me, before I even started to plan what I wanted my app to be, was practice. I found [Codecademy](https://www.codecademy.com/) a useful tool to help reinstate everything I just learned over the couple weeks in the rails section. I also re-watched all the lectures that were provided. From there I was able to grasp how I wanted to start and where I should begin in the whole daunting process of developing an app from scratch. 

As I knew from day one, coding is not easy. It can be extremely frustrating and when I want to give up I need to remind myself that the only way for me to truly understand what I’m doing is to keep practicing, to keep writing code. And the blank slate of each portfolio project helps me with that. While it may take me longer than it should for me to complete my projects, reviewing and practicing helps me completely comprehend what I'm doing. 

While my application is not aesthetically pleasing (I’m hoping after Javascript I will have the skills to go back in and make it prettier) it does everything I envisioned. I created a rails app from scratch with very few mental breakdowns. BRING ON JAVASCRIPT.

