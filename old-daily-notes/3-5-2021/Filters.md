
- filters allow code to be run before or after specific stages in a request process
- filters handle tasks like authorization and response caching
- you run filters inside action execution
- you can use filters to have a single action
- you select an action, run the filters, then return what you need

- there are 5 filter types that run at different times in the aaction process - look over the slides/table for these!!!

- even if you don't have any filters middleware, try-catch and more will catch exceptions within the pipeline and will send an HTTP 500 error

- I WILL NEED TO GO OVER THIS STUFF LATER
- logging in a before action filter?

- exception filters inherit from the iexceptionfilter

- filters run when we've already selected a controller and an action - when you're in your mvc context

- middleware runs before a controller is reached/before you reach your mvc context