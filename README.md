animateCSS
==========

A tiny jQuery plugin for native CSS animation with jQuery (chainable)

CSS animation parameters
----------
1. transition-duration
2. transition-timing-function
3. transition-delay

Example
----------
<javascript>

	$(this).fadeIn().animateCSS({
		
		'duration': '0.2s',
		'timing_function': 'ease-in',
        'css': {
        	'transform': "scale(1.1, 1.1)"
        }
	
	}).animateCSS({
    
        'duration': '0.5s',
        'timing_function': 'ease-out',
        'css': {
        	'transform': "scale(1, 1)"
        }
    
    }).queue(function(next) {
        
        console.log('Animation done!')
        next();
        
    });
