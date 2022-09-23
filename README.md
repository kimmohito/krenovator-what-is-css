# What Exactly is CSS?

Cascading Style Sheets (CSS) is a markup language responsible for how your web pages will look like. It controls the colors, fonts, and layouts of your website elements.

This style sheet language also allows you to add effects or animations to your website. You can use it to display some CSS animations like click button effects, spinners or loaders, and animated backgrounds.

Without CSS, your website will appear as a plain HTML page. Here’s how example of page [without css](#without-css) and [with css](#with-css) will look like.

## Without CSS
<html>
    <form>
        <h3>Login</h3>
        <label>Username: </label><br>
        <input type="text"><br>
        <label>Password: </label><br>
        <input type="text"><br>
        <button>Login</button><br>
        <a href="#">Forgot password?</a>
    </form>
</html><br>

## With CSS
<html>
    <style type="text/css">
        .form-with-css{
            background: #fff;
            text-align: center;
            padding: 20px;
        }
        .form-with-css .card{
            border: solid 1px #ccc;
            border-radius: 5px;
            margin: auto;
            padding: 20px;
            width: 340px;
        }
        .form-with-css h3{
            margin-bottom: 20px;
        }
        .form-with-css label{
            display: absolute;
            top: 0;
            color: #00acee;
        }
        .form-with-css input{
            background: #eee;
            border: solid 1px #ccc;
            border-radius: 5px;
            display: inline-block;
            margin-bottom: 20px;
            padding: 10px;
            text-align: center;
            transition: ease .4s;
            width: 280px;
        }
        .form-with-css input:hover{
            background: #ccc;
        }
        .form-with-css button{
            background: #00acee;
            border: none;
            border-radius: 5px;
            color: #fff;
            cursor: pointer;
            display: inline-block;
            margin-bottom: 20px;
            padding: 10px;
            transition: ease .4s;
            width: 300px;
        }
        .form-with-css button:hover{
            background: #333;
        }
        .form-with-css a{
            color: #00acee;
        }
    </style>
    <form class="form-with-css">
        <div class="card">
            <h3>Login</h3>
            <input type="text" placeholder="Phone, Email or Username"><br>
            <input type="password" placeholder="Password"><br>
            <button>Login</button><br>
            <a href="#">Forgot password?</a>
        </div>
    </form>
</html><br>

# The Difference Between Inline, External and Internal CSS Styles

There are three ways you can use to implement CSS into your HTML: internal, external, and inline styles. Let’s break them down.

## Internal CSS
Internal or embedded CSS requires you to add `<style>` tag in the `<head>` section of your HTML document.

This CSS style is an effective method of styling a single page. However, using this style for multiple pages is time-consuming as you need to put CSS rules on every page of your website.

Here’s how you can use internal CSS:

1. Open your HTML page and locate `<head>` opening tag.

2. Put the following code right after the `<head>` tag
```
    <style type="text/css">
```

3. Add CSS rules on a new line. Here’s an example:
```
    .body {
        background-color: blue;
    }
    .body h1 {
        color: red;
        padding: 60px;
    }
```

4. Type the closing tag
```
    </style>
```

Your HTML file will look like this:

```
    <!DOCTYPE html>
    <html>
        <head>
        <style>
            body {
            background-color: blue;
        }
        .body h1 {
            color: red;
            padding: 60px;
        } 
        </style>
        </head>
        <body>
            <h1>Krenovator - What is CSS</h1>
            <p>This is our paragraph.</p>
        </body>
    </html>
```

Output:
<html>
    <style type="text/css">
        .body {
        background-color: blue;
    }
    .body h1 {
        color: red;
        padding: 60px;
    } 
    </style>
    <div class="body">
        <h1>Krenovator - What is CSS</h1>
        <p>This is our paragraph.</p>
    </div>
</html>

### Advantages of Internal CSS:
You can use class and ID selectors in this style sheet. Here’s an example:

```
.class {
    property1 : value1; 
    property2 : value2; 
    property3 : value3; 
}

#id {
    property1 : value1; 
    property2 : value2; 
    property3 : value3; 
}
```

Since you’ll only add the code within the same HTML file, you don’t need to upload multiple files.

### Disadvantages of Internal CSS:
Adding the code to the HTML document can increase the page’s size and loading time.

## External CSS
With external CSS, you’ll link your web pages to an external `.css` file, which can be created by any text editor in your device (e.g., `vscode`).

This CSS type is a more efficient method, especially for styling a large website. By editing one `.css` file, you can change your entire site at once.

Follow these steps to use external CSS:

1. Create a new `.css` file with the text editor, and add the style rules. For example:
```
.xleftcol {
   float: left;
   width: 33%;
   background:#809900;
}
.xmiddlecol {
   float: left;
   width: 34%;
   background:#eff2df;
}
```
2. In the `<head>` section of your HTML sheet, add a reference to your external `style.css` file right after `<title>` tag:
```
<link rel="stylesheet" type="text/css" href="style.css" />
```
Don’t forget to change `style.css` with the name of your `.css` file.

Advantages of External CSS:
Since the CSS code is in a separate document, your HTML files will have a cleaner structure and are smaller in size.
You can use the same .css file for multiple pages.
Disadvantages of External CSS:
Your pages may not be rendered correctly until the external CSS is loaded.
Uploading or linking to multiple CSS files can increase your site’s download time.

## Inline CSS
Inline CSS is used to style a specific HTML element. For this CSS style, you’ll only need to add the style attribute to each HTML tag, without using selectors.

This CSS type is not really recommended, as each HTML tag needs to be styled individually. Managing your website may become too hard if you only use inline CSS.

However, inline CSS in HTML can be useful in some situations. For example, in cases where you don’t have access to CSS files or need to apply styles for a single element only.

Let’s take a look at an example. Here, we add an inline CSS to the `<p>` and `<h1>` tag:

```
<!DOCTYPE html>
<html>
<div style="background-color:black;">
    <h1 style="color:white;padding:30px;">Krenovator - What is CSS</h1>
    <p style="color:white;">This is our paragraph.</p>
</div>
</html>
```

### Advantages of Inline CSS:
- You can easily and quickly insert CSS rules to an HTML page. That’s why this method is useful for testing or previewing the changes, and performing quick-fixes to your website.
- You don’t need to create and upload a separate document as in the external style.

### Disadvantages of Inline CSS:
- Adding CSS rules to every HTML element is time-consuming and makes your HTML structure messy.
- Styling multiple elements can affect your page’s size and download time.

## Conclusion
In this tutorial, you’ve learned the difference between the three types of CSS: internal, external, and inline. Here’s the recap:

- **Internal** or embedded ⁠— add `<style>` tag in the `<head>` section of HTML document

- **External** ⁠— link the HTML sheet to a separate `.css` file

- **Inline** ⁠— apply CSS rules for specific elements.

So, which CSS style will you use?