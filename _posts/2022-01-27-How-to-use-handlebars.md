---
layout: default
---

### How to use handlebars...

Handlerbars is templating engine that dynamically generates your HTML page. It’s an extension of Mustache with a few additional features. Mustache is fully logic-less but Handlebars adds minimal logic thanks to the use of some helpers (such as if, with, unless, each and more) that we’ll discuss further in this article. As a matter of fact, we can say that Handlebars is a superset of Mustache.


Create a template inside the header using script tag.
Load the CDN(content delivery network)

```
<script src="https://cdnjs.cloudflare.com/ajax/libs/handlebars.js/4.7.7/handlebars.js" integrity="sha512-c7SfJeKRl8g7wgL+zMGX78faYVGp+NZVQ587mRLrqeLySX/qHCQOKw/iZ5Pp64DaPjvedixWC/Fe73upnhBaRA==" crossorigin="anonymous" referrerpolicy="no-referrer"></script>
```
Create a tamplate script in your html, the template can also be created in separate file or same file. The template is the combination of HTML ``` type="text/x-handebars :"``` and handlebars expression ```{{your variable here}}``` variables are written in double curly braces e.g({{}}) and know as expressions. 
```
<script type="text/x-handlebars" class="name-teplate">
   <div>
      My name is {{name}}. I'm a coder  at {{occupation}}.
   </div> 
</script>
```

The next step is to write the necessary JavaScript, This will  contain references to the tamplate along the context object which is the source of the data being passed to the template. The data passed can be either a js literal object or a jQuery object. 
 
 ```const element = document.querySelect('<classname>'); ```

 Next is to pass the HTML to the Handlebars.compile() function. Then, the you pass the data context to the template. And finally, you add the compiled HTML to the DOM. Here is a shot of these steps written out in JavaScript:

 ``` var compiledTemp = Handlerbars.compile(element.innerHTML); ```

Now inject data into the compiled template. 
```
compiledTemp({
    name : 'Akho',
}); 
``` 
use .innerHTML to send the data to html. 
``` element.innerHTML = <YOUR template with data> ``` 
