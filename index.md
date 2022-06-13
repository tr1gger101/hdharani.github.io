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

 <img src="/bug.jpg" width="500" height="500">
 
 
 ### IDOR on my college's website
 
- This was a pretty basic finding.
- The URL had an integer as their profile id's for example https://www.example.com/profile/1
- The page displayed personal details of every student enrolled in the college.
- Upon changing the profile id to a different integer, it displayed details of the student corresponding to their id.
- This leaked personal details of students.

