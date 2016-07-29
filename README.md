# Lightframe - simple CSS grid system for building web pages.

Version: 0.8 (beta release)

I was inspired to write my own grid system/framework because others, specifically bootstrap, are incredibly bloated with a lot of features that aren't used a lot of the time and it is hard to create a custom UI without tons of overrides and customizations. So this inspired me to write Lightframe.

Lightframe is a grid/framework that is designed to build web pages in a streamlined matter without the bloat of modern CSS frameworks. It is based on a floated columns and flexbox layout. All websites have 3 major components: navigation, content and footer. Lightframe enables you to build these parts of your pages out quickly and with minimal bloat. Lightframe has *no UI styles Associated with it* - which gives the developer much more flexibility to customize the look and feel of the UI for their project.

This framework assumes the developer understands how to build custom UIs. If you're looking for a "starting point" for your UI, I would recommend looking into something like [materializecss](http://materializecss.com/) or even [Bootstrap](http://getbootstrap.com/)

If you need to support legacy browsers (specifically, IE8 or IE9) for the flexbox grid, please use a polyfill, such as [Flexibility](https://jonathantneal.github.io/flexibility/). 

To use this out of the box, simply include lightframe.css in the <head> of your page found in lightframe/css/lightframe.css

## If you want to make modifications to the SASS files:

1. Clone the repo
2. open up command line, navigate to the repo and run     npm install
3. Run     gulp
4. Make changes in the source SASS files to suit your specifc needs, then include the compiled "styles.css" file to your page. 

## How to use lightframe.css

Table of contents:
* Grid system
	* Flex Grid
* Navigation
* Footer

1. Grid System

To utilize the grid for 1-3 items you have one of the following divs:

    <div class="col-full"></div>

    <div class="col-half"></div>

    <div class="col-third"></div>

    <div class="col-quarter"></div>

    <div class="col-flex"></div>

And so on. Much like a standard grid, you will need to wrap these in a container and row. For the grid structure, it will simply look like this:

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

1A. Flex Grid

Using the flex grid/columns is the same HTML structure as the standard grid. For the flex grid to work, you simply divide your container width by how many items you have per row, and define the width in pixels. 

For example, if you have a container of 1200px, and you have 3 items per row, you would set a width of 400px to the flex column. So it would change to:

    .col-flex { display: flex; margin: auto; padding-bottom: 4rem; width: 400px; }

If you have different flex rows with different number of items per row, use a modifier class and change:

    .col-flex--new { display: flex; margin: auto; padding-bottom: 4rem; width: 400px; }

This also applies for the other columns as well. to customize simply use a modifier class.

The SASS file does the math for you on line 71 in dev/scss/_lightframe.scss. 

2. Navigation 

    <nav class="lf-menu">
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
