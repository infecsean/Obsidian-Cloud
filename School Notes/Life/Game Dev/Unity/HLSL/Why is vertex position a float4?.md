# Why the FUCK is a vertex position a float4?
---
Resources: [thread](https://forum.unity.com/threads/a-vertex-position-is-a-float4-what-does-the-4th-component-represent.152809/)

In matrix transformations, transformations are represented by 4x4 matrices.
The first three floats are linear ==transformations== in 3D (Rotation, scaling, etc...)

The fourth float is a vector, it is a ==translation== (displacement).

The fourth float is always 1, since a 0 would represent a transformation, discarding the need to use a fourth float.

I mean it is linked in the thread above but heres the wikipedia page
[Get into details](https://en.wikibooks.org/wiki/Cg_Programming/Vertex_Transformations#Structure_of_the_Model_Matrix)