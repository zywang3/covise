Instructions for ExaBrick Plugin:

Detailed explanations on what this plugin does and how are described in my master thesis "Real-Time Rendering of Large AMR Data in Virtual Reality Environments" August 2023. Files described in this thesis and those you might need to rebuild the plugin can be found in the folder ExaBrickPlugin in this COVISE fork.  

To build ExaBrick Plugin in src/OpenCOVER/plugins/ukoeln/ExaBrick, you need to do the following steps:

1. Build owlExaBrick locally on your device from https://github.com/owl-project/owlExaBrick#create-exa-file-and-run-viewer

2. Link your owlExaBrick into the 3rdparty folder in COVISE

3. The UseExaBrick.cmake file (from folder ExaBrickPlugin) contains configuration directives that ensure proper linkage and access to the necessary ExaBrick libraries, it need to be added into covise/cmake/Using/UseExaBrick.cmake

4. Build the ExaBrick folder with "ADD_SUBDIRECTORY(ExaBrick)" in src/OpenCOVER/plugins/ukoeln/CMakeLists.txt

5. Use the configuration data in folder ExaBrickPlugin to start OpenCOVER, data for plugin to load need to be in .exa format with .cells and .scalar data for the AMR data in the same directory, as well as the .xf transferfunction, which can be generated using exaViewer of ExaBrick frmework. How to convert AMR data into ExaBrick data structure is described in https://github.com/owl-project/owlExaBrick#create-exa-file-and-run-viewer
