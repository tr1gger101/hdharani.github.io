## Welcome to Harshit's Blog

In this blog, I write on how I found some web-application vulnerabilites.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### PicsArt's DOM Based XSS

- Just like most websites, PicsArt too uses the "Sign in with Google" function. As I was just playing around with this function, I noticed that there was a "next" parameter in the URL after I logged in through Google. 
- I first thought of an Open-Redirect vulnerablity possibility and entered a random site as the value for the "next" parameter.
- Sad, this didn't work.
- Then, I thought of entering some JavaScript code into the parameter and noticed that the site of responding as per my code.
- I directly went for it. I entered the XSS payload <script>alert(document.cookie)</script> and alas! 
- The page responded with my site cookie.

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](blob:https://web.whatsapp.com/dcfe51d5-b212-45b0-b548-6f21b84e4e5b)
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/tr1gger101/tr1gger101.github.io/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.

