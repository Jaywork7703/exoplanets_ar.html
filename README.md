<!DOCTYPE html><script src="https://cdn.jsdelivr.net/gh/aframevr/aframe@1.3.0/dist/aframe-master.min.js"></script>
<script src="https://raw.githack.com/AR-js-org/AR.js/master/aframe/build/aframe-ar-nft.js"></script>

<style>
  .arjs-loader {
    height: 100%;
    width: 100%;
    position: absolute;
    top: 0;
    left: 0;
    background-color: rgba(0, 0, 0, 0.8);
    z-index: 9999;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .arjs-loader div {
    text-align: center;
    font-size: 1.25em;
    color: white;
  }
</style>

<body style="margin : 0px; overflow: hidden;">
  <!-- minimal loader shown until image descriptors are loaded -->
  <div class="arjs-loader">
    <div>Loading, please wait...</div>
  </div>
  <a-scene
    vr-mode-ui="enabled: false;"
    renderer="logarithmicDepthBuffer: true; precision: medium;"
    embedded
    arjs="trackingMethod: best; sourceType: webcam;debugUIEnabled: false;"
  >
    <!-- we use cors proxy to avoid cross-origin problems ATTENTION! you need to set up your server -->
    <a-nft
      type="nft"
      url="your-server/https://raw.githack.com/AR-js-org/AR.js/master/aframe/examples/image-tracking/nft/trex/trex-image/trex"
      smooth="true"
      smoothCount="10"
      smoothTolerance=".01"
      smoothThreshold="5"
    >
      <a-entity
        gltf-model="your-server/https://raw.githack.com/AR-js-org/AR.js/master/aframe/examples/image-tracking/nft/trex/scene.gltf"
        scale="5 5 5"
        position="150 300 -100"
      >
      </a-entity>
    </a-nft>
    <a-entity camera></a-entity>
  </a-scene>
</body>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AR Exoplanets Experience</title>
    <script src="https://aframe.io/releases/1.2.0/aframe.min.js"></script>
    <script src="https://cdn.jsdelivr.net/gh/AR-js-org/AR.js@3.3.2/aframe/build/aframe-ar.js"></script>
    <style>
        body { margin: 0; }
        canvas { display: none; }
    </style>
</head>
<body style="margin: 0; overflow: hidden;">
    <a-scene embedded arjs>
        <!-- Marker for TRAPPIST-1e -->
        <a-marker preset="hiro">
            <a-image src="https://images.immediate.co.uk/production/volatile/sites/3/2020/06/GettyImages-1200812247-9cb02f2.jpg" 
                     scale="2 2 2" 
                     position="0 0 0">
            </a-image>
            <a-text value="TRAPPIST-1e" position="0 1.5 0" scale="1 1 1" color="#FFFFFF"></a-text>
            <a-text value="40 light years away" position="0 0.8 0" scale="1 1 1" color="#FFFFFF"></a-text>
        </a-marker>

        <!-- Marker for Proxima Centauri b -->
        <a-marker preset="kanji">
            <a-image src="https://cdn.mos.cms.futurecdn.net/cBRbG8de8ybLDGV3Z7n7AE-1200-80.jpg" 
                     scale="2 2 2" 
                     position="0 0 0">
            </a-image>
            <a-text value="Proxima Centauri b" position="0 1.5 0" scale="1 1 1" color="#FFFFFF"></a-text>
            <a-text value="4.24 light years away" position="0 0.8 0" scale="1 1 1" color="#FFFFFF"></a-text>
        </a-marker>

        <!-- Marker for Kepler-442b -->
        <a-marker preset="data-color">
            <a-image src="https://cdn.mos.cms.futurecdn.net/S9g3qUFKu4jb8HDLsPwnLF-1200-80.jpg" 
                     scale="2 2 2" 
                     position="0 0 0">
            </a-image>
            <a-text value="Kepler-442b" position="0 1.5 0" scale="1 1 1" color="#FFFFFF"></a-text>
            <a-text value="1,200 light years away" position="0 0.8 0" scale="1 1 1" color="#FFFFFF"></a-text>
        </a-marker>

        <a-entity camera></a-entity>
    </a-scene>

    <script>
        // Optional: Add custom functionality here
    </script>
</body>
</html>
