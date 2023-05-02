Download Link: https://assignmentchef.com/product/solved-computer-graphics-opengl
<br>
<h1>Overview</h1>

This section lists some basic environments/libraries needed in our following class. In the next section, we will go through details of setting it up in Windows, Mac OS, and Linux.

<ul>

 <li>C++11</li>

 <li>Graphic card support OpenGL 3.3+</li>

 <li>CMake 2.8+ (If you want to compile the libraries on your own)</li>

 <li>Glew</li>

 <li>Glfw/glut/freeglut</li>

 <li>Glm</li>

 <li>NanoGUI/AntTweakBar</li>

 <li>stb_image</li>

</ul>

In this provided example code, you can practice configuring OpenGL shader environment with GUI. It uses NanoGUI as GUI toolkit. The output of this example code should be like this:







<h1>Configuration Tutorial</h1>

This section provides the basic GLEW, GLFW and GLM compile tutorial. For GUI you can feel free to choose any GUI libs such as NanoGUI or AntTweakBar, and for loading images you can feel free to choose any image libs such as stb_image.

The TA has wrapped binary files for windows VS2015 x64 version:<u> link</u>

<u>(https://github.com/kingofyeti/opengl_configuration)</u>, which already includes GLFW, GLEW, GLM, Freeglut, AntTweakBar, NanoGUI and STB_image. It also includes a tutorial <u>link</u>

<u>(http://jody-lu-blog.logdown.com/posts/1533525)</u> for configuring MAC OS version of NanoGUI.




Windows (Visual Studio):

1: Download compiled binary file

<ul>

 <li>GLEW: <u>link (https://sourceforge.net/projects/glew/files/glew/2.0.0/glew-2.0.0win32.zip/download)</u></li>

 <li>GLFW: <u>link (https://github.com/glfw/glfw/releases/download/3.2.1/glfw-</u></li>

</ul>

<u>3.2.1.bin.WIN64.zip)</u>

<ul>

 <li>GLM: <u>link (https://github.com/g-truc/glm/archive/0.9.8.5.zip)</u> 2: Wrap into folder and add to environment path:</li>

</ul>

Add this folder into your system variables with:

Variable name: OPENGL

Variable value: YOUR_CURRENT_FOLDER

Add dll files into directly into project folder (Not recommended)

Put all dll files into a folder and add it into “Path” (Recommended)

Variable name: Path

Variable value: YOUR_DLL_FOLDER

3: Open Visual Studio and create an empty project. Add helloworld.cpp file into it

4: Add external libs path and include path in Property pages (or import prop page)

5: Run code

MAC OS (XCode):

1: Homebrew:

<ul>

 <li>$ brew update</li>

 <li>$ brew install glfw3 glew</li>

 <li>GLM you can directly add it to include header path 2: XCode:</li>

 <li>Add /usr/local/include in header path</li>

 <li>Add /usr/local/glew/2.0.0/lib /usr/local/Cellar/glfw/3.2.1/lib in library path 3: Add link binary libraries</li>

 <li>3.2.dylib libGLEW.2.0.0.dylib OpenGL framework</li>

</ul>

(If you are facing the “GLFW Fails to Open Window in OSX error”(This is one error I face during compilation), add glfwWindowHint(GLFW_OPENGL_FORWARD_COMPAT, GL_TRUE);) (http://stackoverflow.com/questions/22887922/glfw-fails-to-open-window-inosx)

4: Run code

Linux (ubuntu):

1: Install using apt-get

<ul>

 <li>$ sudo apt-get install libglew-dev libglfw3-dev libglm-dev 2: Compile</li>

 <li>$ sudo g++ -o helloworld helloworld.cpp -std=c++11 -lGL -lglfw -lGLEW 3: Run code</li>

</ul>


