    ---
    layout: default
    ---

### Handlebars set-up in express

Install Handlebars 

``` $ npm install express-handlebars ```

Handlebars set-up On app.js or index.js

``` 
import { engine } from 'express-handlebars';

const app = express();

app.engine('handlebars', engine());
app.set('view engine', 'handlebars');
app.set('views', './views');

app.get('/', (req, res) => {
    res.render('home');
});

app.listen(3000);

```
Now create the ``` main ``` layout to wrap up the HTML page which can be reused for the differrent views of your app. 
{{{body}}} is used as a placeholder for where the main content should be rendered. 
 
 ```
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <title>Example App</title>
</head>
<body>

    {{{body}}}

</body>
</html>

```

