Create and include an age-check snippet
 

From your Shopify admin, go to Online Store > Themes.
Find the theme you want to edit, and then click Actions > Edit code.
Click on the Snippets folder to expand and view its content.
Under the Snippets folder, click on Add a new snippet.
Name your new snippet age-check, and click Create snippet. Your age-check snippet will open in the online code editor.
ageverify01.jpg
In a new browser tab, open the following file.
Copy all of the code you see there and return to your Themes page.
In the online code editor, paste the code you copied into your age-check.liquid snippet.
Save your changes.
In the Layouts folder, locate and click on your theme.liquid file to open it in the online code editor.
In the online code editor, scroll down a bit until you see the opening <body> tag.
Right after the opening <body> tag, paste the following code:

{% render 'age-check' %}
 

This will include the age-check.liquid snippet at the very beginning of the body content of your theme file.
Click Save to save your changes.
What if I want to show an image in the background?
 

Upload a large JPG image (at least 1024 by 1024 pixels) to your theme assets on the Edit HTML/CSS page. Rename that file age-check-background.jpg.


To see the age verification in action, take a look at this demo store.

 

Changing the age limit
 

In your age-check.liquid snippet, change the following code on line number 2:


{% assign age = 18 %}
 

to:


{% assign age = 21 %}
 

You can also edit the text on lines 6 and 10.

 

What if I want to add a date of birth picker?
 

In your age-check.liquid snippet, change the following code on line number 1:


{% assign enter_date_of_birth = false %}
 

to:


{% assign enter_date_of_birth = true %}
 

Testing the functionality
 

Once you have clicked on the Enter link, you are not prompted about your age again for another 2 weeks. To bring on the age verification again, you need to manually delete a cookie called isAnAdult. To delete cookies, you can use the following extension in Google Chrome.

 

If customers disable JavaScript
 

If you want to keep out customers that have JavaScript disabled, add the following to the head section of your theme.liquid file in the Edit HTML/CSS page:


<noscript>
<meta http-equiv="refresh" content="1; url=/pages/age-check" />
</noscript>

Replace age-check with the handle of the page you want to redirect to on your website.
