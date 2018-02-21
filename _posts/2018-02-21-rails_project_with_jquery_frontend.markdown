---
layout: post
title:      "Rails Project with jQuery Frontend"
date:       2018-02-21 17:37:34 +0000
permalink:  rails_project_with_jquery_frontend
---

*In this assessment your goal is to expand upon the rails assessment you did previously. The goal is to add dynamic features that are possible only through jQuery and a JSON API for your app. *

Taking my Wedded-List app and adding jQuery front-end was a very enjoyable process for me. Since my [rails backend](http://aimeecarney.com/rails_portfolio_project) was completely done and working, I could soley focus on Javascript, specifically using jQuery.

Getting to this point, I wasn't sure if Javascript was for me. I fell in love with Ruby and always saw Javascript as more of a daunting, scary process. However after completing this project I am proud to say that Javascript stole my heart.  I loved using AJAX and being able to grab data from other pages and display on the current page without refreshing. It made me feel like a magician :) 

Once I was able to get the basic GET requests going, I was able to dive further in and edit links or other data to make the page even more dynamic. 

**An example and snippet of my code below:**

*Requirement: "Must render at least one show page (show resource - 'one specific thing') via jQuery and an Active Model Serialization JSON Backend."*

In my lists.js file I added the following:


```
$(".js-next").on("click", function() {
      var nextId = parseInt($(".js-next").attr("data-id")) + 1;
      $.getJSON("/lists/" + nextId + "/list_data", function(data) {
        $(".listName").text(data["name"]);
        $(".listDate").text(data["date"]);
        $(".listCity").text(data["city"]);
        $(".listState").text(data["state"]);
        $(".guestlist").text("");
        $.each(data.contacts, function(index){
            $(".guestlist").append(this.name+"<BR>")
          });
        url = this.url
        cleanUrl = url.substring(0, url.lastIndexOf("/") + 1)
        editUrl = cleanUrl + "edit"
        contactUrl = cleanUrl + "add_contact"
        localUrl = cleanUrl + "local_contact"
        $("#editLink").attr("href", editUrl);
        $("#contactLink").attr("href", contactUrl);
        $(".local_contacts_list").text("");
        $(".load_contacts").attr("href", localUrl);
        // re-set the id to current on the link
        $(".js-next").attr("data-id", data["id"]);
      });
    });
```

What I specifically loved was creating new url's, and swapping out the href values to make sure the page wasn't just loading data, but was functional as well.

I am extremely happy with the way my program is running. And while my application is working how I intend it to, there is still styling I am hoping to get back to, as it is pretty basic right now. 

And finally one of my big takeaways from this project was debugging, specifically [Chrome breakpoints](https://www.youtube.com/watch?v=H0XScE08hy8) which I discovered and will be following up with a blog post explaining how to use.
