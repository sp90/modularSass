#Modular SASS

## Why
I needed a structure so that if i make 2 apps for 1 client and i need to reuse my topbar from the first app and it needs to be used inside my secound app it needs to take me secounds to move.

## How
So how do i do that here iv'd made a modular structure everything you build should be modules, thats the stuff you wanna move or reuse.

The core is here to setup basic tags like h1, h2, h... and extend their use so if you need to invert the text color you add a .invert and its inverted the color

Pages is just if you have a specific style for a page i use this really rarely but its nice to have for big projects.

Settings is for basic setup like fonts, colors, grids and more

Vendor is external libraries for mixins, animations and more

## What
So what to take from all this. Its basicly just to take notice to the modules folder thats where you have your modularity which you can move to other projects the core should be the same in every project tough you can extend and customize it to the project usage, pages is where you put page specific styles.

This enables you to move a module fx "topbar" move it to a new project and reuse all the style that comes with it and copy the html where you need it to go.


##The stucture

* all.scss - // **Ties up the whole structure**
* Core - // **The core is extendable**
	* _core.scss - // **Binds all core elements in**
	* document
		* defaults
	* forms
		* inputs
	* texts
		* headers
		* paragraphs
		* links 
* Modules - // **Modules should be moveable**
	* _modules.scss  - // **Binds all modules in**
	* topbar - // **example modules**
		* _sample-submodule.scss
		* _topbar.scss - // **Binds all submodules in**
* Pages - // **Pages are project specific**
	* _pages.scss  - // **Binds all pages in**
	* _sample-page.scss
* Settings
	* _breakpoints.scss - // **Setup breakpoints here**
	* _mixins.scss - // **Local or personal mixins**
	* _settings.scss - // **Binds all the settings in**
	* _used-animations.scss - // **Add animation keyframes from animate.scss vendor library**
	* extends
		* _extends.scss - // **Binds grid and extends it**
		* _grid.scss - // **CSS grid by csswiziardy**
	* font-stack
		* _font-stack.scss - // **Embed fonts here**
	* variables
		* _colors.scss
		* _easing.scss
		* _fonts.scss
		* _variables.scss - // **Binds all the variables in**
* Vendor
	* _vendor.scss - // **Binds all librarys in** 
	* animate - // **Sass extention on animate.css lib that i made**
	* bourbon - // **Bourbon mixin library by Thoughtbot**
	* breakpoint - // **Breakpoint mixin *DEPRECATED made a subset of it in the local mixin file**
