<img align="left" width="100" height="100" alt="Profil2_sym_100" src="https://github.com/user-attachments/assets/eb732e26-5008-46cd-989b-152fb5f8683b" />

# GodotSampleGDExtension
Sample Godot Project with C++ dll (GDExtension) with Visual Studio debugging.

## Content
This sample project follows the sample page from Godot Engine documentation here:
https://docs.godotengine.org/en/4.4/tutorials/scripting/gdextension/gdextension_cpp_example.html

- godot folder contains the godot project
- code folder contains the C++ code.

## Open in Visual Studio
#### Requirement: Visual Studio installed with "Desktop deveopment in C++" workload.
https://visualstudio.microsoft.com/fr/downloads/
#### Requirement: Godot installed 

To open it in Visual Studio, chose "Open a Local Folder" and select the **code folder**.
After opening, CMAKE should generate the proper build scripts (you can see it in Output)

## Troubleshooting
-If the Build menu remains empty in VS, close and reopen visual studio.

-If you debug and get this message from godot: "**Couldn't detect whether to run the editor, the project manager or a specific project. Aborting.**", launch the Edit target instead of Debug, then press play in the Godot Editor. After that, Debug target will work.

## Build and debug
When building, it first retrieves and compiles godot-cpp versioin 4.4 (to change this, edit CMakLists.txt)
#### Important: you need to edit the launch.vs.json file to set the "exe" paths to your godot executables.
The compiled dll is then copied to godot/bin where library.gdextension tells Godot about it

Build the x64-Debug version of the dll to debug, and select Debug debug target to launch and debug the godot project directly.
Select Edit debug target to launch the godot editor. To debug while the editor is launched you will need to attach manually to the running project.

Build the x64-Release version of the dll to export the godot project (then you should uncheck debug in godot export)

## Rename project
To rename the project
- close VS
- delete .vs folder in code
- delete out folder in code
- delete bin folder in godot
- rename top folder
- open code folder in VS
- get a well-deserved toast

  
  



