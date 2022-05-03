---
title: The Platonic Solids
image: https://thynstyx.github.io/vzome-sharing/2022/04/30/21-37-13-Platonics-hull/Platonics-hull.png
layout: vzome
description: 
 How all the Platonic solids exist within the same 3D convex hull with all their nodes lying on the same spherical surface.
---

{% comment %}
 - [***web page generated from this source***][post]
 - [data assets and more info][github]


[post]: <https://thynstyx.github.io/vzome-sharing/2022/01/25/Keplers-Kosmos-Revisited-Hull-Coloured-14-27-22.html>
[github]: <https://github.com/ThynStyx/vzome-sharing/tree/main/2022/01/25/14-27-22-Keplers-Kosmos-Revisited-Hull-Coloured/>
{% endcomment %}

<p>These models in the 30-gon field show the "set" of 5 Platonic solids and their accompanying "packing pieces" which fit witin the same 3D hull.</p>

<p>The colouring of the 3D hull is the same for each model and on loading all the models are aligned in the same way and at the same scale.</p>

<p>There are actually multiple alignments available for positioning Cubes, Octahedra, Icosahedra and Tetrahedra within the hull.</p>

<p>The Tetrahedron model requires 4 "packing pieces" to permit the Tetrahedron to be fitted/extracted within the hull in a physical model.
(The other models can be built/disassembled using only two pieces.)</p>

<p>Only one example of each solid has been selected to keep these representations as simple as possible.  The alternatives could be found in the physical model by rotating the "packing pieces" within the trackball hull.</p>

<p>Notice that the camera position is retained when the model is changed!</p> 

  const sources = [
 "https://ThynStyx.github.io/vzome-sharing/2022/04/30/22-59-09-Platonics-skeleton/Platonics-skeleton.vZome",
 "https://ThynStyx.github.io/vzome-sharing/2022/04/30/21-37-13-Platonics-hull/Platonics-hull.vZome",
 "https://ThynStyx.github.io/vzome-sharing/2022/04/30/22-20-21-Platonics-Tetrahedron/Platonics-Tetrahedron.vZome",
 "https://ThynStyx.github.io/vzome-sharing/2022/04/30/22-22-16-Platonics-Cube/Platonics-Cube.vZome",
 "https://ThynStyx.github.io/vzome-sharing/2022/04/30/22-16-13-Platonics-Octahedron/Platonics-Octahedron.vZome",
 "https://ThynStyx.github.io/vzome-sharing/2022/04/30/22-12-48-Platonics-Icosahedron/Platonics-Icosahedron.vZome",
 "https://ThynStyx.github.io/vzome-sharing/2022/04/30/22-09-54-Platonics-Dodecahedron/Platonics-Dodecahedron.vZome"
 ];
 function prevButton() {
        stepSource(-1);
  }

  function nextButton() {
	stepSource(1);
  }

  function stepSource(step) {
	  const src = document.getElementById("viewer").src;
	  for (let i = 0; i < sources.length; i++) {
		if(src == sources[i]) {
			setSource(i + step);
			break;
		}	  
	  }
  };

  function setSource(index) {
	const viewer = document.getElementById("viewer");
	viewer.src = sources[(index + sources.length) % sources.length];
}
</script>
	
<div>
    <button type="button" onclick='setSource(0)'>Hull Skeleton </button>
    <button type="button" onclick='setSource(1)'>Hull complete </button>	
    <button type="button" onclick='setSource(2)'>Tetrahedron Solid</button>
    <button type="button" onclick='setSource(3)'>Cube Solid </button>
    <button type="button" onclick='setSource(4)'>Octahedron Solid </button>
    <button type="button" onclick='setSource(5)'>Icosahedron Solid </button>
    <button type="button" onclick='setSource(6)'>Dodecahedron Solid </button>	
</div> 
		
<vzome-viewer id="viewer" style="width: 85%; height: 60vh; margin: 5%"
    src="https://ThynStyx.github.io/vzome-sharing/2022/04/30/21-37-13-Platonics-hull/Platonics-hull.vZome" >
  <img id="image" src="https://ThynStyx.github.io/vzome-sharing/2022/04/30/21-37-13-Platonics-hull/Platonics-hull.png" />
  <vzome-viewer style="width: 100%; height: 65vh;"
</vzome-viewer>