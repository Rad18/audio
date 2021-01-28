	document.addEventListener("DOMContentLoaded", () => {
	    var btnMusic = document.querySelector('.tn-elem__2627035031608498774851 .tn-atom');
	    var btnMusicMenu = document.querySelector('.t450__right_buttons_but .t-btn');
	    var playerMusic = document.getElementById('player');
	    var isMusicPlay = false;
	   
	    playerMusic.onended = playerMusic.onerror = function() {
	        playerMusic.src = playerMusic.currentSrc;
	        playerMusic.play();
	    };
	  
btnMusic.addEventListener("click", function() {
	        event.preventDefault();

	        if (isMusicPlay) {
	            isMusicPlay = false;
	            playerMusic.pause();
	            btnMusic.classList.remove('active-btn');
	            pauseTS = Date.now();
            console.log(pauseTS);
	        }
	        else {
	            isMusicPlay = true;
	            btnMusic.classList.add('active-btn');
            
             pauseTS = Date.now();
          console.log(pauseTS);
	            if (pauseTS != null) {
	            	var secondsToSkip = (Date.now() - pauseTS) / 1000;
	            	var resumeTime = playerMusic.currentTime + secondsToSkip;
	            	
	            	while(resumeTime > playerMusic.duration) {
	            		resumeTime -= playerMusic.duration;
	            	}

	            	playerMusic.currentTime = resumeTime;
	            }

	            playerMusic.play();
	        }
	    });
	   
	    btnMusicMenu.addEventListener("click", function() {
	        event.preventDefault();

	        if (isMusicPlay) {
	            isMusicPlay = false;
	            playerMusic.pause();
	            btnMusicMenu.classList.remove('active-btn');
	            pauseTS = Date.now();
             console.log(pauseTS);
	        }
	        else {
	            isMusicPlay = true;
	            btnMusicMenu.classList.add('active-btn');
              pauseTS = Date.now();
            
             console.log(pauseTS);
	            if (pauseTS != null) {
	            	var secondsToSkip = (Date.now() - pauseTS) / 1000;
	            	var resumeTime = playerMusic.currentTime + secondsToSkip;
	            	
	            	while(resumeTime > playerMusic.duration) {
	            		resumeTime -= playerMusic.duration;
	            	}

	            	playerMusic.currentTime = resumeTime;
	            }

	            playerMusic.play();
	        }
	    });

    
    

    
    
    
    
    
    
    
    
    
//     btnMusic.addEventListener("click", function() {
// 	        event.preventDefault();

// 	        if (isMusicPlay) {
// 	            isMusicPlay = false;
// 	            playerMusic.pause();
// 	            btnMusic.classList.remove('active-btn');
// 	            pauseTS = Date.now();
// 	        }
// 	        else {
// 	            isMusicPlay = true;
// 	            btnMusic.classList.add('active-btn');

// 	            if (pauseTS != null) {
// 	            	var secondsToSkip = (Date.now() - pauseTS) / 1000;
// 	            	var resumeTime = playerMusic.currentTime + secondsToSkip;
	            	
// 	            	while(resumeTime > playerMusic.duration) {
// 	            		resumeTime -= playerMusic.duration;
// 	            	}

// 	            	playerMusic.currentTime = resumeTime;
// 	            }

// 	            playerMusic.play();
// 	        }
// 	    });
	   
// 	    btnMusicMenu.addEventListener("click", function() {
// 	        event.preventDefault();

// 	        if (isMusicPlay) {
// 	            isMusicPlay = false;
// 	            playerMusic.pause();
// 	            btnMusicMenu.classList.remove('active-btn');
// 	            pauseTS = Date.now();
// 	        }
// 	        else {
// 	            isMusicPlay = true;
// 	            btnMusicMenu.classList.add('active-btn');

// 	            if (pauseTS != null) {
// 	            	var secondsToSkip = (Date.now() - pauseTS) / 1000;
// 	            	var resumeTime = playerMusic.currentTime + secondsToSkip;
	            	
// 	            	while(resumeTime > playerMusic.duration) {
// 	            		resumeTime -= playerMusic.duration;
// 	            	}

// 	            	playerMusic.currentTime = resumeTime;
// 	            }

// 	            playerMusic.play();
// 	        }
// 	    });
    
    
     
     
	 });


