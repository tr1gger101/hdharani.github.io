## Welcome to Harshit's Blog

In this blog, I write on how I found some web-application vulnerabilites.



### PicsArt's DOM Based XSS

- Just like most websites, PicsArt too uses the "Sign in with Google" function. As I was just playing around with this function, I noticed that there was a "next" parameter in the URL after I logged in through Google. 
- I first thought of an Open-Redirect vulnerablity possibility and entered a random site as the value for the "next" parameter.
- Sad, this didn't work.
- Then, I thought of entering some JavaScript code into the parameter and noticed that the site of responding as per my code.
- I directly went for it. I entered an XSS payload and alas! 
- The page responded with my site's cookie.
- They fixed the vulnerability but unfortunately, there was no acknowledgement from their side 😢

![Image](/bug.jpg)

