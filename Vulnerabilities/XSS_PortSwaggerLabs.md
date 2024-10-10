
>[!caution]- Lab1 :
>- first of all, spot all the end node that you can use like login and comment fields
>- ---
>- second make sure to check if the end node render your code or not by checking the special character of html at first like :
>	- `'"><s>elzoz}}[` this payload almost check the xss and sql vulnerability.
>	- if it rendered, you will find a line along `elzoz` and know you will try to make it a xss vuln instead of html vuln by using html and JS
>---
>- if it doesn't handle the special character like `<h1>` and other tags, done in the previous step
>
>----
>- now just wait and think, what is the dangerous would come of this vulnerability...
>	- like if i found an xss in the login page, what i can get from it like password or account name or what else ??
>	- then determine your methodology to achieve that, (draw the road)
>----


>[!caution]- Port_Swagger Testing:
>------
>- it is a fucking simple concept...
>	- just put your payload and see where it will be found
>	- try to test if the simple tags renders or not
>	- if you find your payload `<script>`, try to bypass the syntax with your mind and put your malicious code ...
>	- if it use DOM file ...
>		- if it is link, try to use `javascript:alert()`
>	- if there are firewalls, use burp intruder to test what are the valid tags and attributes to test ....
>---
>- learn how to combine tags and attributes to make a payload ....
>- need to be know the syntax of javascript and html and how they work together ....
>- 