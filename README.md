Sparks.js
=========

#### My updates for this lib ####

Just use it in THREE.js
Look at code example:

    scene.add(new THREE.Particles({
                                    size:10,
                                    count: 100,
                                    position: new THREE.Vector3(0,0,0),
                                    program:function(ctx){
                                        ctx.fillRect(0, 0, 10, 10);
                                    },
                                    sparksInit: function(emitter, SPARKS){
                                        var sphereCap = new SPARKS.SphereCapZone(0, 0, 0, 0, 0, 10);
                                        emitter.addInitializer(new SPARKS.Lifetime(0,2));
                                        emitter.addInitializer(new SPARKS.Velocity(sphereCap));
                                        emitter.addAction(new SPARKS.Age());
                                        emitter.addAction(new SPARKS.Move());
                                        emitter.addAction(new SPARKS.Accelerate(0.2));
                                    },
                                    position: new THREE.Vector3(10,10,10)
                                  })
            );

You can view online demo here http://elephanter.github.io/sparks.js

#### Simple 3D Javascript Particles Engine ####

Sparks.js is a library to help create 3D particles in Javascript.

Its simple, fast and fun to play with.

This is an ongoing project, so check out issue tracker, the [wiki](https://github.com/zz85/sparks.js/wiki), the code and examples inside github.

Sparks.js welcomes feature and pull requests, so don't be shy to fork away!

It uses [three.js](https://github.com/mrdoob/three.js) for Vector classes and rendering and uses ease functions from [tween.js](https://github.com/sole/tween.js/).

####Demos Online####
- http://jabtunes.com/labs/arabesque/
- http://jabtunes.com/itcameupon/

####Examples Online####
- [Particle Tests](http://jsdo.it/zz85/27tB/fullscreen)
- [Brillance Particles + Custom Shapes](http://jsdo.it/zz85/x8Gf)
- [Realtime Sparks.js Editor by Jerome Etienne](https://github.com/jeromeetienne/sparkseditor) 

####Articles####
- [Article on Sparks.js by Jerome Etienne](http://learningthreejs.com/blog/2011/12/14/particles-introduction-to-sparks-js/)
- [Presentation on Sparks.js by Jerome Etienne](https://github.com/jeromeetienne/slides-sparks.js)

####Upcoming features####
- Text Particles
- ShotCounter


