# randomized_text
Takes a selector, randomizes the value for a random interval, hides the random value, and reveals the true value afterwards.

HTML USE:
		<div>
			<div class="letter"><span class="trueletter">G</span></div>
			<div class="letter"><span class="trueletter">R</span></div>
			<div class="letter"><span class="trueletter">U</span></div>
			<div class="letter"><span class="trueletter">M</span></div>
			<div class="letter"><span class="trueletter">P</span></div>
			<div class="letter"><span class="trueletter">Y</span></div>
    </div>
    
jQuery USE:
  $('.letter').each(function() {
    // grab our trueletter container
		var trueletter = $(this).find('.trueletter');

    // clone trueletter container and do some CSS/Class stuff to it
		$(trueletter).css('display','none').clone().insertAfter(trueletter).removeClass('trueletter').addClass('randomletter').css('display','block');
		
		// set all other vars we'll use
		var randomletter = $(this).find('.randomletter');
		var counter = 0;
		var interval = 0;
		var interval = Math.floor(Math.random()*(200-100+1)+100); // max 150 and min 100
		
		// interval function to run through our loop
		// randomizes our letter before hiding it and showing our true letter
		var randomize = setInterval(function() {
		  //randomize the letter
			var rand = String.fromCharCode((Math.random() * 50) + 43);
			$(randomletter).text(rand);
			
			// stop loop with conditional
			if( counter >= interval ) {
			  clearInterval(randomize);
				randomize = 0;
				$(randomletter).css('display','none');
				$(trueletter).css('display','block');
			};
			counter++;
		}, 10);
	});
