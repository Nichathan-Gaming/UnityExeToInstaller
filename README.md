# UnityExeToInstaller

This repository contains my tutorial describing how to convert a Unity Windows Build into an installable exe file.

## Disclaimer

The instructions given in this tutorial are the instructions used at Nichathan Gaming. We do not guarantee that they will work for you nor do we guarantee that they will provide the same output as we receive. We sincerely hope that this tutorial helps out small developers but we urge people to use it at their own discretion. 

## Instructions
*Convert playable .exe to installable .exe*

0. Download and install the [Inno Setup Compiler](https://jrsoftware.org/isdl.php)

1. Start up Inno Setup Script Wizard

2. Under `New File` select `Create a new script file using the script wizard`

3. Click `OK`

![Progress00](https://user-images.githubusercontent.com/103794085/212016663-3f68aa1c-e962-48ed-9384-bf975376a484.png)

*Do not select `Create a new empty script file`*

4. Click `Next`

![Progress01](https://user-images.githubusercontent.com/103794085/212012509-c94311e2-5f00-452f-a586-48b856effa69.png)

5. Provide the application information

6. Click `Next`

![Progress02](https://user-images.githubusercontent.com/103794085/212012819-c11b5669-09ca-47ff-93e3-bafeaea4bb2e.png)

*You do not have to change anything on this screen*

7. Click `Next`

![Progress03](https://user-images.githubusercontent.com/103794085/212013107-a46a5b61-d30f-424f-952f-0e85725a791c.png)

8. Click Add File(s)

9. Select your loose files in the `Build` folder.

*Do not select the folders yet*

10. Click `Open`

![Progress04](https://user-images.githubusercontent.com/103794085/212013608-bce8bfb3-81a4-4319-840f-62ea9ef2fe21.png)

11. In your file explorer, navigate to your `Build` folder and in the `MonoBleedingEdge` and `Game_Data` folders, create a subfolder with the same name as the folder.

![Progress05](https://user-images.githubusercontent.com/103794085/212014503-a69ba135-25e9-48a3-8fb9-ac8c59ba7f71.png)
![Progress06](https://user-images.githubusercontent.com/103794085/212014606-9c7eac91-3b34-451c-805e-17f1c290774a.png)

12. Drag and place all files and folders into the new subfolders

![Progress07](https://user-images.githubusercontent.com/103794085/212014922-a3c28721-0b8d-4198-8a9f-b0b7ecdd82f6.png)
![Progress08](https://user-images.githubusercontent.com/103794085/212014975-232910ab-881d-4028-a69f-b265c44c7174.png)

![Progress09](https://user-images.githubusercontent.com/103794085/212014796-363fe587-29f1-43d4-a8fa-e0889d09cc19.png)
![Progress10](https://user-images.githubusercontent.com/103794085/212014852-93ec4680-1f43-4fb5-bbc2-705ba84c9430.png)

13. Back in the Inno Setup Script Wizard, select `Add folder`

14. Locate and add the parent `MonoBleedingEdge` folder

![Progress11](https://user-images.githubusercontent.com/103794085/212015674-7f16c369-55c5-442f-afa2-648b77eebafe.png)

15. When asked if files in subfolders should also be included, click `Yes`

![Progress12](https://user-images.githubusercontent.com/103794085/212016039-0d64f874-9bbc-43e2-b56e-22a2ec67a4f9.png)

16. Repeat steps `13`, `14` and `15` to add the parent `Game_Data` folder.

*Your `Inno Setup Script Wizard` should now look like the image below.*

![Progress13](https://user-images.githubusercontent.com/103794085/212016862-b8812db5-9383-4aea-8f9c-34febf8f8bfd.png)

17. Click `Next`

*You do not have to change anything on this screen*

![Progress14](https://user-images.githubusercontent.com/103794085/212017120-a956b359-4dcf-4274-a216-9ed7841f2501.png)

18. Click `Next`

*You do not have to change anything on this screen*

![Progress15](https://user-images.githubusercontent.com/103794085/212017270-eb348490-f10e-4682-a10b-8c9ab7143fd7.png)

19. Click `Next`

20. **Optional** Add License files or information

![Progress16](https://user-images.githubusercontent.com/103794085/212017467-715bd5ef-2d5c-4f49-92ec-1a5b3735a378.png)

21. Click `Next`

22. select `Administrative install mode`

23. select `Ask the user to choose the install mode at startup`

24. Click `Next`

![Progress17](https://user-images.githubusercontent.com/103794085/212017699-9a3ed0e8-52ae-4a7e-ab19-d1b3237951e5.png)

25. Select the language(s) of the program

26. Click `Next`

![Progress18](https://user-images.githubusercontent.com/103794085/212017773-b5cbcea5-317d-4d2b-80f6-b3dbcdaf802a.png)

27. **Optional** Select where this installer will be generated *Default location is to create an `Output` folder in this `Build` folder*

28. Select the file name and icon *Icon must be in an icon file format such as `.ico`. There are many free websites to convert an [image to an icon](https://convertio.co/jpg-ico/)*

29. **Optional** Set a password required to run the executable if desired

30. Click `Next`

![Progress19](https://user-images.githubusercontent.com/103794085/212018794-8cc1775d-bd91-4c3d-922b-f268c110cd79.png)

*You do not have to change anything on this screen*

![Progress20](https://user-images.githubusercontent.com/103794085/212018965-be4afc85-d381-4a26-84ba-4878c0f80475.png)

31. Click `Next`

32. Click `Finish`

![Progress21](https://user-images.githubusercontent.com/103794085/212019100-cd07e029-4891-419d-89f6-3823b7cc34d8.png)

33. Select `Yes` for `Would you like to compile the new script now?`

![Progress22](https://user-images.githubusercontent.com/103794085/212019224-ea5831cc-070b-4d59-89d9-7f3595c966f9.png)

34. Select `Yes` to `save the script before compiling`

![Progress23](https://user-images.githubusercontent.com/103794085/212019367-4add650f-08dc-40b5-b7a5-7ec36df97544.png)

35. Save the installer script anywhere you wish so it can be edited later.

## Running the Installer

1. The installer executable file can be found wherever you saved it in step `27`. If you did not change the default location, then it will be in an Output folder:

![Progress24](https://user-images.githubusercontent.com/103794085/212020564-b439f13b-4362-4ef4-857d-bd9209ca2633.png)

2. Run the installer by `double clicking` it, or `right click` it and select `open`

3. Choose to `Install for all users` or *just for the currently signed in user* `Install for me only`

![Progress25](https://user-images.githubusercontent.com/103794085/212021064-72d41a51-f5b8-4b49-adbf-f2eaea066c32.png)

4. Give permission to install the application *If `Install for all users` was selected*

5. Select a destination location *or leave at the default values*

6. Click `Next`

![Progress26](https://user-images.githubusercontent.com/103794085/212021369-d0d16db4-c61e-4054-bd94-66db8d9704e9.png)

7. Select the checkbox to add a desktop shortcut if you wish

8. Click `Next`

![Progress27](https://user-images.githubusercontent.com/103794085/212021555-1a33d843-ab05-4686-8e24-31bf245ddec9.png)

9. Review the information, then click `Install`

![Progress28](https://user-images.githubusercontent.com/103794085/212021693-a13af19b-6847-47a0-a6c6-ad6322ba4375.png)

10. Wait a moment as files are extracted and installed

![Progress29](https://user-images.githubusercontent.com/103794085/212021775-5ea3d9d6-f2d4-49bd-9894-ad755de514b4.png)

11. Click the checkbox to launch the app right away or not, the click `Finish`

![Progress30](https://user-images.githubusercontent.com/103794085/212021964-6d2d8af2-f946-4854-bc7e-2223cd675ee3.png)

12. Enjoy the application

## Removing an application installed in this manner

1. Open Control Panel, select `Uninstall a program`

![Progress31](https://user-images.githubusercontent.com/103794085/212022592-0c836cf9-7d07-4348-9677-28c5b7c930d6.png)

2. Find your application, select it then click uninstall

![Progress32](https://user-images.githubusercontent.com/103794085/212022499-3f58479b-f028-42d0-bdaa-976ef47ed350.png)

3. Verify that you wish to uninstall it and wait a moment. A restart may be required to fully remove some applications.
