# audio

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
        if (isMusicPlay){
            isMusicPlay  = false;
            playerMusic.pause();
            btnMusic.classList.remove('active-btn');
        }
        else {
            isMusicPlay = true;
            playerMusic.play();
            btnMusic.classList.add('active-btn');
        }
    });
   
    btnMusicMenu.addEventListener("click", function() {
        event.preventDefault();
        if (isMusicPlay){
            isMusicPlay  = false;
            playerMusic.pause();
            btnMusicMenu.classList.remove('active-btn');
        }
        else {
            isMusicPlay = true;
            playerMusic.play();
            btnMusicMenu.classList.add('active-btn');
        }
    });
   
 });
