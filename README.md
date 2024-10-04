# exoplanets_ar.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AR Exoplanets Experience</title>
    <script src="https://aframe.io/releases/1.2.0/aframe.min.js"></script>
    <script src="https://cdn.rawgit.com/AR-js-org/AR.js/3.3.2/aframe/build/aframe-ar.js"></script>
    <style>
        body { margin: 0; }
        canvas { display: none; }
    </style>
</head>
<body style="margin: 0; overflow: hidden;">
    <a-scene embedded arjs>
        <!-- Marker for TRAPPIST-1e -->
        <a-marker preset="hiro">
            <a-image src="https://upload.wikimedia.org/wikipedia/commons/9/99/TRAPPIST-1e_artistic_rendering.jpg" 
                     scale="2 2 2" 
                     position="0 0 0">
            </a-image>
        </a-marker>

        <!-- Marker for Proxima Centauri b -->
        <a-marker preset="kanji">
            <a-image src="https://upload.wikimedia.org/wikipedia/commons/a/a6/Proxima_Centauri_b.png" 
                     scale="2 2 2" 
                     position="0 0 0">
            </a-image>
        </a-marker>

        <!-- Marker for Kepler-442b -->
        <a-marker preset="data-color">
            <a-image src="https://upload.wikimedia.org/wikipedia/commons/c/c8/Kepler-442b.png" 
                     scale="2 2 2" 
                     position="0 0 0">
            </a-image>
        </a-marker>

        <a-entity camera></a-entity>
    </a-scene>

    <script>
        // Optional: Add custom functionality here
    </script>
</body>
</html>
