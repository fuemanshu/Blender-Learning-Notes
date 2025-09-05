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
        - Mirror
        - Bevel
        - Solidy

    

Chapter 5 - Creating Low Poly Mushrooms

Chapter 6 - Understanding Materials and Shading