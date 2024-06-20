
>[!caution]- About:
>- Hyper text markup language
>- not a programming language(lol)
>- no logic no actual programming, just a presentational language.
>- for build blocks of web. the web pages.
>- .html extension

---
>[!todo]- The Structure :
>- consists of head, body and comments.
>- ![[Pasted image 20240619195814.png]]
>---
>>[!caution]- <!,DOCTYPE html> (always the first)
>>- not a syntax, consider it as a declaration and must be found in the first line.
>>- it is for the html 5 version used in the website
>>- there were a different versions of html types with a different doctype forms.
>---
>>[!success]- Head:
>>- `<head>      </head>`
>>---
>>>[!caution]- Title :
>>>- `<title> book store </title>`
>>>	- it is the minimum description of the website, book store.
>>>	- the name that is appear in the tab itself when  open the website.
>>>	- be in the middle of <,head>
>---
>>[!danger]- Body:
>>- `<body> the following here </body>`
>>- Contain the Content of the page.
>>---
>>>[!tip]- Headers :
>>>- `<h1 ~ h6>             <,/h1 ~ h6>`
>>>	- for make the paragraph header or the topic header in large scale.
>>---
>>>[!faq]- Paragraphs :
>>>- `<p>        </p>`
>>>	- for writing the content of the page, for each header.
>>---
>>>[!success]- Lists :
>>>>[!tip]- Unordered List :
>>>>- `<ul>          </ul>`
>>>>	- unordered list.
>>>>	- dots before the list not numbers.
>>>>---
>>>>- `<li> "name of item" </li> `
>>>>	- should be inside <,ul>
>>>---
>>>>[!quote]- Ordered List:
>>>>`<ol>       </ol>`
>>>>	- ordered list
>>>>	- clean and have list numbers.
>>>>---
>>>>- `<li> "name of item" </li>`
>>>>	- should be inside <,ul>
>>---
>>>[!todo]- Attribute :
>>>- `<a>      </a>`
>>>---
>>>>[!caution]- link :
>>>>- `<a href="link@mail.c" > hyber_word </a>`
>>>>	- for making hyperlinks in words and make links.
>>>>	- need to use <,a>
>>>---
>>>>[!bug]- import photo :
>>>>
>>---
>>>[!caution]- Table :
>>>- `<table>       </table>`
>>>	- for making table
>>>	- consists of table-head & table-row
>>>---
>>>>[!todo]- Table Head :
>>>>- `<thead>`
>>>>	- for putting data description in the head of the table like, name - age - collage. and under each column the actual data of that category.
>>>>	- prefered to use <,th> for each name and <,tr> for the same row
>>>---
>>>>[!danger]- Table Body :
>>>>- for putting the data of each category, like name of customers under the name section.
>>>>---
>>>>- `<tr>`
>>>>	- for putting data in the same row but separate by space.
>>>>	- should be insdie the <,thead>
>>>>---
>>>>- `<th>      </th>`
>>>>	- the th tag 
>>>>	- the table content.
>>>>	- be inside the <,tr>
>>---
>>>[!tip]- DIV :
>>>- `<div "your command" > </div>`
>>>	- it is generic block content
>>>	- group and organize content
>>>	- need the actual command inside it to organize it and make it as a block, but it didn't do anything by itself.
>>>---
>>>- it is better be with css or javascript to perform better results on the overall shape.
>>---
>>>[!caution]- Input :
>>>- `<input type="" name="">`
>>>	- for interring inputs and specify type and name for the input.
>>>	- 

---
>[!bug]- Syntax Style :
>- to make some sort of shape to the words.
>- bold, underline, color, not straight, ...
>---
>>[!todo]- <,Strong> :
>>- for make the syntax bold
>
>>[!success]- <,em> :
>>- for emphasize, not straight lines.
>
>>[!caution]- 

---
>[!tip]- Comments :
>- `<!-- your comment here -->`

---
>[!caution]- Inline & Block Element :
>>[!todo]- Inline :
>>- don't start a new line
>>- take only the necessary width
>>---
>>- <,span> | <,img> | <,a> | <,strong>
>---
>>[!danger]- Block :
>>- Start on a new line
>>- Take full width available.
>>---
>>- <,div> | <h1~6> | <,form>

---
#### Forms :
- interacting with the data.
- GET, POST, DELETE and UPDATE(was a command with 3 char !!!) used here.
- the important part for the security features.
 ----
<br>
```html
<form action="submit_page.php" method="post">
    <!-- Form elements go here -->
</form>

<!-- ============================================ -->
<!-- ============================================ -->

<!-- Action: Specifies the URL to which the form data is sent when the form is submitted. -->

<form action="/submit_page">

<!-- ============================================ -->
<!-- ============================================ -->

<!-- Method: Specifies the HTTP method to be used when sending form data. Common values are GET and POST. -->

<form method="post">

<!-- ============================================ -->
<!-- ============================================ -->

<!-- Name: Specifies the name of the form. -->

<form name="myForm">

<!-- ============================================ -->
<!-- ============================================ -->

<!-- Target: Specifies where to display the response received after submitting the form. Common values are _self, _blank, _parent, and _top. -->

<form target="_blank">

<!-- ============================================ -->
<!-- ============================================ -->

<!-- Enctype: Specifies how the form data should be encoded when submitted. Common values are application/x-www-form-urlencoded (default), multipart/form-data (for file uploads), and text/plain. -->

<form enctype="multipart/form-data">

<!-- ============================================ -->
<!-- ============================================ -->

<!-- Autocomplete: Specifies whether the form should have autocomplete on or off. -->

<form autocomplete="off">

<!-- ============================================ -->
<!-- ============================================ -->

<!-- Input Elements: Various types of input fields. -->

<input type="text" name="username" placeholder="Enter username">
<input type="password" name="password" placeholder="Enter password">
<input type="email" name="email" placeholder="Enter email">
<input type="submit" value="Submit">
<input type="radio" name="gender" value="male"> Male
<input type="radio" name="gender" value="female"> Female
<input type="checkbox" name="subscribe" value="newsletter"> Subscribe to newsletter

<!-- ============================================ -->
<!-- ============================================ -->

<!-- Textarea: Multi-line text input. -->

<textarea name="message" rows="4" cols="50" placeholder="Enter your message"></textarea>

<!-- ============================================ -->
<!-- ============================================ -->

<!-- Select: Drop-down list. -->

<select name="country">
    <option value="usa">USA</option>
    <option value="canada">Canada</option>
    <option value="uk">UK</option>
</select>

<!-- ============================================ -->
<!-- ============================================ -->

<!-- Button: Button element that can be used to submit the form or trigger JavaScript functions. -->

<button type="submit">Submit</button>
<button type="button" onclick="alert('Hello!')">Click Me</button>

<!-- ============================================ -->
<!-- ============================================ -->

<!-- Fieldset and Legend: Used to group related elements within a form. -->

<fieldset>
    <legend>Personal Information</legend>
    <label for="name">Name:</label>
    <input type="text" id="name" name="name"><br><br>
    <label for="email">Email:</label>
    <input type="email" id="email" name="email">
</fieldset>

<!-- ============================================ -->
<!-- ============================================ -->

<!-- Example of a Complete Form -->

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Form Example</title>
</head>
<body>
    <form action="/submit_page.php" method="post" enctype="multipart/form-data" autocomplete="on" target="_self">
        <fieldset>
            <legend>Personal Information</legend>
            <label for="username">Username:</label>
            <input type="text" id="username" name="username" required><br><br>
            <label for="password">Password:</label>
            <input type="password" id="password" name="password" required><br><br>
            <label for="email">Email:</label>
            <input type="email" id="email" name="email" required><br><br>
            <label for="gender">Gender:</label><br>
            <input type="radio" id="male" name="gender" value="male">
            <label for="male">Male</label><br>
            <input type="radio" id="female" name="gender" value="female">
            <label for="female">Female</label><br><br>
            <label for="subscribe">Subscribe to newsletter:</label>
            <input type="checkbox" id="subscribe" name="subscribe" value="newsletter"><br><br>
        </fieldset>
        <fieldset>
            <legend>Message</legend>
            <label for="message">Your Message:</label><br>
            <textarea id="message" name="message" rows="4" cols="50" placeholder="Enter your message"></textarea><br><br>
        </fieldset>
        <fieldset>
            <legend>Country</legend>
            <label for="country">Select your country:</label>
            <select id="country" name="country">
                <option value="usa">USA</option>
                <option value="canada">Canada</option>
                <option value="uk">UK</option>
            </select><br><br>
        </fieldset>
        <input type="submit" value="Submit">
    </form>
</body>
</html>

<!-- ============================================ -->
<!-- ============================================ -->

```

---

#### Example of a Table :
```html
<!-- for making a simple table with the list concept -->
<table>
<!-- for the same row data -->
	<tr> 
		<th> Name </th>
		<th> Age </th>
		<th> Collage </th>
	</tr>
<!-- for ordered list data -->
	<ol> 
		<li> Name </li>
		<li> Age </li>
		<li> Collage </li>
	</ol>

</table>

```


