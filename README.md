# Scenemaker
Scenemaker is an edited version of Valve's Faсeposer. 

It includes several bugfixes, some workflow adjustments, a bit of extra convenience. Nothing drastic, but it can make working on scenes a bit better.

## Installation
Unpack the release .ZIP into your Source game's root\bin folder, where hlfaceposer.exe should already exist. The only files it should ask to overwrite, if any, is the lipsync data files in the root\bin\lipsinc_data folder, that should only be present if you already installed a fix for Faceposer from the VDC; the files would then be identical so you can either skip or overwrite them.

Create the shortcut for scenemaker.exe with the extra launch parameter -game [full path to your sourcemod]; wrap the path in quotation marks if it contains spaces. 

If desired, you can also add -olddialogs option after that so you can browse for actor models using the standard Explorer window.

## Full changelog for version 1.7.6:
Fixes:
- Fixed broken wireframe rendering for the model's bones;
- Disabled model IK to prevent rendering of broken IK helpers - this and broken wireframe was causing framerate drop and sound lags;
- Restored/fixed Smoothshaded model view;
- Fixed the missing lipsync API (now packed with the program) and made it the default choice (the old default only works on Win XP);
- Fixed the Delete key behavior for audio events (needing to click on empty space before clicking on the event to allow deletion);
- Fixed missing UI icons or needing to pack them in the mod folder, now they are packed with the program;

New features and changes:
- The curve type in curve-based tools can be assigned via a context menu; previously, this ability was tied solely to 0-9 hotkeys without any tooltips;
- The model rendering was brought closer to the HLMV, with more rendering choices (smoothshaded, bone weights, bad vertex data, UV), wireframe overlay, viewing attachments and collision model;
- New -olddialogs command line option enables browsing for models in a usual Explorer browser instead of Steam's in-VPK browser (that requires unpacking models to work). Previously, -nosteamdialog already allowed this; the new command merely brings it on par with HLMV, which also has that option;
- By default, loops now have the infinite number of loops set (-1) instead of the default being 0 (never looping);
- "Go to Homepage" Help menu option was renamed to "Open VDC website (Wiki)";
- A few deprecated/irrelevant menu options have been hidden, such as picking the ground texture;
- Custom icon, About window and different background colour of the program's window;

## Compatibility
Scenemaker is forked from the regular Faceposer for HL2/SDK 2013. It most likely cannot work with games that are newer, such as Portal 2, however, given that the VCD format hasn't changed since before HL2 released, you should be able to make scenes for them under HL2/SDK with models ported over. There's no way for me to make a fork of Scenemaker for different games, so I'll leave these experiments up to you.
