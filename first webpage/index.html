<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Webcam in Green Screen with Background and Filters</title>
    <style>
        /* General Page and Background Styling */
        body, html {
            margin: 0;
            padding: 0;
            height: 100%;
            overflow: hidden;
        }
        #background {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: cover;
            z-index: -2;
        }

        /* Container and Webcam Styling */
        #container {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            z-index: 1;
        }
        #overlay {
            max-width: 100vw;
            max-height: 100vh;
            width: auto;
            height: auto;
            z-index: 2;
        }
       /* Enlarge webcam container */
    #webcam-container {
    position: absolute;
    overflow: hidden;
    z-index: 3;
    border-bottom-left-radius: 8px;
    border-bottom-right-radius: 8px;
    width: 100vw; /* Full viewport width */
    height: 100vh; /* Full viewport height */
    }

/* Webcam fully fills the container */
    #webcam {
    width: 100%;
    height: 100%;
    object-fit: cover;
    transform: scaleX(-1);
    }

        /* PNG Overlay Styling */
        .png-overlay {
            position: absolute;
            transform: translate(-50%, -50%);
            z-index: 4;
            max-width: 50%; /* Set the maximum width to 20% of the viewport width */
            max-height: 50%; /* Set the maximum height to 20% of the viewport height */
        }

         #no-hard-feelings-logo {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-45%, -45%);
           z-index: 5;
            max-width: 180px; /* Adjust width as needed */
            max-height: 180px; /* Adjust height as needed */
            display: none; /* Hidden initially for flashing effect */
    }


        /* Filter Buttons */
        #filter-options {
            position: absolute;
            bottom: 20px;
            left: 20px;
            z-index: 10;
            display: flex;
            gap: 10px;
        }
        .filter-btn {
            padding: 5px 10px;
            background-color: rgba(255, 255, 255, 0.7);
            border: none;
            border-radius: 15px;
            cursor: pointer;
            font-size: 12px;
            transition: background-color 0.3s;
        }
        .filter-btn:hover {
            background-color: rgba(255, 255, 255, 0.9);
        }
        #webcam-container.lines::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: repeating-linear-gradient(
                0deg,
                transparent,
                transparent 2px,
                rgba(0, 0, 0, 0.1) 2px,
                rgba(0, 0, 0, 0.1) 4px
            );
            z-index: 5;
            pointer-events: none;
            opacity: 0;
            transition: opacity 0.3s;
        }
        #webcam-container.lines::before {
            opacity: 1;
        }

        /* Glitch Effect */
#webcam-container.glitch::after {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: repeating-linear-gradient(
        45deg,
        rgba(255, 0, 0, 0.3),
        rgba(0, 64, 255, 0.3) 10px,
        rgba(60, 255, 0, 0.3) 10px
    );
    animation: glitch-animation 0.5s infinite;
    pointer-events: none;
}
@keyframes glitch-animation {
    0% { transform: translate(0, 0); }
    25% { transform: translate(-1.5px, -1.5px); }
    50% { transform: translate(3px, 3px); }
    75% { transform: translate(-3px, 3px); }
    100% { transform: translate(0, 0); }
}


/* Neon Glow Effect */
#webcam-container.neon-glow {
    filter: brightness(1.5) contrast(1.5) saturate(2) drop-shadow(0 0 5px #ffffff);
}


/* Fisheye Effect */
#webcam-container.fisheye {
    filter: blur(1px) contrast(1.5) saturate(2);
    transform: scale(1.3) rotate(15deg);
}

/* Dirty Green Glow Filter */
.filter-dirty-green {
    filter: contrast(5) brightness(0.8) hue-rotate(80deg) saturate(0.4);
    box-shadow: 0 0 10px 5px rgba(35, 68, 2, 0.4); /* Green glow effect */
}


    </style>
</head>
<body>
    <img id="background" src="background.png" alt="Background Image">
    <div id="container">
        <img id="overlay" src="POP UP BIG.png" alt="Overlay with Green Screen">
        <div id="webcam-container">
            <video id="webcam" autoplay playsinline></video>
        </div>
        <img id="no-hard-feelings-logo" src="NO HARD FEELINGS .png" alt="No Hard Feelings Logo">

        <!-- Centered PNG Overlays -->
        <img id="png-overlay-1" class="png-overlay" src="hazard icons.png" alt="PNG Overlay 1">
        <img id="png-overlay-2" class="png-overlay" src="sensitive content.png" alt="PNG Overlay 2">
    </div>

    <div id="filter-options">
        <button class="filter-btn" data-filter="none">Normal</button>
        <button class="filter-btn" data-filter="grayscale(100%)">B&W</button>
        <button class="filter-btn" data-filter="brightness(1.2) blur(5px)">Bloom</button>
        <button class="filter-btn" data-filter="lines">Lines</button>
        <button class="filter-btn" data-filter="sepia(100%)">Sepia</button>
        <button class="filter-btn" data-filter="brightness(0.7) contrast(1.2)">Low Exposure</button>
        <button class="filter-btn" data-filter="glitch">Glitch</button>
        <button class="filter-btn" data-filter="neon-glow">Neon Glow</button>
        <button class="filter-btn" data-filter="fisheye">Fisheye</button>
        <button class="filter-btn" data-filter="dirty-green">Dirty Green Glow</button>

    </div>

    <script>
        const background = document.getElementById('background');
        const overlay = document.getElementById('overlay');
        const webcamContainer = document.getElementById('webcam-container');
        const video = document.getElementById('webcam');
        const humanError = document.getElementById('human-error');
        const filterButtons = document.querySelectorAll('.filter-btn');
        
        // Overlay PNGs
        const pngOverlay1 = document.getElementById('png-overlay-1');
        const pngOverlay2 = document.getElementById('png-overlay-2');

        // Access webcam
        navigator.mediaDevices.getUserMedia({ video: true })
          .then(stream => {
              video.srcObject = stream;
          })
          .catch(error => {
              console.error('Error accessing webcam:', error);
              alert('Could not access the webcam. Please ensure it is connected and permissions are granted.');
          });

        // Function to position the webcam within the green screen area
        function positionWebcam() {
          const greenScreenX = 272.5; 
          const greenScreenY = 205; 
          const greenScreenWidth = 1006; 
          const greenScreenHeight = 729.5;

          const scale = overlay.width / overlay.naturalWidth;

          webcamContainer.style.left = `${greenScreenX * scale}px`;
          webcamContainer.style.top = `${greenScreenY * scale}px`;
          webcamContainer.style.width = `${greenScreenWidth * scale}px`;
          webcamContainer.style.height = `${greenScreenHeight * scale}px`;
      }

      // Position webcam and overlays when the overlay image is loaded
      overlay.addEventListener('load', positionWebcam);
      window.addEventListener('resize', positionWebcam);

      // Set initial position for PNG overlays (centered)
      pngOverlay1.style.left = '60%';
      pngOverlay1.style.top = '65%';
      pngOverlay2.style.left = '80%';
      pngOverlay2.style.top = '50%';

    // Flashing logo functionality
    setInterval(() => {
    const logo = document.getElementById('no-hard-feelings-logo');
    if (logo.style.display === 'none') {
        logo.style.display = 'block';
    } else {
        logo.style.display = 'none';
    }
    }, 1000); // Change 1000 to adjust the flashing interval (in milliseconds)

      // Filter functionality
      filterButtons.forEach(button => {
          button.addEventListener('click', () => {
              const filter = button.getAttribute('data-filter');
              webcamContainer.classList.remove('lines');
              
              if (filter === 'lines') {
                  webcamContainer.classList.add('lines');
                  video.style.filter = 'none';
              } else {
                  video.style.filter = filter; // Apply selected filter
              }
          });
      });


      filterButtons.forEach(button => {
    button.addEventListener('click', () => {
        const filter = button.getAttribute('data-filter');
        webcamContainer.classList.remove('lines', 'glitch', 'double-exposure', 'polar-coordinates', 'neon-glow', 'tilt-shift', 'blur-glow', 'color-shift','filter-dirty-green', 'fisheye');
        
        // Remove previous filter classes and apply the selected one
        if (filter === 'lines') {
            webcamContainer.classList.add('lines');
            video.style.filter = 'none';
        } else if (filter === 'glitch') {
            webcamContainer.classList.add('glitch');
            video.style.filter = 'none';
        } else if (filter === 'neon-glow') {
            webcamContainer.classList.add('neon-glow');
            video.style.filter = 'none';
        } else if (filter === 'dirty-green') {
            webcamContainer.classList.add('filter-dirty-green');
            video.style.filter = 'none';  // Make sure no conflicting inline filter is applied
        } else if (filter === 'fisheye') {
            webcamContainer.classList.add('fisheye');
            video.style.filter = 'none';
        } else {
            // If no special filter, apply the CSS filter to the video directly
            webcamContainer.classList.remove('glitch', 'double-exposure', 'neon-glow', 'tilt-shift', 'blur-glow', 'color-shift', 'sketch', 'pixelate', 'fisheye');
            video.style.filter = filter;
        }
    });
});

    </script>
</body>
</html>
