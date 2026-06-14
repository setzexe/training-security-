# Cross Site Scripting

Cross-Site Scripting, also known as **XSS Injection**, happens when a website accidentally lets hackers sneak bad code (typically JavaScript) intp a web page for other peoples view. This is a very common attack vector. It breaks the trust that a site will have for a user, since that site will do whatever is inputted.

While technically it should be called "CSS", that language already exists for web development.

## Mechanics

Sites take input. This can include important forums, or just simple things like a comment section or search bar. These attacks typically involve smaller input areas like this. Attackers will look for these input sections with no real filter or sanitization.

Upon finding this vulnerable input, the attacker will submit some form of input (like a comment) that contains an attack or malicious script. Scripts are wrapped in script tags usually with JavaScript. These inputs get saved directly into the website's database. 

That input is going to affect the site in some way. Let's say its a comment with a script that makes the user click a malicious popup. The user will access the site, like a forum. Because one of these inputtable areas had some script inserted into it and was submitted, the contents of this forum post are visible to anymore, which includes the script. This causes the script to run whenever people access the site. These user's might think it belongs to the website, but it is actually malicious.

## Attack Types

**Persistent** XSS attacks are stored in someway. Like a forum post; inputted forum posts are saved in the database for anyone to see if they visit the website. If this forum takes in malicious input with a script, the browser is going to run the code. **These scripts can do a lot.** Stealing session cookies to steal credentials, taking them to malicious sites, etc.

**Non-persistent** attacks, or **Reflected** attacks, are not necessarily stored on a website. They are instead XSS attacks that happen via an infected URL. Since user's typically can not infect their own URL, attackers will often send users a malicious link that they would see as legit. For instance, an attacker can email a user an Amazon link for a product. In the parameters of this URL, there is actually a hidden script. If the user does not notice this link, the browser will play the script for the user. This can do alot of things; traffic flood, making you click a malicious link, stealing data, etc.

## How to prevent this

When building a website or looking at the security of a website, it comes down to two main rules.

- **Never trust user input.** Always assume a user could inject some malicious code at some point. Website must strip and filter out and information that could lead to XSS. For example, filtering "<" or ">".
- **Encode data** if you can. If a site MUST show user text, showcase it in a harmless manner that just runs off text, not a potential executable.

Things like **being careful with untrusted links** or **keeping applications and security updated** also directly help.