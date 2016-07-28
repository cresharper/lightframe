# Lightframe - yet another CSS grid system for building web pages.

Version: 0.8 (beta release)
Author: Connor Harper

Github pages page coming soon...

I was inspired to write my own grid system/framework because others, specifically bootstrap, are incredibly bloated with a lot of features most don't use and it is hard to create a custom UI without tons of overrides and customizations. So this inspired me to write Lightframe.

Lightframe is a framework that is designed to help Front End Developers build web pages in a streamlined matter without the bloat of modern CSS frameworks. It is based on a floated columns and flexbox layout. All websites have 3 major components: navigation, content and footer. Lightframe enables you to build these parts of your pages out quickly and with minimal bloat. Lightframe has *no UI styles Associated with it* - which gives the developer much more flexibility to customize the look and feel of the UI for their project.

This framework assumes the developer understands how to build custom UIs. If you're looking for a "starting point" for your UI, I would recommend looking into something like [materializecss](http://materializecss.com/). 

If you need to support legacy browsers (specifically, IE8 or IE9) for the flexbox grid, please use a polyfill, such as [Flexibility](https://jonathantneal.github.io/flexibility/).  

To use this out of the box, simply include lightframe.css in the <head> of your page found in lightframe/css/lightframe.css

## How to use

Table of contents:
* Grid system
* Navigation
* Footer

1. Grid System

To utilize the grid for 1-3 items you have one of the following divs:

    <div class="col-full"></div>

    <div class="col-half"></div>

    <div class="col-third"></div>

    <div class="col-quarter"></div>

    <div class="col-flex"></div>

And so on. Much like a bootstrap, you will need to wrap these in a container and row. For the grid structure, it will simply look like this:

    <div class="container">
	   	<div class="row">
	   		<div class="col-full">
	   			<div class="content">
	   			<p>Content here</p>
	   			</div>
	   		</div>
	   	</div>
	</div>

	<div class="container">
	   	<div class="row">
	   		<div class="col-half">
	   			<div class="content">
	   			<p>Content here</p>
	   			</div>
	   		</div>
	   		<div class="col-half">
	   			<div class="content">
	   			<p>Content here</p>
	   			</div>
	   		</div>
	   	</div>
	</div>

And so on... <div class="content"> has a default padding of 20px. 

2. Navigation 

    <nav class="lf-menu">
		<img class="lf-menu__logo" src="/img/dynatrace-logo.png">	
		<ul class="lf-menu__items">
			<li><a href="">Item 1</a></li>
			<li><a href="">Item 2</a></li>
			<li><a href="">Item 3</a></li>
			<li><a href="">Item 4</a></li>
		</ul>
	</nav>

Add the prefix of "--right" or "--left" to either of the children of <nav class="lf-menu"> to float items in their respective directions.  


3. Footer 

The footer is basically identical to the navigation

    <div class="lf-footer">
		<ul class="lf-menu__items--stacked lf-menu__items--right">
			<li><a href="">Item 1</a></li>
			<li><a href="">Item 2</a></li>
			<li><a href="">Item 3</a></li>
			<li><a href="">Item 4</a></li>
		</ul>
	</div>


# lightframe
