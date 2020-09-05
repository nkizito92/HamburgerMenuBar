# HamburgerMenuBar

Wondering what I did in this video?
[Create A Hamburger Menu Bar With HTML and CSS](https://www.youtube.com/watch?v=lH-78zRNh30&ab_channel=KizitoNjoku)

Well you came to the right place. Here each key factor will be explained.

## What is needed!

The first thing you need is an _html file_. Here you will setup the page with _html, head, and body tag_ like so:

```
    <html>

        <head>

        </head>
        <body>

        </body>

    </html>

```

Once you have this setup now it's time for you to add in some _div_ tags in side the _body_ tag. You will need one _div_ that contains 3 more _div_ just like this:

```
<body>
    <div>
        <div></div>
        <div></div>
        <div></div>
    </div>
</body>

```

##Awesome

Now that this is set as well we need to add a class attribute to the parent _div_. Let's call it buns like so:

```
    <div class="buns">
        ...
    </div>

```

Kind of like a hamburger, first there's buns and inside lies 3 toppings.

## CSS Style

Cool now it's time to design this Menu bar by giving it a shape and giving it life.
Before we can jump to designing this delicious burger we need toaster to toast the buns and a frying pan to cook the toppings. What type of tag and file do we need? We need a _link_ tag that lives within the _head_ tag and a _CSS_ file called design. What is the link tag for and why does it live within the head tag? Well if you think of it in human terms when someone ask you for the location to a place, you're are going to think in your _head_ the best way direct someone to that specific place. In this case the css file is the place and the link tag is directing you through the _href_ attribute. It should look like this

### Example

```

      <html>

        <head>
         <link rel="stylesheet href="design.css">
        </head>
        <body>
            ...
            ...
        </body>

    </html>

```

Alright now lets jump to the design file. So far we only have 2 types of selectors we must alter. The _class selector_ for "buns" and the _tag selector_ for the 3 div's inside it. Ok now lets start with the class selector called "buns". We need to add a transition of 0.4s, border, a width/height with 300 or less pixels, and border-radius like so:

```
.buns {
  transition: 0.4s;
  width: 300px;
  height: 300px;
  border: 10px solid black;
  border-radius: 20px;
}

```

Next is the 3 div's with in the "buns" but this time replace the height and border with padding and margin. We also need to add a background-color as well so it should be set in this contexts:

```
.buns div {
  transition: 0.4s;
  width: 30px;
  padding: 10px 60px;
  background: black;
  border-radius: 20px;
  margin: 60px auto;
  
}

```
