# READ ME

## Instructions to run Project.
It is necessary to use Python and Unity (2021.3.40f1 versión was used but versión 2021.3.24f1 and close versions also work). 
It is also necessary to pip install mediapipe.

1. Open the unity proyect and add the CalibrationScene from folder "scenes" to Hierarchy.
2. In Windows PowerShell or cmd terminal run main.py using Python.
3. Run the Unity project.
--------------------------------------------------------------------------

## Instructions to import a SMPL, SMPL-X or other 3D model to the proyect
1. Download model from oficial website.
2. Inside the Unity project window, search for the source of model (mesh/model)
3. Modify the following in the isnpector window (only fo SMPL and SMPL-X models)
    - Import Blendshapes: On
    - Mesh Compression: On
    - Read/Write:Enable
    - Optimize Mesh: Off
    - Keep Quads: Off
    - Weld Vertices: Off
    - Normals: Calculate
    - Smoothing Angle: 180
    - Tangents: None
    - Click on "Apply"
    Inside tab "Rig" -> Animation Type: Humanoid
4. In the tab " Rig" click on Configure...
5. Copy model (first element on the list in the left).
6. Paste in Hierarchy of the proyect.
7. In Inspector add componente: Avatar (script).
8. Add Preview Camera (Main camera) and Animator (model).
9. Resize model and adjust it in Game Scene.
---------------------------------------------------------------------------

## Instructions for calibration
1. Run main and Unity project. Press "C" and copy pose.
2. One done, DO NOT stop the project, just pause and click "Store to New Calibration Data".
3. Stop the project and add the model in Calibration Data.
4. Enable "use calibration data".
5. Ready tu run.
---------------------------------------------------------------------------

## For other 3D models
If you wanted to use other 3D models:
1. The humanoid avatar must be rigged for animation and configured as humanoid in the Unity Rig import settings. Also, the following bones are required: Upper Arm -> Hand, Upper Leg -> Foot, Hips -> Chest, Neck -> Head. Most humanoid avatars will have this by default.
2. The resting pose of the avatar should be a T-pose.
3. Add the Avatar script to the GameObject and correctly assign all the fields.
----------------------------------------------------------------------------


## Useful links
This video can help a lot with the import of new models and calibration process. Step by step:
https://www.youtube.com/watch?v=DFHDnALoiQE
Github of original base project: https://github.com/ganeshsar/UnityPythonMediaPipeAvatar