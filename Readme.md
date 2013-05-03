## Frontend Framework

This framework is a frontend framework based on:

* [HTML5 Boilerplate - v4.0.3](http://html5boilerplate.com)
* [Bootstrap - v2.2.2](http://twitter.github.com/bootstrap)
* [SCSS](http://sass-lang.com) principles and splited layout/scss subfiles
* [Codekit's](http://incident57.com/codekit) .kit feature which helps creating html files out of multiple assets via @include rule

--

Furthermore and quite more important your own css is based on [SCSS](http://sass-lang.com).

What does that mean in detail?

* 1 scss file which creates 1 css file (style.scss -> style.css)
* in there, a common structure gets imported which contains an index,a variables file which gets divided into various subfiles (named after the variables group) again to have a better overview as well as most common elements (subfiles again)

--

Last but not least it makes use of the [Codekit's](http://incident57.com/codekit) .kit feature which helps creating html files out of multiple assets via the @include rule

What does that mean in detail?

* 1 file (.kit) which creates 1 html file (depends on naming of the kit file)
* in there all specified include documents get implemented and build a complete html file

## Use the framework if:

* You want to build a project based on [HTML5 Boilerplate](http://html5boilerplate.com) and [Bootstrap](http://twitter.github.com/bootstrap)
* You want your own css code to make use of scss
* You want to use [Codekit for Mac](http://incident57.com/codekit) or [Hammer for Mac](http://hammerformac.com) to make use of easy creation of new html documents (Kit files or just an the html file (rename .kit to html and it will be build in the Hammer Build folder))


## Installation

**Requires Sass 3.2**


The framework is incredibly easy to get up and running (provided you’re all set for Sass). Simply [download the latest version](https://github.com/Tischers/Frontend_Framework/archive/Main.zip) of the framework from right here on GitHub, unpack the zip file and watch the scss folder.

You can watch the file by `cd`ing into the directory that houses the `.scss`
and running the following:

   
   
	 $ sass --watch style.scss:style.min.css --style compressed


Alternatively you can just drag and drop the folder containing the project right into [Codekit for Mac](http://incident57.com/codekit) or [Hammer for Mac](http://hammerformac.com) and the rest gets done automatically...

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
	

	\*------------------------------------*/
 
_variables.scss_

	/*------------------------------------*\
    Include.scss
	\*------------------------------------*/

	/**
	 * Generic helper classes and project mixins.
	**/

	@import "generic/mixins"; 
	@import "generic/helper";
  
	/**
	 * Includes all the various parts
	**/
	
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


## Architecture - HTML (.kit feature)

_index.kit_
	
	Logically imports all specific html parts into the document at its respective place
	
	<!--
	===============================================
	* Project Name:
	* Project Description:
	* File Name:
	* Author: 
	* Version:
	* Last Change:
	* Log:
	* ToDo:
	===============================================
	-->

	<!-- @include "includes/_pre_header.html" -->

	<head>

	<!--
	===============================================
	Meta_Basic
	===============================================
	-->
    <meta charset="UTF-8" >
	<meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1" >
	<meta name="viewport" content="width=device-width, initial-scale=1">

	<!-- Responsive not resizable
	<meta name="viewport" content="width=device-width, minimum-scale=1.0, maximum-scale=1.0, user-scalable=no" />
	-->
	<!--
	===============================================
	Meta_Page_Info
	===============================================
	-->
    <title></title>
	<meta name="description" content="xyz" >
	<meta name="keywords" content="xyz" >

	<!-- @include "includes/_header_css.html" -->

	<!-- @include "includes/_header_js.html" -->

	<!-- @include "includes/_header_msc.html" -->


	</head>

	<body>
	<!-- @include "includes/_body_begin.html" -->
	<!-- @include "includes/_nav.html" -->



	<!-- @include "includes/_footer.html" -->
	<!-- @include "includes/_body_end.html" -->
	</body>

	</html>

_The following files are being imported:_

	<!-- @include "includes/_pre_header.html" -->
	<!-- @include "includes/_header_css.html" -->
	<!-- @include "includes/_header_js.html" -->
	<!-- @include "includes/_header_msc.html" -->
	<!-- @include "includes/_body_begin.html" -->
	<!-- @include "includes/_nav.html" -->
	<!-- @include "includes/_footer.html" -->
	<!-- @include "includes/_body_end.html" -->
	
Each of them contains content which should be the same on each file/page you create so that you can just rename the index.kit to the page you want to create...

--

##### Currently the files are filled with boilerplate best practice code based on the provided index.html file which comes with the standard installation of boilerplate

--

## Credits

Due to the fact the framework is based on Bootstrap and Boilerplate the Credits goes the the creators:

* [HTML5 Boilerplate - v4.0.3](http://html5boilerplate.com)
* [Bootstrap - v2.2.2](http://twitter.github.com/bootstrap)

And probably more…

