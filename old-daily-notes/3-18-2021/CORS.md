# CORS
- stands for cross-origin resource sharing
- cors is an http-header based mechanism that allows a server to indicate which domains can request data from, and what to respond to
    - if something isn't listed as an allowed origin, you'll just throw an error
- when you create a service, you want to specify who can access your data
    - security via authentication/authorization
# Same Origin Policy
    - Browser security prevents a web page from making requests to a different domain than the one that served the web page
    - default policy
    - cors relaxes this security by allowing other domains to make requests to your server
- if you have different server deployed somewhere and it's trying
- anti-forgery tokens prevent attackers from circumventing your origin policy - if an attacker doesn't have this token, then they won't be able to attack hopefully

# CSRF
- cross site request forgery
    - a web security vulnerability that allows an attacker to circumvent the same origin policy, which is designed to prevent different websites from interfering with each other
    - common vulnerability in cookie based systems