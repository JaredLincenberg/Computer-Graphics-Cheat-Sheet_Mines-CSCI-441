# CSCI 441: Computer Graphics
### Dr. Jeffrey Paone
## Using
* OpenGL
* GLFW3
* GLM
* SOIL
### Sources For Class
* Website: [cs-courses.mines.edu/csci441](https://cs-courses.mines.edu/csci441/index.html)
* Canvas: [Home Page](https://elearning.mines.edu/courses/18245)
## How to do stuff
### Triangles
```
glBegin(GL_TRIANGLES);{
  glColor3f(r,g,b); // RGB values between 0-1
  glVertex2f(x1,y1); // Points of the triangle
  glVertex2f(x2,y2);
  glVertex2f(x3,x3);
  // New Triangle
  glVertex2f(x4,y4); // Points of the triangle
  glVertex2f(x5,y5);
  glVertex2f(x6,x6);
};glEnd(); //Important
```
```
glBegin(GL_TRIANGLE_FANS);{
  glColor3f(r,g,b); // RGB values between 0-1
  glVertex2f(ax1,ay1); // Anchor point of the triangle
  glVertex2f(x2,y2); 
  glVertex2f(x3,x3); // Creates triangle (a1,2,3)
  glVertex2f(x4,y4); // Creates triangle (a1,3,4)
  glVertex2f(x5,y5); // Creates triangle (a1,4,5)
};glEnd(); //Important
```
```
glBegin(GL_TRIANGLE_STRIP);{
  glColor3f(r,g,b); // RGB values between 0-1
  glVertex2f(x1,y1); 
  glVertex2f(x2,y2); 
  glVertex2f(x3,x3); // Creates triangle (1,2,3)
  glVertex2f(x4,y4); // Creates triangle (2,3,4)
  glVertex2f(x5,y5); // Creates triangle (3,4,5)
};glEnd(); //Important
```
### Lines

### 2D Color
#### There are two types of interpolation in Open GL:
1. `glShadeModel(GL_FLAT);`
  * Takes the color of the last vertex of a triangle as the color for the whole triangle.
2. `glShadeModel(GL_SMOOTH);`
  * Takes the color of all vertices and averages them based on distance.
## Transformations
#TK
## Callback Functions
### Functions that take in function pointers
### [Guide](https://www.glfw.org/docs/latest/input_guide.html)
### [Reference](https://www.glfw.org/docs/latest/group__input.html)
#### Put in `GLFWwindow* setupGLFW(){}`
* `glfwSetMouseButtonCallback( windowMain, mouse_button_callback );`
  * `void mouse_button_callback(GLFWwindow *win, int button, int action, int mods){}`
* `glfwSetKeyCallback( windowMain, key_board_callback);`
  * `void key_board_callback(GLFWwindow *win, int key, int scancode, int action,int mod){}`
