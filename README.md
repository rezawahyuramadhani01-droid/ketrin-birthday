    <script>
        const toggle = document.getElementById('mode-toggle');
        const body = document.body;
        const greeting = document.getElementById('greeting');
        const message = document.getElementById('message');
        const profilePic = document.getElementById('profile-pic');
        
        const audioCutie = document.getElementById('audio-cutie');
        const audioBaddie = document.getElementById('audio-baddie');

        toggle.addEventListener('change', function() {
            if(this.checked) {
                // BADDIE MODE ACTIVATED
                audioCutie.pause();
                audioBaddie.currentTime = 0; // Forces song to start from the beginning
                audioBaddie.play();
                
                // Swaps to Baddie Photo
                profilePic.src = "https://github.com/rezawahyuramadhani01-droid/ketrin-birthday/raw/main/baddie-photo.jpg";
                
                body.classList.add('baddie-mode');
                greeting.innerText = "HBD KETRIN.";
                message.innerText = "To the coolest, most unstoppable girl I know. Own your day.";
            } else {
                // CUTIE MODE ACTIVATED
                audioBaddie.pause();
                audioCutie.currentTime = 0; // Forces song to start from the beginning
                audioCutie.play();
                
                // Swaps back to Cutie Photo
                profilePic.src = "https://github.com/rezawahyuramadhani01-droid/ketrin-birthday/raw/main/cutie-photo.jpg";
                
                body.classList.remove('baddie-mode');
                greeting.innerText = "Happy Birthday, Ketrin!";
                message.innerText = "To the girl who makes every day brighter. Hope your birthday is as sweet and amazing as you are!";
            }
        });
    </script>
