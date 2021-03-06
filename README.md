# WiseDownload

## Executive summary
WiseDownload is a Chrome extension that prevents users from downloading undesired files. In order to achieve this goal, WiseDownload asks the user for the type of file they wish to download, and verified the given file extension.

## Technical details
In the code, the *rules* map between a file type, e.g., an image, a document, etc., and their possible extensions. When WiseDownload starts, the *rules* dictionary is initialized and used throughout the whole code.
When a user selects the type of the file they are downloading, its extension is compared to the extensions corresponding to the selected type. The file is downloaded safely only if there is a match.

### Used frameworks
 * [jQuery](https://jquery.com/)
 * [bootstrap](http://getbootstrap.com/)

## Files
 * bg.js - the background script that is loaded into each tab. It loads all the other scripts and style file, initializes the rules, creates and handles listeners, and calls the relevant function when a listener is triggered.
 * popup_ui.js - responsible for generating the "popup" (see the figure below) that a user sees when a download is initiated. Please note that this file is not responsible for any BL, as it all happens in bg.js. 
 * helper.js - contains various UI-related utils functions.

![The user is queried regarding the type of the file he/she is downloading](/demo_img.jpg?raw=true "The user is queried regarding the type of the file he/she is downloading")

## TODOs
 * Create a separate JSON file for the rules
