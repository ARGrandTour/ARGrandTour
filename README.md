<!DOCTYPE html>
<html>
<head>
    <title>AR.js Location-based</title>
    <!-- Importa A-Frame e AR.js -->
    <script src="https://aframe.io/releases/1.3.0/aframe.min.js"></script>
    <script src="https://raw.githack.com/AR-js-org/AR.js/master/aframe/build/aframe-ar.js"></script>
    <script src="https://raw.githack.com/AR-js-org/AR.js/master/three.js/build/ar-threex-location-only.js"></script>
</head>
<body style="margin: 0px; overflow: hidden;">
    <!-- Definisci una scena A-Frame -->
    <a-scene embedded arjs='sourceType: webcam;'>
        <!-- Definisci la posizione GPS del monumento -->
        <a-entity 
            gps-entity-place="latitude: 41.8902; longitude: 12.4922" 
            geometry="primitive: box" 
            material="color: red" 
            scale="5 5 5">
            <a-text value="Colosseo, Roma" color="#FFFFFF" position="0 2 0"></a-text>
        </a-entity>
        <!-- Camera per AR -->
        <a-camera gps-camera rotation-reader></a-camera>
    </a-scene>
</body>
</html>
