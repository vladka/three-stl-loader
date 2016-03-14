## three-stl-loader

@aleeper's [THREE.STLLoader](http://threejs.org/examples/js/loaders/STLLoader.js) repackaged as a node module

## install

`npm i --save three-stl-loader`

## usage

```js

var THREE = require('three')
require('three-stl-loader')(THREE)

var loader = new THREE.STLLoader()

loader.load('./path/to/stl', function (geometry) {
  var material = new THREE.MeshPhongMaterial({
    color: 0xff5533,
    specular: 0x111111,
    shininess: 200
  })

	var mesh = new THREE.Mesh(geometry, material)
	mesh.position.set(0, - 0.25, 0.6)
	mesh.rotation.set(0, - Math.PI / 2, 0)
	mesh.scale.set(0.5, 0.5, 0.5)
	mesh.castShadow = true
	mesh.receiveShadow = true

	scene.add(mesh)
})

```
