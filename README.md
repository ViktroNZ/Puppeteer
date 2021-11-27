# Puppeteer
A UE5 plugin for improving the Metahuman ARKit face tracking.

It includes a UI which allows you to set the Minimum and Maximum range of a given ARKit input. It also includes a small amount of smoothing to minimise noise and makes inferences from ARKit blendshapes to drive additional Metahuman rig controls.

There is still a lot of room for improvement - particularly around smoothing and inference of rig control values. 

This was built as a short experimental side project.

# Installation instructions
0. Open your UE5 project and enable the Apple ARKit Face Support plugin and LiveLink plugin if it isn't enabled already. You'll need to do this before enabling Puppeteer otherwise Puppeteer will have compile issues as it'll be missing a LiveLink node.
1. Download the files for this plugin by clicking "Code" in the GitHub interface and then clicking "Download Zip"
2. Place this in your `../[ProjectName]/Plugins/` folder. You may need to create the "Plugins" folder
4. Open the project in UE5 and enable the Puppeteer plugin in Plugins window. You can find this in the /Edit/Plugins file menu and searching "Puppeteer"
4. Import a Metahuman into the project. If you haven't done this before, YouTube has some great videos on how to do this
5. In the Content browser, open the "Puppeteer Content" folder and open the "Main_Level". You can use your own level, but this one is a good starting point
6. Select the `Puppeteer_Actor` in the World Outliner and set the `Metahuman Actor Class` to the blueprint actor of your new Metahuman. You'll find it's called something like "BP_[Metahuman Name]"
7. Open up the LiveLink Face App on your phone, get the Live Link subject name (it's at the bottom of the iPhone app screen) and type that into the `Live Link Subject` Name field of the `Puppeteer_Actor`
8. With the LiveLink Face App running on your phone, press Play. Hopefully it should all be working!
9. Press 1 to toggle the Puppeteer UI