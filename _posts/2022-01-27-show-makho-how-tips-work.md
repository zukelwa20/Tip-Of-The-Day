---
layout: default
---

# How to use handlebars...

Handlebars template make it easy to read and display data. 

Handlerbars is templating engine that dynamically generates your HTML page. It’s an extension of Mustache with a few additional features. Mustache is fully logic-less but Handlebars adds minimal logic thanks to the use of some helpers (such as if, with, unless, each and more) that we’ll discuss further in this article. As a matter of fact, we can say that Handlebars is a superset of Mustache.


Create a template inside the header using script tag.
Load the CDN(content delivery network)

```
<script src="https://cdnjs.cloudflare.com/ajax/libs/handlebars.js/4.7.7/handlebars.js" integrity="sha512-c7SfJeKRl8g7wgL+zMGX78faYVGp+NZVQ587mRLrqeLySX/qHCQOKw/iZ5Pp64DaPjvedixWC/Fe73upnhBaRA==" crossorigin="anonymous" referrerpolicy="no-referrer"></script>

```
Create a tamplate script in your html, the template can also be created in separate file or same file. The template is the combination of HTML ``` type="text/x-handebars :"``` and handlebars expression ```{{your variable here}}``` variables are written in double curly braces e.g {{}} and know as expressions. 

```
<script type="text/x-handlebars" class="name-teplate">
   <div>
      My name is {{name}}. I'm a coder  at {{occupation}}.
   </div>
   </script>
   
```

```
Reference the template in js(dom logic).

Get html text using .innerHTHL.
Create the variable of your compiled template.
Inject data into the template. 
Use the keys to display. 
Remember to use the correct keys, that means use the same keys you have used to set data into the compiled template variable. 
Make sure inside of your template you do not have a code that is commented out or you have the correct syntax.

to continue...

```
