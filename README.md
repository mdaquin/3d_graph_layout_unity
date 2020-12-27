
This is a demo project showing how 3D force layout graph can be implemented in Unity, using Spring Joints.

What it does is explained in https://towardsdatascience.com/3d-force-directed-graphs-with-unity-587ad8f7dff

# Importing

To import into Unity, create a new project and copy everything here to the "Assets" directory of your project. The scene with the graph is "GraphScene".

You might need to re-add the scripts to the objects if the paths are lost when importing. That includes the graph.cs script in the graph object, the node.cs script for the node prefab you want to use, and the camera.cs script for the camera.

The node and edge prefabs might have lost their material too, so you might need to re-add that. 

# Using

The graph objects has a number of parameters:
   - The file to use (GML file) - if no file is given, the example graph will be computed
   - The prefab to use for nodes. It should be a RigidBody, preferably with frozen rotation and a child that is a 3D text to show the label.
   - The prefab for edges
   - The size of the space in which nodes will be initially placed.

The camera can go back and forth and will always look towards the centre of the graph. It has a:
   - a speed parameter
   - it needs to be provided with the graph object

The prefabs folder includes a number of node and edge styles from the article linked above. Some include a text for the label of the node, some don't.
To set the distance between nodes, scale the box collider of the node prefab you are using.

A number of GML files are included in the Resource folder, and come from https://github.com/gephi/gephi/wiki/Datasets

# Disclaimer

Check the LICENCE file for the (open source) licence.

This is a demo project, so using it might not be straighforward, and it might not always behave in the expected way. For example, the graph often becomes unstable if its size is set to be much larger than needed, but it will also converge to a bad layout if it is too small. The graph will move arround and not remain static, and it is not possible to predict where it goes, so the camera will always look towards the center. It does limit the possibility of exploring the graph though. Any suggestion, feedback or contribution welcome.

