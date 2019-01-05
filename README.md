# Guide to create and Compile your first SASS/SCSS file

## Create youe very own scss file.
Before we do that, it's good to note that browsers can't understand scss. In order for your browser to understand the code you write in your scss file, you need to compile it to plain css. Incase you feel that this is extra work, don't worry. You can easily automate it using task runners like [Gulp](https://gulpjs.com/).
For now, since we're learning the basics, it's good to do it the "time consuming way", so that when you actually [automate](https://css-tricks.com/gulp-for-beginners/), you'll
know what's going on under the hood.

Let's start with 
#### Step 1
- Create a folder anywhere on your computer. I'll name it as "*abc*".

#### Step 2
- Create a file and give it any name you'd like. 
- Save the file with a *.scss* extension. Example: *xyz.scss*

#### Step 3
- Copy the below SCSS code and paste it in your *xyz.scss* file. (Don't worry if you don't understand what the code yet)
```
$primary-color: #000;

body{
   color: #fff;

  p {
	  font-color: $primary-color;
  }
}

```

#### Step 4 (Almost there!)
- Open your terminal and [navigate](https://www.dummies.com/computers/macs/mac-operating-systems/how-to-use-basic-unix-commands-to-work-in-terminal-on-your-mac/) to the abc folder that we created in Step 1.

#### Step 5 (Final Step)
- Compiling our xyz.scss file into css. To do that
```
sass xyz.scss:xyz.css
```

Done! You've created and compiled your first scss file. 
Now the only thing left is to link the compiled xyz.css file to your project (i.e adding it to the <head> </head> section of your project)

But hold on, what about the other files that were created?

1- *xyz.css* file (This is the compiled css file)

2- *xyz.css.map*  (This is a source map file. It basically helps shows you the line number of the code when you inspect a style in the browser)

3- *.sass-cache* directory (This folder mostly exists to speed up compilation)

In General you don't need to worry about about them. Just know that they are quite useful when it comes to debugging your code.
