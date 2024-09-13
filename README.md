# **Cub3D: A First-Person 3D Maze Exploration Game*

## **Overview**

Cub3D is a 42 school project that challenges you to create a dynamic first-person view inside a 3D maze using **raycasting**, the technique popularized by games like **Wolfenstein 3D**, the first-ever First-Person Shooter (FPS). This project introduces the use of the really simple **MiniLibX** library for rendering 3D graphics in C.

The goal is to simulate a 3D maze from a first-person perspective where the player can move around, interact with the environment, and explore the maze by rendering 2D images in a pseudo-3D style using raycasting principles.

## **Features**

- **Raycasting**: Implemented raycasting to render 2D projections of 3D walls from the player's viewpoint.
- **Maze Navigation**: Players can navigate through the maze with smooth movement using W, A, S, D keys.
- **Wall Textures**: Dynamically displayed wall textures based on the direction (North, South, East, West) the player faces.
- **Floor and Ceiling Colors**: Customizable floor and ceiling colors using RGB values.
- **MiniLibX Integration**: Utilized the MiniLibX library for handling window creation, image rendering, and key events.
- **Player Interaction**: Implemented player controls, such as looking around (left and right arrow keys) and moving within the maze.

## **Map Structure**

The game uses a `.cub` file format to describe the map and game configuration. The map file includes:
- Wall textures for all directions (North, South, East, West).
- Customizable floor and ceiling colors.
- A grid layout for the maze, where:
  - `1` represents a wall.
  - `0` represents a walkable space.
  - `N`, `S`, `E`, `W` indicate the player’s starting position and orientation.

### Example Map Structure:

```
NO ./ressources/textures/capybara/capybara1.xpm42
EA ./ressources/textures/capybara/capybara2.xpm42
SO ./ressources/textures/capybara/capybara3.xpm42
WE ./ressources/textures/capybara/capybara4.xpm42
	
F 59,59,59
C    22,50,85	 		 	

1111111111111111111111111111
111111000001111110001111111111
1111110000011111000001111111111
1111110000011111000001111
111111000001111111011111111
1111110000000000000000001
11111100000001000000001111111111
1111110000001000000000111101111
11111100000000000N0000000111111111111
111111000000000000000111011111100011111
     111111110011111111101   11000001111
1111111111100000011111110111110001101111
1111110000001111000011110111110000001111
1111110000011 110000011101111100000011111
11111100000111110000011101111100000000001
11111100000111111100011101111100000000001
11111100000000000000000001111100011100001
11111100000001000000001111111100000000001
11111100000010000000001111110000000000001
111111000000000000000011111111000000000011111111
111111000000000000000000000000000000000011111111
111111111111111111111111111111111111111111111111
1111111111111111111111111111111111111111111111111111111111111111
```

## **Technology Stack**

| Technology  | Description                                      |
|-------------|--------------------------------------------------|
| **Language**| C                                                |
| **Graphics**| MiniLibX (MLX)                                   |
| **Raycasting**| Custom raycasting algorithm inspired by Wolfenstein 3D|
| **External Functions** | Open, Close, Read, Write, Printf, Malloc, Free, etc. |

## **MiniLibX and Raycasting**

The **MiniLibX** library (or MLX) provides a simple framework for working with graphics in 42 projects. It allows creating windows, drawing pixels, handling keyboard/mouse events, and displaying images. MLX was crucial for rendering the game visuals in Cub3D, and its use is a core part of this project.

**Raycasting**, on the other hand, is a technique used to render 3D-like environments in 2D by calculating the distance between the player and the objects around them. Cub3D employs this technique to simulate depth and perspective as players navigate the maze.

## **Controls**

- `W`: Move forward
- `S`: Move backward
- `A`: Strafe left
- `D`: Strafe right
- `←`: Look left
- `→`: Look right
- `ESC`: Exit the game

## **Resources**

- [Raycasting Tutorials by Lode](https://lodev.org/cgtutor/raycasting.html): An excellent resource for understanding the raycasting technique.
- [MiniLibX Documentation](https://harm-smits.github.io/42docs/libs/minilibx.html): Guides on using the MiniLibX library effectively.
- [Game Engine Black Book: Wolfenstein 3D](https://fabiensanglard.net/gebbwolf3d/book.shtml): A deep dive into the technical development of Wolfenstein 3D.

## Demo

