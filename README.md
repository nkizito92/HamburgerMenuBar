# HamburgerMenuBar

Wondering what I did in this video?
[Create A Hamburger Menu Bar With HTML and CSS](https://www.youtube.com/watch?v=lH-78zRNh30&ab_channel=KizitoNjoku)

Well you came to the right place. Here each key factor will be explained.

## What is needed!

The first thing you need is an _html file_. Here you will set up the page with _html, head, and body tag_ like so:

```
    <html>

        <head>

        </head>
        <body>

        </body>

    </html>

```

Once you have this setup now it's time for you to add in some _div_ tags in side the _body_ tags. You will need one _div_ that contains 3 more _div_ just like this:

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

Now that this is set as well, we need to add a class attribute to the parent _div_. Let’s call it buns like so:

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

Alright now lets jump to the design file. So far we only have 2 types of selectors we must make and alter. The _class selector_ for "buns" and the _tag selector_ for the 3 div's inside it. Ok now lets start with the class selector called "buns". We need to add the _elements_ _transition_ of 0.4 seconds, _border_ (with 10 pixels of a solid black line), a width/height with 300 or less pixels, and a _border-radius_ of 20 pixels or less like so:

```
.buns {
  transition: 0.4s;
  width: 300px;
  height: 300px;
  border: 10px solid black;
  border-radius: 20px;
}

```

Next is the 3 div’s within the “buns” but this time replace the height and border with padding and margin. We also need to add a background-color as well so it should be set in these contexts:

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

## Great

If you followed all the instructions this far you should see the burger menu bar on your HTML page.

## Animation Time

Ok, we got the hamburger menu bar fully set. Now it’s time to add some animation. To do this we most add reactions to selectors themselves. We want the first and third div to form a down arrow when the mouse is hovering over the “buns”. How do we make that happen? Well first we need to create another selector (Descendant combinator _.buns div_) and add a psuedo-class called hover like so:

```
.buns:hover div {
}

```

Inside there will be the elements transition of 0.4 seconds and transform to make the first and third div to form a down arrow by coding this:

```
.buns:hover div:nth-child(1) {
  transition: 0.4s;
  transform: translate(-50px, 80px) rotate(45deg);
}

.buns:hover div:nth-child(3) {
  transition: 0.4s;
  transform: translate(50px, -80px) rotate(135deg);
}

```

What is _:nth-child()_ for? Is that another pseudo-class? Why yes it is another pseudo-class. _nth-child_ allows you to select the specific child within the parent in this case I chose the first div and the third div. Ok What does translate and rotate do? In translate, it has to params required, the _x-axis_ and the _y-axis_.
For rotate, you can sort of already guess what it does. It will rotate the first and third child div by 45 degrees and 135 degrees. Now for the 2 child div we are going to make it become invisible. All we need to do is add an _opacity_ of 0 and of course the _transition_.

## Example

```
.buns:hover div:nth-child(2) {
  transition: 0.2s;
  opacity: 0;
}

```

## Almost There!!

Perfect now the last trick we need is to make the _border-raduis_ of the hamburger menu become a full circle when hovering over it. All we need to do is create another .buns class selector, add _hover_, and _transition_ just like this:

```
.buns:hover {
 transition: 0.4s;
 border-radius: 95%;
}
```

# Congratulations

WOW!! you did it pat yourself on the back you deserve it!!

## Extra tricks

To make the menu change color when you click it just make another .buns selector and add the pseudo class _active_
like so:

```
 .buns:active {
  background-color: orange;
}

 .buns:active div {
  background-color: white;
}


```
