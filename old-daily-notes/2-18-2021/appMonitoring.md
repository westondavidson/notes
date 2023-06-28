# Application Monitoring
- highlighting certain events that occur during the program
- this includes debugging!

# Breakpoints
- You can add breakpoints to pause your code at a place and review what's happening in your code step by step
- you can't really use breakpoints in production, so how do we "debug" our code?

# Logging
- You can use logging for program runtime
- you might want to log errors, business logic events, external system transactions, etc.
- this depends on your need

# logging levels
- there are 6 levels of logging which vary in importance, from least to most important
- you can determine what you want to see in your logs
- 

# where are the logs?
- you can store them in files, txt, xml, etc
- DBs
- Console (don't do this lol)
- Etc. - research more!

# Tracing
- similar to logging
- unlike logging, you do tracing to track user interaction with a system
- like tracing their steps!
- this will help diagnose "how" an error arose - what was called, what data changed, etc.