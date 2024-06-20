
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
>>- <,head>   <,/head>
>>---
>>>[!caution]- Title :
>>>- <,title> book store </,title>
>>>	- it is the minimum description of the website, book store.
>>>	- the name that is appear in the tab itself when  open the website.
>>>	- be in the middle of <,head>
>---
>>[!danger]- Body:
>>- <,body> the following here <,/body>
>>- Contain the Content of the page.
>>---
>>>[!tip]- Headers :
>>>- <,h1 ~ h6>             <,/h1 ~ h6>
>>>	- for make the paragraph header or the topic header in large scale.
>>---
>>>[!faq]- Paragraphs :
>>>- <,p>                  <,/p>
>>>	- for writing the content of the page, for each header.
>>---
>>>[!success]- Lists :
>>>>[!tip]- Unordered List :
>>>>- <,ul> <,/ul>
>>>>	- unordered list.
>>>>	- dots before the list not numbers.
>>>>---
>>>>- <,li> "name of item" <,/li>
>>>>	- should be inside <,ul>
>>>---
>>>>[!quote]- Ordered List:
>>>><,ol> <,/ol>
>>>>	- ordered list
>>>>	- clean and have list numbers.
>>>>---
>>>>- <,li> "name of item" <,/li>
>>>>	- should be inside <,ul>
>>---
>>>[!todo]- Attribute :
>>>- <,a>   <,/a>
>>>---
>>>>[!caution]- link :
>>>>- <,a href="link@mail.c" > hyber_word <,/a>
>>>>	- for making hyperlinks in words and make links.
>>>>	- need to use <,a>
>>>---
>>>>[!bug]- import photo :
>>>>
>>---
>>>[!caution]- Table :
>>>- <,table> <,/table>
>>>	- for making table
>>>	- consists of table-head & table-row
>>>---
>>>>[!todo]- Table Head :
>>>>- <,thead>
>>>>	- for putting data in the head of the table, meta data about the table...
>>>---
>>>>[!danger]- Table Row :
>>>>- <,tr>
>>>>	- for putting data in the same row but separate by space.
>>>>	- should be insdie the <,thead>
>>>>---
>>>>- <,th> <,/th>
>>>>	- the th tag 
>>>>	- the table content.
>>>>	- be inside the <,tr>
>>>---

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
>- <,!-- your comment here -->

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


