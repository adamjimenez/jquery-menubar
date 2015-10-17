# Documentation #

## Description ##

This plugin for jQuery UI provides a menubar with togglable top-level menu items, multileveled menu items, checkable menu items.

The HTML elements use standard jQuery UI class names.


## Options ##

```
var defaults = {
		
	// whether or not to add the drop down arrow for top-level menu items
	addArrow: true,
	
	// text to use as arrow
	titleArrowText: "<small>&nbsp;&#9660;</small>",
	
	// how long to wait to open sublevel menu items
	menuOpenDelay: 200,
	
	// whether to close the menu on pressing the escape key
	closeOnEsc: true,
	
	// an array of more objects as the root list of menuitems
	// e.g. 
	// {
	//     name: "Menu item", // the name of the menu item
	//     checkable: false, // whether the menu item is checkable (or togglable for top-level items)
	//     disabled: false, // whether the item should start off disabled
	//     attr: null, // attributes to set on this menu item (e.g. { foo: "value of foo attr", bar: "value of bar attr" })
	//     selecton: function(){}, // callback for when the item is selected on
	//     selectoff: function(){}, // callback for when the item is selected off
	//     select: function(selected)(){}, // callback for when item is clicked (selected set appropriately)
	//     hoveron: function(){}, // callback for when the item is hovered over with the cursor
	//     hoveroff: function(){}, // callback for when the item is hovered off with the cursor
	//     open: function(){}, // callback for when a parent item is opened
	//     close: function(){}, // callback for when a parent item is closed
	//     items: [] // array of sub menu items
	// }
	items: undefined,
};

$("#foo").menubar(defaults);
```


## Events ##

Events can be bound to menu elements (li).  The following events are triggered by the plugin.

  * selecton
  * selectoff
  * select
  * hoveron
  * hoveroff
  * open
  * close


## Functions ##

You can call some functions on the plugin after you've generated the menubar.  They do not trigger events; they bypass them.

  * $(li).menubar("**disable**") : disables the menu item
  * $(li).menubar("**enable**") : enabled the menu item
  * $(**ul**).menubar("**enableall**") : enable everything in the menu
  * $(li).menubar("**selecton**") : make the menu item selected on
  * $(li).menubar("**selectoff**") : make the menu item selected off
  * $(li).menubar("**name**", **newName**) : set a new name for the menu item