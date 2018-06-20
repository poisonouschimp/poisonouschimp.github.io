---
layout: post
title:  "My first post"
date:   2018-06-20 11:47:22 +0000
categories: jekyll update
---
<p>
"I want to link my code notes here <a href="poisonouschimp.github.io/code_notes.txt">This is my link</a>

If the link doesn't work here are my notes:
<p>All HTML elements created using tags-https://developer.mozilla.org/en-US/docs/Web/HTML/Element
Global Attributes-https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes

<body> --opens display content
<p>Hello World!</p>
<p> opening tag "p for block of plain text paragraph"
Hello World! content
</p> closing tag
</body> --closes display content
<h1></h1> - opens and closes heading tags, goes to h6
<div></div> - "division" or container that divides the page into sections. Groups elements in HTML together. Add 2 spaces for subelements for ease of reading.
Attributes:
id - specify different content such as <div>s and helpful when using an element more than once.
<p> long block of text in chunks
<span> short piece of text separate inline
<em> - emphasizes text style "italics"
<strong> - highlights important text "bold"
<br> - line break, only starting tag no closing tag
<ul> - unordered list shell, bullet points (list item tag) made by <li></li>
<ol> - ordered list, numbered to give process or rank to items, still use <li></li> for the items.
<img> - adds images and is self closing tag
src - attribute that selects image source, URL location
<img scr="image-location.jpg" />
alt - attribute adds text description of picture, also helps SEO site ranking because web crawlers see it.
<img src="file location" alt="text description" />
<video src="myVideo.mp4" width="320" height="240" controls>
  Video not supported - only displays if video not supported by their browser
</video> - video requires opening and closing tag

HTML site standards:
<!DOCTYPE html> - must be first line of code in html document and tells which version of html to use to read the code. Save files in .html
<html></html> adds structure and content and is interpreted as html code
<head></head> adds meta data to page above body tags
<title></title> - gives tabs their info and is inside the head
<a> - anchor element that links to a web page
<a href="https://www.link.com/">This is a link to link.com</a>
href- hyperlink reference used to path to other webpages.
target="_blank" - lets the link open a new window or tab, add after the URL in the <a> tag
local files use relative path of ./index.html vs absolute path of https://..... and ./ tells browser to look in the current folder
You can wrap any element in anchor tags<a></a> to make them link
<p id="top">targets top of page</p>
<h1 id="bottom">targets bottom of page</h1>
The target link to is written as
<ol>
  <li><a href="#top">Top</a></li>
  <li><a href="#bottom">Bottom</a></li>
</ol>
Add comments to code <!-- This will not display. -->
<table>
  <thead>Encloses table head</thead>
  <tbody>
    <tr>
      <th></th> adds blank table header row that       aligns the table headings correctly over the       data they correspond to.
      <th scope="col">Column name</th>
      <th scope="row">Row name</th>
        <td>xxx</td> adds table data
        <td colspan="2">Makes column span 2         across</td>
        <td rowspan="2">Makes row span 2 down</td>
    </tr> adds table row
  </tbody> contains all table data excluding table   headings
  <tfoot>Encloses table footer</tfoot>
</table> creates table element
CSS gives customization to HTML
font-size: 18px; in CSS under th, td { } changes all text to 18pixles

CSS - Cascading Style Sheets, language web developers use to style HTML content on a web page. Colors, font type, font size, shadows, images, element positioning
<link href="style.css" type="text/css" rel="stylesheet"> - links the .css document to the html document
You can add CSS inline in HTMl rather than a .css file by <p style="color: red; font-size: 20px;">Text!</p>
Inline requires doing it for every h1 element, but you can write CSS in its own section
<head>
  <style>
    p {
      color: red;
      font-size: 20px;
    }
  </style>
</head>

p {
} The CSS syntax selects the <p></p> element in HTML
.class is the CSS syntax to select HTML class elements in the tag
.green {
  color: green;
}
.bold {
  font-weight: bold;
}
<h1 class="green bold">...</h1> will make the CSS rules apply to the HTML h1 to make it green and bold. So you don't have to write custom rules for each h1.
id="element name" HTML id name
#element name { CSS selector for HTML element
} ID's override elements so they always appear the same
CSS can select HTML elements by tag, class, ID
CSS classes are reused by many elements
CSS IDs style only one element and override styles of tags and classes.
CSS tags are least specific, then classes, then IDs most specific.
!important overrides all other rules and forces all  elements to follow that rule.
font-family: sets font typeface times new roman is the defualt for all html elements. When typeface is more than one word put it in ""
font-size: set font size
font-weight: sets bold, or normal to disable certain elements that are not to be bold
text-align: left right center of the parent element
color: styles foreground color
background-color: styles background color
opacity: from 0.0 - 1.0 from fully invisible to fully visable.
background-image: url("..."); sets element's background to display an image
height width- of content area, default are set to hold raw contents of the box. Pixles allow the exact size to display on all devices, overflow mobile screen.
padding- space between content area and border. can do padding-top, right, bottom, left. Can do one line to specify all 4 by padding: 6px 11px 4px 9px; that goes from top, right, bottom, left in a clockwise rotation. If the top and bottom and left and right equal each other you can use the shortcut padding: 5px 10px; to say top and bottom 5px, left and right 10px.
border- thickness and style of border surrounding content area and padding. width is the thickness of border either in px or (thin, medium, thick). Style is the design of border (none, dotted, solid, 7 others). Color of the border with 140 built in keywords. Default border is medium none color
border-radius: makes it so borders aren't a square box. px is radius of circle for the corners or you can make it a circle by setting to 100% or same height of box.
margin- space between border and outside edge of element "outside edge of box". keeps a zone around the element so no other items can be displayed in the zone. Can also use margin-top/bottom/right/left. Can use margin: 1px 2px 3px 4px; to specify each corner from top, right, bottom, left. Can use margin: 1px 2px; to specify top and bottom, left and right together. Also lets you center the content by margin: 0 auto;with top and bottom being 0px zone and left and right automatically centers it in the containing element. Must have a specified width smaller than the screen width to have it automatically center, default is full page. Top and bottom margins collapse (non-additive, the larger margin sets the spacing). Left and right margins are additive, so 10px + 20px of adjecent margins would be 30px effective spacing.
min-width and max-width: ensures max or min width of element box, helpful for displaying on any device. Also min-height and max-height. If max height is set too low content spills outside contetnt box and becomes illegable.
overflow- when text flows outside element, tells what to do. Hidden- hides from view, scroll- can view rest of content by scrolling, visable- display outside containing element and is default setting. Element is the sum of all margins/padding/border/content and if larger than parent area will overflow.
https://s3.amazonaws.com/codecademy-content/courses/freelance-1/unit-4/diagram-boxmodel.svg
* {
  margin: 0;
  padding: 0;
} typically first rule in external CSS style sheet to override user browser defined default CSS rules.
Visibility- hides or shows elements from view. hidden hides and visible displays and element. display: none completly hides from webpage whereas hidden will leave empty space where element is intended to display.
default font-weight is - normal
default box model is box-sizing: content-box;
content-box: width + padding + border = actual rendered widith of an element's box
Border-box- contains all elements rather than having external elements. Content is automatically sized based off remaning usable size after subtracting padding/margins/borders
* {
  box-sizing: border-box;
} sets all boxes to be border-box
position- default value is static and does not need to be specified. Relative to static position using top/bottom/left/right: 2px offset properties, absolute makes all elements on the page ignore the element and act like it is not present on the page. The element will be positioned to the closest positioned parent element (top left corner)., fixed locks the element to a static location on the screen while scrolling and useful for navigation bars.
display- inline (default display for some tags like <em><strong><a> are inline. Inline has a box that wraps tightly around their content and only uses space necessary to display their content. The height and width cannot be specified in CSS. display: inline; allows any element to display inline that are not as default like paragraphs/divs/headings), block(fill whole width of page, but can specify the width. Default block-level are all level of heading elements <h1>-<h6>/<div>/<footer>), inline-block(elements can appear next to each other and can specify their height and width. Images are the best example of default inline-block elements.
z-index- controls depth of elements, deeper elements appearing behind shallower elements. Uses numbers to rank their order. A relative z-index of 2 will overlay an absolute position since it is a static "0". So for locked header bars use position:fixed, width:100%, z-index:10 or higher number so it doesn't get out ranked.
float- aligns element as far left or right as possible. float: left/right; must have specified width or element will assume full width of its containing element. Different height element floated at same time can cause bumping to happen and not properly move to the left or right.
clear- specifies how elements should behave when they bump into each other on the page. Can be left/right/both/neither. Meaning left/right side will not tough any other element within the same element, both makes neither side of element touch any other element within the same containing element. None makes it so the element can tough either side.
Hexidecimal color code- uses 0-15 so 16 digits and past 0-9 A-F represents 10-15. Black is #000 and white is #FFF. Hex (6) is 6 digets in total, when adjacent pairs are the same you only need 3 digits to display the color, but could use all 6. You cant take 6 and make 3 if they are not the same though. Aqua is #00FFFF, but also #0FF because 00/FF/FF = 0/F/F.
RGB colors: color:(23, 45, 23); from a 0-255 of amount of red/green/blue to add.
HSL: Hue-Saturation-Light color scheme.
color: hsl(120, 60%, 70%); the first number is the degree of hue from 0-360 on the color wheel. Red is 0* or 360*/Green 120*/Blue 240*, 2nd and 3rd numbers are % representing saturation(percent purity of the color from 0% grey in the middle of the wheel to 100% at the edge of the circle for pure color) and lightness(starts at 50%, 100% is pure white and 0% is pure dark).
HSLA- same as HSL, but A is Alpha/opacity and is a decimial from 0-1 where 0 is transparent and 1 is solid opaque. RGBa is the same.
zero opacity is called : transparent; and is equivalent to rgba(0,0,0,0)
font-family: "courier new"; changes from default times new roman to courier new.
font-weight: bold/normal; can be assigned a numeric value ranging from 100-900, valid values are multiples of 100 within the range such as 200 or 500. 400 is the default font-weight of most text, 700 is a bold font-weight and 300 is a light font-weight. Not all fonts can be assigned a font weight and you can look up which values are available.
font-style: italic; default is normal.
word-spacing: 0.25em is the default. Helps with bolded or all caps.
letter-spacing: known as kerning. Helps with reading uppercase text.
text-transform: uppercase/lowercase; forces all text to upper or lowercase
text-align: right/center/left;
line-height: modifies the leading of text"space between font and line height". Can be made by a unitless number that computes the line height as a ratio of the font size. A specified by unit such as 12px/%/ems/rems. Unitless is prefered as it automatically adjusts to new fonts.
Serif- fonts that have extra details on the ends of the letters(times new roman/georgia/others). Better for print and are easier to read in long paragraphs of text.
Sans-Serif- fonts that do not have extra details on the ends of each letter and they have straight flat edges (Arial/Helvetica). Easier to read on computer that have lower resolution than print.
Fallback fonts: if cannot dispaly one font use known font computer has
h1 {
  font-family: "Garamond", "Times",
serif;
} says"use garamond, but times if not available, if not then use any serif font pre-installed on the user's computer.
To link fonts from fonts.google.com use
<head>
  <link href="https://fonts.googleapis.com/css?family=Droid+Serif:400,700,700i|Playfair+Display:400,700,900i" rel="stylesheet">
</head>
Rather than link you can import directly into style sheet by using @font-face. You paste the google link into browser then copy the /* latin */ rules to the top of style.css
Add fonts from local directory by
@font-face {
  font-family: "Roboto";
  src: url(fonts/Roboto.woff2) format('woff2'),
       url(fonts/Roboto.woff) format('woff'),
       url(fonts/Roboto.tff) format('truetype');
}

grid-template-columns
grid-template-rows
grid-template
grid-template-area
grid-gap
grid-row-start
grid-row-end
grid-column-start/end
grid-area
To set up a grid you need both grid container and grid items. Grid container is the parent that contains the grid items as children and applies styling and positioning to them.
To turn HTML element into grid container you set the element's display property to grid (block level grid) or inline-grid(for inline grid). Then you assign other properties to layout the grid.
.grid {
  display: grid;
  width: 500px;
  grid-template-columns: 100px 200px;
}sets 2 columns 1st being 100px wide and 2nd being 200px wide. Or can set as % of grid width. Or even mix and match px and %.
grid-template-rows: sets row height and same as columns for sizing.
grid-template: replaces grid-template-rows/columns by grid-template: 200px 300px / 20% 10% 70%; Where row size / column size
fr- is CSS unit for fraction and prevents overflowing boudaries of the grid. can mix and match numbers too.
grid-template: repeat(3, 100px); says add 3 columns/rows at 100px, same as writing 100px 100px 100px. Can also do different sized repeats as repeat(2, 20px 50px); will make 4 columns where it will be 20px50px20px50px
minmax(100px, 500px) 100px; says 1st and 3rd column will always be 100px, but 2nd column will move between 100-500px depending on browser size. Also must have variable grid size, so no width: 500px;.
grid-row/column-gap: puts blank space between every row and column in the grid.
grid-gap sets row and column gap at the same time. grid-gap: 20px 10px; sets the distance between rows to 20 and columns to 10px. If only one value is given it will set both column and row gap to that value.
Grid-row/column-start/end: is child level grids to define how many of each row and column they are to take up. If a grid has 5 rows, the grid row lines range from 1-6. If a grid has 8 columns, the grid row lines range from 1-9. Grid-row-end should be 1 greater than the row end. So an element that covers 2,3,4 would be grid-row-start:2, grid-row-end:5
grid-row is the shorthand for grid-row-start/end with grid-row: 4 / 6; would span rows 4 and 5. When it spans multiple rows it also includes the grid-gap and thus the height is the sum of spanned grids plus gaps. Can also write as grid-column: 4 / span 2; which is same as grid-column: 4 / 6; where it exists in 4th and 5th column.
grid-area: combines grid-row-start, grid-column-start, grid-row-end, grid-column-end in that order like grid-area: 2 / 3 / 4 / span 5;

grid-template-areas
justify-items
justify-content
justify-self
align-items
align-content
align-self
grid-auto-rows
grid-auto-columns
grid-auto-flow

grid-template-areas: allow the naming of sections of the webpage to use as values in grid-row/col-start/end and grid-area.

.container {
  display: grid; - makes HTML into CSS grid command
  max-width 900px; - max resize for browser
  position: relative - makes respect to a point
  margin: auto;
  grid-template-areas: "head head"
		       "nav nav"
                       "info services"
                       "footer footer";
grid-template-rows: 300px 120px 800px 120px;
  grid-template-columns: 1fr 3fr;
}

header {
  grid-area: head;
}

nav {
  grid-area: nav;
}

.info {
  grid-area: info;
}

.services {
  grid-area: services;
}

footer {
  grid-area: footer;
}

justify-items: start/end/center/stretch; positions grid items along the inline(row/axis) from left to right across the webpage. Stretch fills the items to grid area.
justify-content: start/end/center/stretch/space-around/space-between/space-evenly; position the entire grid along the row axis. Center- centers the grid horizontally in the grid container. Stretch- stretches the grid items to increase the size of the grid to expand horizontally across the container. Space-around- includes an equal amount of space on each side of a grid element, resulting in double the amount of space between elements as there is before the first and after the last element. Space-between- includes an equal amount of space between grid items and no space at either end. Space-evenly- places an even amount of space between grid items and at either end.
align-items: start/end/center/stretch: aligns grid items "positions them" from top to bottom.
align-content: start/end/center/stretch/space-around/space-between/space-evenly. Positions the rows along the column axis or from top to bottom.
justify-self: specifies how an individual element should position itself wrt row axis, will override justify-items for any that are declared.
align-self: specifies how an individual element should position itself wrt column axis and will override align-items for any that are declared. They both accept the start/end/center/stretch commands.
grid-auto-rows: specifies the height of implicitly added grid rows.
grid-auto-columns: specifies the width of implicitly added grid columns.
grid-auto-rows/columns accept the same values as their explicit counterparts (grid-template-rows/columns). pixles (px), percentages(%), fractions(fr), repeat().
grid-auto-flow: specifies whether new elements are added to rows or columns and accepts row/column/dense.
row-specifies the new elements should fill rows from left to right and create new rows when there are too many elements (default setting).
column- specifies the new elements should fill columns from top to bottom and create new columns when there are too many elements.
dense- attempts to fill holes earlier in the grid layout if smaller elements are added. row and column can be paired with dense like
grid-auto-flow: row dense;

Adding an image: <img src="">
Adding a video:
<video width="320" height="240" controls>
  <source src="video-url.mp4" type="video/mp4">
</video>
Where width and height sets the size of the screen that displays the video, controls adds the play/pause/volume control/source src sets the URL of the video to play/type specifies different video formats.
<div class="container">
...
</div> - Div's enclose chunks of code as a "container" that can have CSS rules applied to it as well as move around the code easier.

Page Meta Data: Brains of the webpage
<!DOCTYPE html>: Tells web page to expect HTML doc
<html>...</html>: root parent of HTML document and of all HTML elements on the webpage.
<title>...</title>: Contains site title and one way users can find the site through a search engine like GOOGLE
<meta charset="utf-8"/>: tells the web browser which character set to use, in this case the character set is utf-8.

CSS link file: <link rel="stylesheet" type="text/css" href="main.css"/>
Where -rel= specifies the relationship between the current file and the file being linked to, in this case rel is to stylesheet
-type= specifies the type of file linked to
-href= provides the URL of the file being linked to.

Rems: Ensure HTML elements scale in porportion to each other on various web browsers and screen sizes. On most browsers 1rem=16px, 2rem=32px, 3rem=48px.
em: a relative value that changes in porportion to the size of the parent element. If parent element has font-size: 20px, child element of font-size: 1em would be 20px, but child element of font-size:.5em would be 10px.

float
display: flex
flex-wrap: wrap
a:active, :active- is a psuedo-class selector which only styles an element when it is being clicked.
top: 2px; will simulate a button being clicked.

Bootstrap: a popular CSS framework with prewritten CSS rules designed to help build webpages faster.
in HTML header: used to organize headers on a webpage
Footer: used to organize footers on a webpage.
Section: Defines sections on a webpage
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/css/bootstrap.min.css"/>
Bootstrap classes
row: Arranges HTML elements in rows, and can be useful when building headers/navigation menus, main feature sections, supporting content sections and footers.

jumbotron: Used to create large showcase sections featuring important content.

col-sm-*: Used to span a specified number of columns on the Bootstrap grid. The "sm" is short for "small", and maintains desired CSS layouts on small screens (tablet-sized).

text-right: Bootstrap class used to orient text to the right side of the webpage.

btn btn-primary: Bootstrap class used to style page elements as buttons.

Terminal command line:
https://www.codecademy.com/articles/command-line-commands
To access the command line use terminal emulator.
$- shell prompt and appears when terminal is ready to accept a command.
Ls (ls)- lists the files and folders inside the file you are in. Folders are called directories, files and directories on the computer are organized into a file system.
File system- organizes the computer files and directories into a tree structure. The first directory in the file system is the root directory, the parent to all other directories and files in the filesystem. Each parent directory can contain more child directories and files.
pwd- print working directory. Outputs the name of the directory currently working in "the working directory." For CodeAcadmey the working directory is home/ccuser/workspace/
Using ls and pwd shows where you are in the filesystem.
cd- change directory, selects one of the dispalyed file directories to make it the current working directory.
arguement- when a file/directory/program is written as a command it is called an arguement. In the example the 2015 directory is an arguement for the cd command. The cd command takes a directory name as an arguement and switches into that directory.
To navigate directory to a directory use cd with the directory's path as an arguement "$ cd jan/memory" to move up a directory use "$ cd .." which moves from jan/memory up to jan/
$ mkdir media- mkdir stands for make directory, takes directory name as arguement and creates a new directory in the current working directory.
touch- creates a new file inside the working directory. It takes the file name as an arguement and creates an empty file in the current working directory.
ls -a: ls lists all files and directories in the working directory, the -a modifies the behavior to also list the files and directories starting with a dot(.), files starting with a dot are hidden and don't appear when using ls alone. -a is called an option and options modify the behavior of commands.
ls options:
ls -a= lists all content, including hidden files and directories
ls -l= lists all contents of a directory in long format with 7 columns of info.
-1. Access Rights- actions that are permitted on a file or directory
-2. Number of hard links- counts the number of child directories and files. This includes the parent directory link (..) and current directory link(.).
-3. The username of the file's owner.
-4. The name of the group that owns the file.
-5. The size of the file in bytes
-6. The date & time the file was last modified.
-7. The name of the file or directory.
ls -t= order files and directories by the time they were last modified.
ls -alt= lists all contents, including hidden files and directories, in long format, ordered by the date and time they were last modified.
cp frida.txt lincoln.txt - copies files or directories, we copy the contents of frida.txt into lincoln.txt. Use cp with the source file as the first arguement and the destination directory as the second arguement. Copy from place into.
Wildcards- cp * satire/ will select groups of files. The * selects all files in the working directory, so * satire/ copies all files in the satire directory. cp m*.txt scifi/ will select all files in the working directory starting with m and ending in .txt and copies them into scifi/
mv - command moves files from the first arguement and the destination directory as the second argument. To rename a file use mv with the first arguement and the new file name as the second arguement, by moving the 1st into the second it renames the first.
rm - command removes "deletes" files and directories. rm waterboy.txt removes the file from the filesystem.
rm -r: is an option that modifies behavior of the rm command "-r" stands for recursive and removes all the directory and all of its child directories. When you use rm to remove a file it is a perm delete, no recovery.
stdin- standard input, info inputted into the terminal through the keyboard or input device
stdout- standard output, info outputted after a process is run
stderr- standard error, an error message outputted by a failed process.
Redirection- reroutes standard input, standard output, and standard error to or from a different location.
> - command redirects the standard output to a file.
cat - command outputs the contents of a file to the terminal. cat hello.txt, the contents of hello.txt are displayed. cat oceans.txt > continents.txt will take the data from oceans.txt and overrite the data in continents.txt
>> - command appends "adds" it to the file on the right
< - takes the standard input from the file on the right and inputs it into the program on the left.
| - is a "pipe", takes standard output of the command on the left and pipes it as standard input to the command on the right "command to command redirection". $ cat volcanoes.txt | wc | cat > islands.txt says take the volcanoes file -> input it to word count wc command -> take the word count and redirect the output of cat to islands.txt
wc - outputs number of lines, words, characters in order.
sort- takes input and orders it alphabetically for standard output.
uniq- "unique" filters out adjacent and duplicate lines in a file. $ sort deserts.txt| uniq > uniq-deserts.txt will sort the names in deserts.txt alphbetically, then send to uniq to filter out adjacent entries, finally outputs the results to uniq-deserts.txt
grep- "global regular expression print" searches files for lines that match a pattern and returns the results. It is case sensitive, in grep Mount mountains.txt grep is searching for case sensitive words with Mount in it and displaying it.
grep -i- makes the grep command non-case sensitive
grep -R- searches all files in a directory and outputs filenames and lines containing matched results. -R "recursive" will search the directory for the string Arctic and outputs the filenames and lines with matched results.
grep -Rl- searches all files in a directory and outputs only file names with matched results
sed- "stream editor" accepts standard input and modifies it based on an expression before displaying it as output data, similar to "find and replace".
sed s- substitution
sed 's/snow/rain/'- searches for snow and the replacement string "rain" is the text to add in place.
/g - means global, sed searches forests.txt for the word snow and replaces it with rain globally, all instances of snow on the line will be turned to rain.
nano- command line text editor. nano hello.txt opens a new txt file named hello.txt in the nano text editor ^ stands for ctrl key. ctrl+O stands for output, ctrl+X exits the nano program, ctrl+g opens the help menu, clear clears the terminal
~/.bash_profile is the name of the file used to store environment settings "the bash profile" when session starts it will load the contents of the bash profile before executing commands
~ - user's home directory
. - hidden file
nano ~/.bash_profile opens up ~/.bash_profile in nano
echo "Welcome, Jane Doe" creates a greeting in the bash profile which is saved, it tells the command line to echo the string "Welcome, Jane Doe" when a terminal session begins.
source ~/.bash_profile activates the changes in the ~/.bash_profile for the current session, rather than having to close and reopen for a new session.
alias pd="pwd" alias command creates keyboard shortcuts "aliases" for common commands. Everytime you enter the alias it will be the same output as the regular command.
alias hy="history" will output a history of commands entered in the current session
alias ll="ls -la" the command line now outputs all contents and directories in long format, including all hidden files
export USER"Jane Doe" environment variables that can be used across commands and programs and hold info about the environment.
USER="Jane Doe" sets the envt varb USER to Jane Doe
export- makes the variable available to all child sessions initiated from the session you are in. A way to make the variable persist across programs.
echo $USER returns the value of the variable. $ is always used when returning a variables value. echo $USER returns the name set for the variable.
export PS1=">> " PS1 is a variable that defines the makeup and style of the command prompt. sets the command prompt variable and exports the variable, we change the default prompt of $ to >>
echo $HOME- environment variable that displays the path of the home directory. By typing echo $HOME the terminal displays the path /home/ccuser/ as output
echo $PATH- stores a list of directories separated by a colon.
/bin/pwd - prints the working directory
/bin/ls lists files in the working directory
env- environment command returns a list of the envt varb for the current user
env | grep PATH is a command that displays the value of a single environment variable. The standard output of env is piped to grep command. grep then searches for the value of the variable PATH and outputs it to the terminal.

Git - software that allows you to keep track of changes made to a project over time. Git works by recording changes made to the project, storing those changes, then allowing you to reference them as needed.
git init- initializes the Git environment to begin tracking changes made to the project.
Git project has 3 parts:
1. A Working Directory- where you do all the work, creating, editing, deleting, organizing the files
2. A Staging Area- where you list changes you make to the working directory
3. A Repository- where Git permanently stores those changes as different versionf of the project.
Git workflow consists of editing files in the working directory, adding files to the staging area, saving changes to a Git repository. In Git we save those changes with a commit.
git status- checks the status of the project. Untracked files are those that Git sees, but has not started tracking changes yet.
git add filename - adds a file to the staging area, filename refers to the name of file you are editing.
git diff filename- check differences between the working directory and the staging area.
git commit -m "Complete first line of dialogue" - Standard conventions for commit message: must be in quotation marks, written in present tense, brief < 50 characters.
git log- shows a 40 character SHA unique commit code, the commit author, date and time of the commit, the commit message.
In Git the current commit you are on is called the HEAD commit. Shows everything the git log command displays for the HEAD commit plus all the file changes that were committed.
get checkout HEAD filename- restores the file in the working directory to look exactly as it did when you last made a commit.
git add filename_1 filename_2 - adds 2 files in one command
git reset HEAD filename- resets the staging area to be the same as the HEAD commit. Does not discard file changes from the working directory, just removes them from the staging area.
git reset commit_SHA- uses the first 7 char of the SHA of a previous commit, so git reset *******.
git branch- allows you to split the history, command answers which branch am I on.
git branch new_branch- creates a new branch, new_branch is what you want to name the branch.
git checkout branch_name- switches to new branch
git merge branch_name- will merge the current branch to the master
git branch -d branch_name- will delete the branch from the Git project.
git clone remote_location clone_name- clones so you have your own copy of the branch
remote_location- tells Git where to go to find the remote. Can be a web address or a filepath.
clone_name- is the name you give to the directory in which Git will clone the repository. Git gives remote a name origin automatically so you can refer to it easier.
git remote -v- list of Git project's remotes.
git fetch- brings changes onto a remote branch
git merge origin/master-
For Git collaborations the typical flow is:
1. Fetch and merge changes from the remote
2. Create a branch to work on a new project feature
3. Develop the feature on your branch and commit your work
4. Fetch and merge from the remote again (in case new commits were made while you were working)
5. Push your branch up to the remote for review
Steps 1 and 4 are a safeguard against merge conflicts and step 5 is a git push
git push origin your_branch_name-pushes your branch up to the remote, origin. From there it can be reviewed and merge the work with the master branch making it part of the definitive project version.

Deploying a Website - Jekyll
Jekyll- simple static site generator. Very common way of generating a ready to publish website within seconds.
gem install jekyll- installs the jekyll gem
jekyll new directory_name- fills it with jekyll content
jekyll serve- view your site locally, starts local server that will server the files to your computer. By default, the address for the local server that Jekyll's serve command starts is http://localhost:4000/.
Jekyll's defaults:
1. _config.yml- config file that contains values needed to be edited only once. The values used across your site (site title, email, etc)
2. _includes/- directory contains all the partials (code templates that keep you from repeating your code over and over) that your site uses to load common components like the header and footer.
3. _posts/- directory where blog posts are stored. New blog posts can be added and will be rendered with the site's styling, as long as the file name follows Jekyll's standard naming convention.
4. _layouts/- directory contains templates that are used to style certain types of posts within the site. Ex: new blog posts will use the HTML layout defied in post.html
Website in /home/ccuser/workspace/daw/personal-website
Created the required GitHub repo
Used Git to add, commit, and push your website to the repo
Succesfully used GitHub Pages to deploy your site to the Internet!"
</p>
