## Frontend Framework

This framework is a frontend framework based on:

* [HTML5 Boilerplate - v4.2.0][1]
* [Bootstrap - v3.0.][2]
* [SCSS][3] principles and splited layout/scss subfiles
* [Hammer][4] Template feature which helps creating html files out of multiple assets via @include rule

---- 

Furthermore and quite more important your own css is based on [SCSS][5].

What does that mean in detail?

* 1 scss file which creates 1 css file (style.scss -\> style.css)
* in there, a common structure gets imported which contains an index,a variables file which gets divided into various subfiles (named after the variables group) again to have a better overview as well as most common elements (subfiles again)

---- 

Last but not least it makes use of the [Hammer's][6] Templating feature which helps creating html files out of multiple assets via the @include rule

What does that mean in detail?

* 1 html file consists out of many @include snippets
* in there all specified include documents get implemented and build a complete html file
* Hammer outputs all compiled files in an specific Build folder

## Use the framework if:

* You want to build a project based on [HTML5 Boilerplate][7] and [Bootstrap][8]
* You want your own css code to make use of scss
* You want to use [Hammer for Mac][9] to make use of easy creation of new html documents

## Installation

**Requires Sass 3.2**


The framework is incredibly easy to get up and running (provided you’re all set for Sass). Simply [download the latest version][10] of the framework from right here on GitHub, unpack the zip file and watch the scss folder.

You can watch the file by `cd`ing into the directory that houses the `.scss`
and running the following:

	 $ sass --watch style.scss:style.min.css --style compressed


Alternatively you can just drag and drop the folder containing the project right into [Codekit for Mac][11] or [Hammer for Mac][12] and the rest gets done automatically...

That’s it, your project is now set up.

Now it is time for you to add your styles into the specific scss splits.

Most common used css groups are added as scss files and indexed already.

## Architecture - SCSS

_styles.scss_

	Styles.scss
 
	The following parts are imported:
	- Index - overview of the css layout
	- Variables - collection of variables which are accessible throughout the project
	- Styles - basically these are the style splits/groups where you write your code
 
_index.scss_
 
	This file contains the index of all the scss subfiles 
	/*------------------------------------*\
	Index - Stylesheet: style.css

	0.  Variables
	1.  Mixins
	2.  Helper Classes
	3.  Global (body, page sructure)
	4.  Header
	5.  Navigation
	6.  Pagination
	7.  Breadcrumb
	8.  Images
	9.  Media
	10. Buttons 
	11. Lists
	12. Forms
	13. Links
	14. Tables
	---
	15. Selectors
 

	\*------------------------------------\*/
 
_variables.scss_

	/*------------------------------------*\
	Include.scss
	\*------------------------------------\*/

	/\*\*
	 \* Generic helper classes and project mixins.
	\*\*/

	@import "generic/mixins"; 
	@import "generic/helper";
  
	/\*\*
	 \* Includes all the various parts
	\*\*/
 
	@import "parts/global";
	@import "parts/header";
	@import "parts/navigation";
	@import "parts/pagination"; 
	@import "parts/breadcrumb";
	@import "parts/images";
	@import "parts/media";
	@import "parts/buttons";
	@import "parts/lists";
	@import "parts/forms";
	@import "parts/links";
	@import "parts/tables";


## Architecture - HTML

_index.html_
 
	Logically imports all specific html parts into the document at its respective place

_The following files are being imported:_

	<!-- @include "include/_pre_header.html" -->
	<!-- @include "include/_header_css.html" -->
	<!-- @include "include/_header_js.html" -->
	<!-- @include "include/_header_msc.html" -->
	<!-- @include "include/_body_begin.html" -->
	<!-- @include "include/_nav.html" -->
	<!-- @include "include/_footer.html" -->
	<!-- @include "include/_body_end.html" -->
 
Each of them contains content which should be the same on each file/page you create so that you can just rename the index.kit to the page you want to create...

---- 

##### Currently the files are filled with boilerplate best practice code based on the provided index.html file which comes with the standard installation of boilerplate

---- 

## Credits

Due to the fact the framework is based on Bootstrap and Boilerplate the Credits goes the the creators:

* [HTML5 Boilerplate - v4.2.0][13]
* [Bootstrap - v3.0][14]

And probably more…

[1]:	http://html5boilerplate.com/
[2]: http://getbootstrap.com/
[3]:	http://sass-lang.com/
[4]:	http://hammerformac.com/
[5]:	http://sass-lang.com/
[6]:	http://hammerformac.com/
[7]:	http://html5boilerplate.com/
[8]:	http://getbootstrap.com/
[9]:	http://hammerformac.com/
[10]:	https://github.com/Tischers/Frontend_Framework/archive/Main.zip
[11]:	http://incident57.com/codekit/
[12]:	http://hammerformac.com/
[13]:	http://html5boilerplate.com/
[14]:	http://getbootstrap.com/
