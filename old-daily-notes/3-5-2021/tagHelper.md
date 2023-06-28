# tag helpers
- tag helpers enable server-side code to participate in creating and rendering HTML elements in razor files
- a way to tie your views to your logic in your program
- example: tag helper asp-for can tie a property of an object to an html tag!
- all tag helpers do is tie your views to the underlying objects that are coming in!
- helpers are also used to tie views to particular actions in controllers

- razor syntax allows adding logic to html
    - tag helpers are a part of razor syntax

# two types of helpers
1. HTML helpers
    - used to help render complex content
    - basically just methods that let you render html
1. MVC Tag Helpers
    - tag helpers are attributes of our html elements
- tag helpers are preferrable, but if a tag helper is unavailable, html helpers can be used
- Html.something is an html helper - our actionlinks are html helpers
- asp-something are tag helpers, and looks like an atribute of an html tag

# form tag helper
- some views just need an action to route to, so instead of creating a whole new controller, we just call an action that occurs in a preexisting controller - example: asp-action="Create" means that you submit the form to the herocontroller to the create action

# label tag helper
- gives the label for a model value

# more notes
- using an input tag helper means that the data type of a tag is tied to what the input type is of the property

