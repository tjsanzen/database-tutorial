# Demo Static Database

The purpose of this project is to create a completely "static" database that can be
hosted with free resources on the internet.

In this example, we will be create a demo review site for a restaurant.

The only part of this that the end user has to interact with is the review page itself. 
On this page, we have to main elements, the reviews and the submit a review form. 

## The Reviews
The reviews section is built on JavaScript, which using an external api called API
Spreadsheet, we are able to create a Google Spreadsheet, stored in our Google Drive
which, when a new item is added, automatically updates and once the page is refreshed
on the client end, will immediately update. 

## The Submission
It would not be efficient at all if every time someone wanted to leave a review, they
had to email us and we had to add it to the database ourselves. To get around this, we
add a review form to the website, managed for free by external host, Formspree.io. In 
combination with Zapier, we can use their free email parser in this way;

The end user submits a review via Formspree on our site. It then is sent through
Formspree in the format of an email to Zapier's email parser, which locates the wanted
information: in this case, the reviewer's name, the restaurant's name, and their review.
Using this parsed information, it sends it through the main Zapier API into our spreadsheet,
which is automatically updated by Google and accessable to API Spreadsheet to be displayed 
on our completely static website, hosted for free by Github.
