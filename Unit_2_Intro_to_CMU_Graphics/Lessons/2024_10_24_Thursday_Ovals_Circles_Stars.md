# AP Computer Science Principles
Thursday, October 24th 2024

### Ovals, Circles, & Stars

**AIM(s):** <br>
How do we code and customize ovals, circles, and stars?

**OUTCOME ALIGNMENT**:<br> 
<ins>TYS61XT.4</ins> Code using appropriate syntax.<br> 
<ins>TYS61XT.5</ins> Communicate effectively as a Computer Scientist.<br> 
<ins>TYS61XT.6</ins> Engage in the design thinking process to iteratively develop your work.<br> 

**SUCCESS CRITERIA:**
- [ ] I can describe the difference between parameters and arguments.
- [ ] I can use proper syntax to code and customize ovals, circles, and stars.

<table>
  <tr>
    <td>
      <b>DO NOW:</b><br>
      1. In your IDLE make a new file called "Ovals_Circles_Stars_Notes.py" and paste in the starter code from the agenda. <br><br>
      2. In your notebook draw a t-chart and sort the following elements into two categories: <b>Arguments</b> and <b>Parameters</b> <br><br>
      <i>For an extra challenge: Match the arguments to their parameters (there may be multiple combinations) </i><br>
     <ul>
      <li> 'orange'</li>
      <li> 5</li>
      <li> fill</li>
      <li> width</li>
      <li> start</li>
      <li> border</li>
      <li> rgb(0,35,2)</li>
      <li> 'top'</li>
      <li> gradient('red','blue')</li>
      <li> 370</li>
      <li> top</li>
      </ul>
      
</td>
</tr>
</table>

**AGENDA:**

1. Ovals, Circles, and Stars Code Along
    * Starter Code
      ```python
      # Import the CMU Graphics Package:
      from cmu_graphics import *

      # Run program:
      cmu_graphics.run()
      ```
    * Ovals
      * Oval Coordinates vs. Rect Coordinates
      * rotateAngle property
    * Circles
      * radius property
    * Stars
      *  points property
      *  roundness property
   
5. Practice: Start your assignment below.
   
**HOMEWORK:** <br><br>
[Unit 2 Assignment 07](https://github.com/MrJSwotinsky/AP_Computer_Science_Principles/blob/main/Unit_2_Intro_to_CMU_Graphics/Daily_Assignments/07_Due_Fri_Oct_25_Lab_4_Ovals_Circles_Stars.md)<br>


## Resources


|Primary Resources|
|---|
|[Parameters vs. Arguments](https://github.com/MrJSwotinsky/AP_Computer_Science_Principles/tree/main/Resources)<br><br>[CMU Graphics Built-in Color List (including names and RGB Triplets)](https://academy.cs.cmu.edu/docs/builtInColors)<br><br>[The Google Color Picker](https://www.google.com/search?q=google+color+picker&sca_esv=808cf4c753ad636e&rlz=1C1CHBF_enUS904US904&sxsrf=ADLYWILLYFkuoNVAlQnxJdNxPVMnA-AelA%3A1729365379453&ei=gwUUZ52pG5al5NoPhLWrkAE&ved=0ahUKEwjd9oOJlJuJAxWWElkFHYTaChIQ4dUDCBA&uact=5&oq=google+color+picker&gs_lp=Egxnd3Mtd2l6LXNlcnAiE2dvb2dsZSBjb2xvciBwaWNrZXIyChAAGLADGNYEGEcyChAAGLADGNYEGEcyChAAGLADGNYEGEcyChAAGLADGNYEGEcyChAAGLADGNYEGEcyChAAGLADGNYEGEcyChAAGLADGNYEGEcyChAAGLADGNYEGEcyDRAAGIAEGLADGEMYigUyDRAAGIAEGLADGEMYigVI6h9QiRBYsR1wAXgBkAEAmAFToAGfAqoBATS4AQPIAQD4AQGYAgWgAtQCwgIKECMYgAQYJxiKBcICCxAAGIAEGJECGIoFwgIFEAAYgATCAgcQIxiwAhgnwgIHEAAYgAQYDZgDAOIDBRIBMSBAiAYBkAYKkgcBNaAHkB0&sclient=gws-wiz-serp)|

|New Code|Description and Details|
|---|---|
|`Oval(centerX, centerY, width, height)`|Unlike rectangles, the first two parameters give us the center coordinates for the oval. <br><br> The `rotateAngle` property can be used to rotate the oval, or any shape (MUST BE BETWEEN 0 AND 360). For example : `Oval(50,50,30,30, rotateAngle=45`)|
|`Circle(centerX, centerY, radius)`|The first two parameters give us the center coordinates for the circle. <br><br>`radius` defines the length of half the circle (MUST BE GREATER THAN 0)|
|`Star(centerX, centerY, radius, points, roundness=none)`| The first two parameters give us the center coordinates for the star. <br><br>`radius` determines how large the star is (MUST BE GREATER THAN 0)<br><br> `points` determines how many points are in the star (MUST BE GREATER THAN 2) <br><br> `roundness` changes how round the star is (MUST BE BETWEEN0 to 100)|
|**Old Code**|**Description and Details**|
|`gradient(color1, color2, color3, ..., start='center')`|`Gradient` can be used in place of a color for the `fill` parameter. <br><br>For example, in the following code: `Rect(50,50,100,100,fill='blue')`,`'blue'` can be replaced by `gradient('yellow','blue',start='top')` as such: <br><br>`Rect(50,50,100,100,fill=gradient('yellow','blue',start='top'))`<br><br>Gradients need at least 2 colors and can have up to as many colors as you want it to.<br><br>The parameter `start` can be used to customize the gradient.<br><br>The argument passed to `start` can be used to define where the first color begins and then the gradient will proceed linearly or radially across the shape. `start` is set to 'center' by default and can be set to the following values: <br><br> <img src = "https://github.com/MrJSwotinsky/AP_Computer_Science_Principles/blob/main/Resources/Gradient_Start_Values.png">|
|`Rect(left, top, width, height, fill, border, borderWidth)`|The parameters `fill`, `border`, and `borderWidth` can be used to customize rectangles (and other shapes).<br><br>Arguments passed to `fill`, `border`, and `borderWidth` are passed using the **keyword passing technique** meaning they are passed using parameter names.<br><br>The argument passed to `fill` sets the color of the rectangle.<br><br>The argument passed to `border` sets the color of the rectangle's border.<br><br>The argument passed to `borderWidth` sets the width of the rectangle's border.<br><br>Built in colors may be described using their names such as `'midnightBlue'` or `'hotPink'`.  CMU Graphics has a over 100 built-in colors.  **Note:** When using color names, the color names must be surrounded by quotes.<br><br>Other colors may be described using their RGB Triplets such as `rgb(75,15,120)`, a shade of very dark purple, similar, but not identical to, CMU Graphics' `'indigo'` or `rgb(255,180,5)` a shade of bright orange, similar, but not identical to, CMU Graphics' `'orange'`. **Note:** When using RGB triplets, quotes are not required. <br><br>**Example**:<br>`Rect(50, 100, 40, 80, fill = 'navy', border = rgb(185,245,250), borderWidth = 5)` generates a navy rectangle with a light blue border that is 5 pixels wide, as shown below.<br><br><img src = "https://github.com/MrJSwotinsky/AP_Computer_Science_Principles/blob/main/Resources/Rectangle_Image.png" width=50%>
