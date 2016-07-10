#Setting The Root Path with Routes

You can direct people toward a specific page by setting a route to point to that page.

Browse Source Code

#1. Show the Homepage of Your App
config/routes.rb

Replace the line

get "pages/home"

...with the following:

root "pages#home"

#Creating More Pages
Most likely, you're going to need more pages besides just a "Home page." (For example, an "About" page or a "Contact Us" page.) In order to do that, you'll have to add a new view and set a route for it.

Browse Source Code

##1. Add a new action in your controller
app/controllers/pages_controller.rb

def about 
end 
##2. Create the HTML in your view
app/views/pages/about.html.erb

<h1>About US</h1>
<p>We are working on our One Month Rails Pinteresting app</p>
##3. Add your route
config/routes.rb

get "about" => "pages#about"

#What is Embedded Ruby?

Embedded Ruby (erb) is like magic! You'll be able to add dynamic content to your HTML pages.

Browse Source Code

##1. Change your HTML link to an embedded Ruby link
app/views/pages/home.html.erb

<%= link_to "here", "#" %>
##2. Review of this lesson
In HTML, a link looks like this

<a href="#">here</a>
These are embedded Ruby tags
<%=  %>
In Ruby on Rails a link will look like this
<%= link_to "here", "#" %>