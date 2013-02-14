# Fluid Text Resizer #

*Description:* Fluid Text Resizer is a compact yet versatile jQuery text resizer script. It can adjust the text size of a particular section of your page, such as just the primary content area, multiple sections, or the entire document in general. A fluid animation is used to morph into the new text size, and session cookies are used to remember the new setting. It works by first getting the default font size of the target section, whether the unit is pixels, em etc, then increasing or decreasing that accordingly. In other words, it's adaptive.

## Directions ##

*Step 1:* This script uses the following external files:

+ jQuery 1.4 or above (served via Google CDN)
+ fluidtextresizer.js
+ Sample images for the controls

*Step 2:* Add the below code to the HEAD section of your page:

	<style type="text/css">
	
	.controlstyle a{ /*links inside DIV sizecontroldiv*/
	outline:none;
	}
	
	.controlstyle a img{ /*image links inside DIV sizecontroldiv*/
	border-width:0;
	}
	
	.controlstyle a.selectedcontrol img{ /*selected control's image*/
	border-bottom:4px solid darkred;
	}
	
	</style>
	
	<script type="text/javascript" src="http://ajax.googleapis.com/ajax/libs/jquery/1.4.2/jquery.min.js"></script>
	
	<script type="text/javascript" src="fluidtextresizer.js">
	
	/***********************************************
	* Fluid Text Resizer- © Dynamic Drive DHTML code library (www.dynamicdrive.com)
	* Visit http://www.dynamicDrive.com for hundreds of DHTML scripts
	* This notice must stay intact for legal use
	***********************************************/
	
	</script>
	
	<script type="text/javascript">
	
	var mytextsizer=new fluidtextresizer({
		controlsdiv: "sizecontroldiv", //id of special div containing your resize controls. Enter "" if not defined
		targets: ["body"], //target elements to resize text within: ["selector1", "selector2", etc]
		levels: 3, //number of levels users can magnify (or shrink) text
		persist: "session", //enter "session" or "none"
		animate: 200 //animation duration of text resize. Enter 0 to disable
	})
	
	</script>


*Step 3:* Then, add the below sample markup to your page:

	<div id="sizecontroldiv" class="controlstyle">
	
	Increase/Decrease controls: <a href="#smaller"><img src="fontminus.gif" /></a>  <a href="#bigger"><img src="fontplus.gif" /></a><br /><br />
	
	Font levels controls: <a href="#fontsize-1"><img src="-1.gif" /></a> <a href="#fontsize0"><img src="0.gif" /></a> <a href="#fontsize1"><img src="1.gif" /></a> <a href="#fontsize2"><img src="2.gif" /></a>
	
	</div>
	
	<p>Arbitrary link control: <a href="javascript:mytextsizer.setFontLevel(0)">Set font level to default</a>

## Fluid Text Resizer Set up ##

See script project page for additional details on setup and documentation: <http://www.dynamicdrive.com/dynamicindex9/fluidtextresizer.htm>
