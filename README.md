# Guide to create and Compile your first SASS/SCSS file

## Create your very own scss file.
Before we do that, it's good to note that browsers can't understand scss. In order for your browser to understand the code you write in your scss file, you need to compile it to plain css. In case you feel that this is extra work, don't worry. You can easily automate it using task runners like [Gulp](https://gulpjs.com/).
For now, since we're learning the basics, it's good to do it the "time-consuming way", so that when you actually [automate](https://css-tricks.com/gulp-for-beginners/), you'll
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

In general, you don't need to worry about them. Just know that they are quite useful when it comes to debugging your code.

## --watch flag in sass
Now that you know how to compile a SASS/SCSS file, you should know that we don't need to run the compilation command every time we make changes to our scss file. With the help of the **--watch** flag, we can watch individual files or directories for any changes made to our SCSS files *until we stop the process*.

The watch flag basically tells Sass to watch your source files for changes, and **re-compile CSS each time you save your Sass**. If you wanted to watch your style.scss file, you'd just add the watch flag to your compilation command, like so:
```
sass --watch style.scss:style.css
```
**In a real-world scenario** where you have multiple/separate scss files for different components (eg: header.scss, slider.scss, main.scss, footer.scss) you normally watch the folder that contains these files.
For example, if you have a folder named SASS which contains all your .scss files (eg: theme/sass)
```
sass --watch theme/sass:public/stylesheets
```
Sass would watch all files in the theme/sass folder for changes, and compile CSS to the public/stylesheets folder.
