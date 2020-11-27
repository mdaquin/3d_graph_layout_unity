
This is a simple project showing how 3D force layout graph can be implemented in Unity, using Spring Joints.

What it does is explained in https://towardsdatascience.com/3d-force-directed-graphs-with-unity-587ad8f7dff

To import into Unity, create a new project and copy all everything here to the "Assets" directory of your project. The scene with the graph is "GraphScene". The graph objects has a number of parameters:
   - The file to use (GML file) - if no file is given, the example graph will be computed
   - The prefab to use for nodes. It should be a RigidBody, preferably with frozen rotation and a child that is a 3D text to show the label.
   - The prefab for edges
   - The size of the space in which nodes will be initially placed.

The camera can go back and forth and will always look towards the centre of the graph. It has a speed parameter.

GML files included from https://github.com/gephi/gephi/wiki/Datasets 

