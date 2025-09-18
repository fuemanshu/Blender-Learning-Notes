Blender Notes


Book: Low Poly 3D Modeling in Blender
Author: Samuel Sullins


Chapter 2 - Understanding Low Poly Modeling

Understanding Meshes
- blender objects are 2 parts
    - underlying mesh
    - object's location, rotation, and scale

    - mesh is the underlying shape (model part of a 3D model)
    - mesh is made of vertices, edges, and faces
        - vertices - single points in 3D space
        - edges - lines that connect vertices
        - faces (polygons) - shapes defined by edges

    - smooth vs. flat shading
        - smoothness is only an illsion
        - all objects have flat shading and smooth shading must be enabled if desired

    - High poly vs. Low poly
        - poly count - number of polygons/faces in a mesh
        - gives good idea of complexity of a mesh
        - the more polygons the more computing power required

        High Poly
            - generally in the millions
            - low poly - up to a few hundred
                - medium is in between
            - blender struggles with high vertices count
            - used for high detail - but can fake with great textures
            - usually created with digital scanning or sculpting

        Mid-Poly
        - balance of enough polygons that can be deformed for animations
        - used in animated films as part of a subdivision workflow
            - faces are divided into smaller faces
        
        Low poly
            - very few polygons
            - simplistic look
            - suited for simple video games or animated sequences

        good to keep models in the low-to-mid poly range (for cpu resource reasons)

        Low Poly as an art style
        - flat-shaded, unsmoothed, minimal 3D artwork
        - clean, simplistic style
        - goal is to embrace simplicity of an object
        - create with only required polygons
        - simplify but not too much
        - simplicity and complexity
        - simple object combined with realistic shading, high resolution rendering, and modern lighting techniques
        
            - The Rule of Polygons
                - relation between an objects polygon count and its size to importance in the scene
                - the smaller an object, the fewer the polygons it should have
                - example - an object that has smaller versions should be their own 3d model so the polygons shapes are the same size
                - helps looks more cohesive and professional

Chapter 3 - Creating a Low Poly Tree

- Transforming objects
    - Transform - position, rotation, scale
    - edit mode
    - extrusion
    - parenting objects

Part 2 - Modeling and Shading for Low Poly

Chapter 4 - Exploring Modifiers
    
    - Modifiers allow you to make edits and changes that are not permanent until you apply them
    - Modifiers simplify and automate tasks

    Modifiers
        - Array
            - Duplicates object over and over in a straigth line, as many times as you want
            - examples - fence, wooden bridge
            - can combine with Curve Modifier to create line of objects along a curve
            - Count - number of duplicates
            - Relative Offset - spacing between duplicates
            - when you using Array, the amount of duplicates will expnentially duplicate
                - example, 10 count will result in 10 duplicates in the first array, the next array duplicate of the same object with a 10 count will result in 100 total objects
        - Mirror / glass
            - helps making symetrical objects easier and efficient
            - examples, character, vehicle, or almost anything
            - usually the X axis is where objects are mirrored
            - you can attach your mirrow to another object (chair example)
        - Bevel
            - used to round off or chamfer sharp edges
            - used mainly in real world objects since most objects are rouned (even really sharp objects)
            - Amount - size of bevel
            - Segment - controls the smoothness of bevel
            - Angle - any angles greater than set angle is beveled
                - great for objects with smooth and sharp edges
            - 
        - Solidify
            - like the Extrude tool in Edit Mode - adding thickness to a mesh
            - simply adjust the Thickness value for desired affect
            
Chapter 5 - Creating Low Poly Mushrooms

    - Reference Images
    - Starting with Basic Shapes
    - Edit mesh for low poly look

    - Reference Images
        - recommended to give you an idea of what you are making
        - or just have a clear idea of what you're going to create
    
    - Starting with Basic Shapes
        - start with shape similar to desired object (don't create more work for yourself)
        - 

    - sides
        - tri - 3 sided
            - simplest possible shape
            - used in high poly meshes
            - cannot be bent
            - use seldomly and only for artistic scenes not videos or games
        - quad - 4 sided
            - ideal for subdivision work
            - keep flat
        - n-gon - 5 or more
            - best used as perfectly flat
            - don't bend well
    - Triangulation
        - 
    - Starting with Basic Shapes
    - Edit mesh for low poly look

Chapter 6 - Understanding Materials and Shading

    - what are materials and how they work
    - create materials
    - edit materials
    - understand basics of Shader Editor
    - add multiple materials to one model

    - Rendering Engine - does the work of rendering
        - calculates what scene looks like from pov of camera, simulates light and shadow
        - Blender has two - Eevee and Cycles
    - Materials decide how light is going to react with objects
        - materials define all the physical properties of an object's surface
            - color, roughness, shine, metalic, transparency, etc.
        - lights must be set up to see materials
        - Material Preview mode - lets you view materials with default ligthing setups
        - Shading Workspace - where you create materials
        
    - Shader Editor
        - For Low Poly - Only need Shader Editer
        - Nodes - pieces of materials (building blocks that perform a specific function)
            - connect sockets together to build complicated materials
            - Two defaults nodes
                - Principle BSDF
                - Material Output
            - Principle BSDF - (Bidirectional Scattering Distribution Function)
                - calculates how light bounces off a surface
                - only note connected to Surface output
                - focus on these inputs
                    - Base Color, Metallic, Roughness
                    - with these you can make different materials***
                        - mirror - base color -> black, metaliic -> 1, roughness -> 0
                        - shiny plastic - metallic -> 0, roughness -> 0
                        - gold -> base color -> organe-yellow (#FCB001FF), metallic -> 1, roughness -> 0-0.1
            - Material Output
                - always last in material/node tree
                - Surface input - most important
                    - connects to Shader - which defines what the surface looks like and how each face displayed at render time
                - shaders nodes are green
        - Material Slots - allows different materials for different parts on an object
            - create the slots in the Shader Editer, then assign them to specific surfaces

Part 3 - Creating Your Own Assets

Chapter 7 - Creating a Low Poly Tractor
    - break your model into parts to make it manageable
    - think through the process before starting (brainstorm)
    - use Inset, Extrude, and Scale to make shapes (Tractor Example)
        - Alt + E to bring up menu to Extrude Individual Faces (in individual directions)

Chapter 8 - Low Poly Environment Modeling
    - grass - cylinder w/ 3 vertices, scale down top face to taper, add extra vertices in order to add curvature, merge top face (press m, Center) to make grass pointy
    - Proportional Editing - allows for a certain action to affect other things within a certain distance (Fall Off Radius)
    - Rocks - icosphere, join - select two opposing vertices and press j (when there are more than 4 or more edges on the face on an icosphere)
    - merge - allows you to merge vertices to one location if there are too many in one area
    - Knife tool (K) - used to add vertices in the middle of edges, great for adding variety to simple objects that are duplicated

Chapter 9 - Modeling a Kangaroo
    - Importing Reference Images
    - Where to Start when modeling an animal
    - Steps to model any animal in low poly
    
    - Knife tool is very helpful
    - Reference Images - find whatever you can for reference
        - multiple angles - front, side, top
        - simple line art is the usually the best
        - search "[animal] bluebprint image"
    - Importing into Blender
        - set up view so Front View (1) shows front of animal or object
        - Use Opacity setting to make image easier to look at
        - use multiple angles in Blender for reference (front and side usually work best)
    - Start with a Plane mesh, then extrude it
        - do all the following as a plane first
            - set up the basic shape of the torso, then extrude the limbs, neck, and head
        - 

Chapter 10 - Creating Low Poly Houses and Buildings
    - build two skyscrapers
        - add details to skyscrapers
    - create a house
        - make windows and roofs
    
    - creating details on an existing building or model
        - duplicate object
        - then delete faces not needed
        - select all edges, then go to Edges > Subdivide
        - delete faces where you want openings, etc
        - use solidfy to add thickness
            - adjust thickness (negative and positive values are usable)
    - Alt + D  (duplicate with materials - changing materials in one object will replicate it same objects)
    - 


Chapter 11 - Using the Asset Browser