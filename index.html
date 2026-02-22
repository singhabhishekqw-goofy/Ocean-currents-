<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Interactive Ocean Globe</title>
<style>
body { margin:0; overflow:hidden; background:#000814; font-family:sans-serif; }
#popup{
position:absolute;
bottom:20px;
left:50%;
transform:translateX(-50%);
background:rgba(0,0,0,0.85);
color:white;
padding:15px 20px;
border-radius:12px;
display:none;
box-shadow:0 0 20px cyan;
max-width:80%;
text-align:center;
}
.label{
position:absolute;
color:cyan;
font-size:12px;
text-shadow:0 0 8px cyan;
pointer-events:none;
}
</style>
</head>
<body>

<div id="popup"></div>

<script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
<script src="https://threejs.org/examples/js/controls/OrbitControls.js"></script>

<script>

var scene = new THREE.Scene();

var camera = new THREE.PerspectiveCamera(
60,
window.innerWidth/window.innerHeight,
0.1,
1000
);
camera.position.z = 3;

var renderer = new THREE.WebGLRenderer({antialias:true});
renderer.setSize(window.innerWidth,window.innerHeight);
renderer.setPixelRatio(window.devicePixelRatio);
document.body.appendChild(renderer.domElement);

var controls = new THREE.OrbitControls(camera,renderer.domElement);
controls.enableDamping = true;
controls.enablePan = false;
controls.minDistance = 1.5;
controls.maxDistance = 5;

var light = new THREE.DirectionalLight(0xffffff,1.5);
light.position.set(5,3,5);
scene.add(light);

var geometry = new THREE.SphereGeometry(1,64,64);

var texture = new THREE.TextureLoader().load(
'https://threejs.org/examples/textures/planets/earth_atmos_2048.jpg'
);

var material = new THREE.MeshStandardMaterial({map:texture});
var earth = new THREE.Mesh(geometry,material);
scene.add(earth);

var currents = [];

function createCurrent(name,color,points,info){

var curve = new THREE.CatmullRomCurve3(points);
var tubeGeometry = new THREE.TubeGeometry(curve,100,0.02,8,false);
var tubeMaterial = new THREE.MeshBasicMaterial({color:color});
var mesh = new THREE.Mesh(tubeGeometry,tubeMaterial);

mesh.userData = { name:name, info:info };

scene.add(mesh);
currents.push(mesh);

}

// Gulf Stream
createCurrent(
"Gulf Stream",
0xff0000,
[
new THREE.Vector3(-0.5,0.2,0.8),
new THREE.Vector3(-0.2,0.4,0.9),
new THREE.Vector3(0.2,0.6,0.8),
new THREE.Vector3(0.5,0.7,0.6)
],
"Warm current flowing from Gulf of Mexico to Western Europe."
);

// California Current
createCurrent(
"California Current",
0x00ffff,
[
new THREE.Vector3(-0.9,0.3,0.2),
new THREE.Vector3(-0.8,0.0,0.4),
new THREE.Vector3(-0.7,-0.3,0.5)
],
"Cold current flowing southward along North America."
);

var raycaster = new THREE.Raycaster();
var mouse = new THREE.Vector2();

window.addEventListener("click",function(event){

mouse.x = (event.clientX / window.innerWidth)*2 -1;
mouse.y = -(event.clientY / window.innerHeight)*2 +1;

raycaster.setFromCamera(mouse,camera);
var intersects = raycaster.intersectObjects(currents);

if(intersects.length > 0){
var data = intersects[0].object.userData;
var popup = document.getElementById("popup");
popup.style.display = "block";
popup.innerHTML = "<h3>"+data.name+"</h3><p>"+data.info+"</p>";
}
});

function animate(){
requestAnimationFrame(animate);
controls.update();
renderer.render(scene,camera);
}

animate();

window.addEventListener("resize",function(){
camera.aspect = window.innerWidth/window.innerHeight;
camera.updateProjectionMatrix();
renderer.setSize(window.innerWidth,window.innerHeight);
});

</script>

</body>
</html>
