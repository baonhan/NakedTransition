#Naked Transition

Naked Transition is an image transition plugin for jQuery based on jqFancyTransitions by Ivan Lazarevic (http://workshop.rs/projects/jqfancytransitions/).  Where most image transition libraries are built coupled with a slider or gallery functionality (including jqFancyTransitions), Naked Transitions allows you to simply swap two images with neat transition.

##Usage

###Required Markup
Naked Transtion works by replacing the background image of a div with another image that is transitioned in.  By the end of the transition, the background-image style property will be replaced with the new image.  As a result, the following css is required on the div:

`
background-image
position - absolute or relative
width - must be the width of the background image
height - must be the height of the background image
`
Additionally, the new image must be the same dimensions of the original image.

###Running function

davidgranado.com/demos/naked-transitions

`$('div-selector').jqNakedTransition(newImageLocation)`

newImageLocation - A string url of the new image to replace the image in the div.  If this form is used, a default animation will run.

`$('div-selector').jqNakedTransition(newImageLocation, params)`

newImageLocation - A string url of the new image to replace the image in the div.  If this form is used, a default animation will run.

params - an object containing the config options for the animation:

	*strips* Integer - number of strips in animation. __(default 15)__
	*stripSpeed* Integer - time required for each strip to complete animation in ms. __(default 500)__
	*stripDelay* Integer - time between the start of one strip's animation and the start of the next strip's animation animation in ms. __(default 500)__
	*position* String with possible values 'top', 'bottom', 'alternate', 'curtain' - describes where the strips will the animation sequence. __(default alternate)__
	*direction* String with possible values 'left', 'right', 'alternate', 'random', 'fountain', 'fountainAlternate' - describes which strip will animate first and in which order the next animation will proceed. __(default fountainAlternate)__
	*effect* String with possible values 'curtain', 'zipper', 'wave' Preset animations that will override many of the other options __(default none)__
	*complete* function to run once animation is completed. __(default none)__