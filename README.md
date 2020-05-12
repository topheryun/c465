# c465 - Lego Blocks - Unity - C#
Project 1 is basically 3d Tetris using Lego blocks. 
Project 2 is Minecraft using Lego blocks.

## Project 1
Chances are you have played with Lego while growing up. Now you get the opportunity to develop a virtual version of your favorite toy Lego!

The intention of this project is to get your hands dirty with the Unity game engine, and apply some of your skills and creativity in designing an developing the project. 

Executive Summary of Project
You are tasked to create a program that will simulate the falling of Lego blocks of different shapes and sizes randomly from the sky and land on a given platform of an NxM dimensions. While the blocks are falling, the user has the ability to move the falling block within the boundaries of the platform as well as rotate the falling block using their keyboard.

Lego Block Dimensions
Lego Blocks have specific dimensions. You will need to study these specifications and come up with your model based on them.

The image above illustrates the basic unity of a Lego Block. Notice that the units are in metric. In Unity you are also using the metric system. This will be useful as you don't need to make unity conversion, but you will need to understand how to model your Lego Blocks to meet the specifications. 

Hint: When you create a Unit Cube in Unity, it is always 1 Cubic Meter.

The following is an illustration of some of the Lego Blocks that exist. We are going to implement only a subset of the Lego Bricks and Plate for our project.

Lego Bricks and Plates Required for Implementation
Brick 1x1 through Brick 1x6
Brick 2x2 through Brick 2x6
Plate 1x1 through Plate 1x6
Plate 2x2 through Plate 2x6
Lego Color Palette
Use the chart below to define your Lego block colors.

Use the color chart above to define your Lego block colors.

Extra Credit
If you have the appetite for implementing more interesting Lego Blocks, you may do so. Before your implementation, please consult with me.

Core Requirements for the Project
Your project should implement at a minimum the following:

Dynamically generate the platform where the Lego blocks are going to land. The dimensions of the platform will be provided by the user when they run the application.
Dynamically instantiate one of the many Lego blocks at random.
The instantiated Lego block will have a random position on the XZ plane.
The instantiated Lego block will have a random orientation. 
Orientation for Lego block can be only the following 0, 90, 180, 360.
The instantiated Lego block will have a random color assigned to it.
Take a look at the official color palette presented to you.
User can move the falling Lego Block on the XZ plane.
You will use the following keys for the movement: A,W,S,D
User can re-orient the falling Lego Block using the same constraints listed above.
You will use the R key for rotation of the block.
The falling block will stop when it has landed either on the platform or on another existing block.
The cycle will begin all over again until the user quits the application.
The application can be terminated by pressing the Q button.
Camera Movement
The user will also have the ability to control some aspects of the camera during the simulation. They will be able to perform the following:

Rotate the camera around the platform, always looking at the center of the platform
You will use the left and right arrow keys for rotating the camera around the platform.
Move the camera Up and Down on the Y-Axis
You will use the up and down arrow keys for elevating the camera position or lowering it.
Zoom In or Out the camera for closer look at the platform
You will use the z and x keys to zoom in and zoom out the camera.
User Interface and Setup
Your application will have a user interface to help the user along  with your application. When you run your application, it will provide the user with a main menu, where the user can start the simulation, configuration some settings, and exit the application.

Additional Program Requirements
Your program will have two distinct scenes. 

MainMenu
GameScene
You will get additional points if you implement singleton pattern in your project design for the UI. This was demonstrated in class and very easy to implement. 

Your User Interface will have at a minimum the following functions / features:

Start Button
Setting Button
Exit Button
In your Setting Panel you will have at a minimum the following configuration options:

Dimension for the platform (MxN) for simplicity, we can keep the length and width the same, so just one dimension for the base.
Difficulty level, i.e., speed of blocks that are being dropped.
Mode: Uniform or Break-away.
Optional and extra credit, audio for the simulation.
During the simulation, you will also have a small menu present that can bring up the configuration menu and the option to reset or exit the game.

You will get extra points for your design, code structure, code cleanness, over all project design and efficiency.

Your report is a CRITICAL element of the grade, make sure that you do a good job on your report that is clean and has relevant technical details with the appropriate screen-shots. If you have taken software-engineering, think about the way you created your design document.

## Project 2
Now that you have completed  the first project simulating falling Lego blocks, in your next project you will be creating a new mode where you can manually place the Lego blocks and construct something cool at runtime.

The core of the project is driven from a demo I did in class called Building Blocks. The objective of this project is to enhance your understanding of GameObjects, World Space, Transforms, Camera Controls, Graphical User Interfaces along with Mouse and Keyboard Inputs and other cool stuff...

Building Blocks Demo
Building Blocks is a simple project that allows the user to place 1-unit cubes on a predefined board. You can think of it as a block game that allows the user to attach or stack-up cubes to create a specific shape.

To complete this assignment you will need to be familiar with several concepts:

GameObjects
Transforms
Physics Raycast
Object instantiation
Normals
Materials
Textures
Tag
User Interface Design
Event Handlers
Project Specifications:

You are extending Project 1 and adding the following features to it:

Update your Main Menu and Setup Configuration to have a new Mode
In the new mode, you will need to provide the user with the following features and capabilities
UI Panel displaying the user their Lego block types for selection
UI Panel displaying the user their Lego block color or material
UI Panel displaying the user general features such as
Delete
Duplicate
Undo
The user will use the mouse to interact with the world. You will need to perform a few tasks here:

Getting the Mouse Input, Left Click
Create a RaycastHit object to determine info of hit object(s)
Use Physics.Raycast() to determine if you hit something or not
Use Camera.main.ScreenToRay() to convert the mouse coordinate to a Ray object
Determine if you have a hit
If you do have a hit, you will need to determine, what you have hit!

If you are placing a Lego block on the base then the positioning is going to be different then when you are going to be placing a Lego block adjacent to an existing Lego block.

Other Important Implementation Factor

 dynamically display a semi-transparent cube while user is deciding where to place the cube on the board and or other cubes.
if on the board, semi-transparent material will be yellow.
if on a face of an existing block, the cube will have semi-transparent material colored green.
All other functions/features are the same.

Raycasting and Layers
We saw how layers can come in handy during our program development. They can be used to organize your GameObjects by yet another data point. The benefits of layers are many, and one of the benefits can be seen when you are casting a ray. You can simply use a layer mask to tell the ray casting function to ignore GameObjects that are on certain layers.

You will need to define the layers at design time, but you can modify the layer of GameObjects at runtime, given you are using the predefined layers.

