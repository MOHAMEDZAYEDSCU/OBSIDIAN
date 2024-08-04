
>[!caution]- Lab1 :
>- first of all, spot all the end node that you can use like login and comment fields
>- ---
>- second make sure to check if the end node render your code or not by checking the special character of html at first like :
>	- `'"><s>elzoz}}` this payload almost check the xss and sql vulnerability.
>	- if it rendered, you will find a line along `elzoz` and know you will try to make it a xss vuln instead of html vuln by using html and JS
>---
>- if it doesn't handle the special character like `<h1>` and other tags, done in the previous step
>
>----
>- now just wait and think, what is the dangerous would come of this vulnerability...
>	- like if i found an xss in the login page, what i can get from it like password or account name or what else ??
>	- then determine your methodology to achieve that, (draw the road)
>----


