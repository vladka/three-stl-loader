## three-stl-loader-fork

THIS IS FORK OF https://github.com/bohdanbirdie/three-stl-loader published in npm

@aleeper's [THREE.STLLoader](http://threejs.org/examples/js/loaders/STLLoader.js) repackaged as a node module

## install

`npm i --save three`

`npm i --save three-stl-loader-fork`

## usage

```js

var THREE = require('three')
var STLLoader = require('three-stl-loader-fork')(THREE)

var loader = new STLLoader()

loader.load('./path/to/daaaamn.stl', function (geometry) {
  var material = new THREE.MeshNormalMaterial()
  var mesh = new THREE.Mesh(geometry, material)
  scene.add(mesh)
})

```
