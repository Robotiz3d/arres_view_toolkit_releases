## v0.4.3 (2025-04-01)

### Fix

- add loading cursor when toggling defect bounding box annotations

## v0.4.2 (2025-04-01)

### Fix

- clear all appropriate caches after QA/QA review to reload defects that have been deleted/restored

## v0.4.1 (2025-03-27)

### Fix

- fixed confirm_review() params and naming (qa -> review) for review

## v0.4.0 (2025-03-27)

### Feat

- added QA review page and features to restore deleted defects

## v0.3.0 (2025-03-25)

### Feat

- added feature to toggle bounding box annotations for defects
- added time to finish concurrent tasks
- view full job from job info page

### Fix

- replaced duplicated shortcut key for favourating images
- actually delete job from job list page instead of just printing message
- improved tqdm progress bar display
- updated loading cursor logic to be more adaptable for different uses
- corrects instantiation of empty list if no paths to delete in qa

### Refactor

- easier to manage cache sizes
- created decorator to handle all functions which change cursor to loading and back

## v0.2.0 (2025-02-27)

### Feat

- added tqdm progress bar in console and file logs for long runnin background tasks
- added util to run expensive/long api tasks concurrently in background
- added api endpoints for getting asset IDs from defect/path locations

### Fix

- automatic build releases to public repo Robotiz3d/arres_view_toolkit_releases

## v0.1.5 (2025-02-20)

## v0.1.4 (2025-02-20)

### Fix

- create release from github actions build

## v0.1.3 (2025-02-20)

### Fix

- updated help dialog

## v0.1.2 (2025-02-20)

### Feat

- added job delete option in job info for admin users
- added selection options to job list page to batch delete jobs or download logs
- buffer data from api using parallel threads for >10x speedup
- added option to change assigned client in job detail page
- added defect distribution page
- added option to download job logs on job detail page
- added scrollbar to defect checkboxes for qa
- added defect highlighting on right click and required api calls
- added reusable filter components on on job list page
- global keybinds now managed by WindowManager
- build macos nuitka binary
- added logs when viewing job paths, synced to current selected path
- added option to only qa paths containing defects. select from job list
- added counter to deleting paths
- abstracted map tile server selection and added option to coverage map page
- changed the path filter to use index instead of id
- major improvements to review tools
- major updates to add QA features
- added scars api integration
- added path and defect delete endpoints
- added cropping paths and sending deleted path requests to server
- added birds eye view page
- added route coverage map page
- added auto playback play/pause and speed options
- added option to select map tile server
- add keybind to show help dialog
- check for new updates and notify user if there are any
- show feedback when clicking on mini map to select path
- changed job list to use treeview, exponentially faster
- added autoplay and starring paths
- fully migrated to new API
- click on minimap to jump to path
- QoL improvements in map
- added data (path/defect) export to csv
- major updates. path list is now tree view, much faster, better shortcuts, etc.
- added login page
- added more keyboard shortcuts
- complete redesign of job path page
- added bunch of apis for getting images and defect data
- added left/right arrow keybinds for scrolling images
- fixed keybinds, fixed ai image, added image saving

### Fix

- updated icons for all messageboxes to be appropriate to message
- show all jobs under QA accounts for QA admin
- updated prev/next path keyboard shortcuts to f/h
- increased ttl cache timeouts
- updated image cache timeout to 15 mins
- fixed dropdown if no jobs for user
- fixed checking if running interpreted or nuitka compiled
- skip copying credentials file when running compiled as it is handled by nuitka build
- added watch cursors when loading job detail and qa pages
- added prefs.template to be copied and converted to prefs.ini for nuitka build
- add user section with username and password when creating prefs.ini
- pass secrets as args to scripts
- corrected moved script filepaths
- include each credential setup script only for appropriate os
- inject credentials appropraitely per os during nuitka build
- improve how credentials are stored and injected into nuitka build
- fixed artifact path to upload
- fixed artifact path to upload
- improved nuitka build action and now runs on all OSes
- disable caching on github actions
- file name follows macos convention
- removed gitignored files from nuitka build
- fixed setup and credentials imports
- fixed loop counter when cropping paths
- fixed path/defect qa selection logic. remembers states if qa is cancelled
- removed SystemButtonFace and replaced with default colour for cross platform compatibility
- continue with qa confirmation even if error from api and highlight errors in red
- fixed close button logic on qa dialog to be cross platform compatible
- improvements to coverage map page
- change wait cursor to watch for cross platform compatibility
- improvements to skipping defect free chunks
- handle errors when cropping paths
- sort paths after qa to retain order
- corrected path index calculation after qa has been finished
- if the current id is not found after qa, reset to 0
- fixed bugs when selecting and deselecting paths and defects
feat: added option to skip empty paths
fix: improved refresh of job when completing qa
and more...
- updated scars UpdateDefectQA endpoint to take a dict of defects and their manualcheck values
- clear path segmap cache so deleted defects are not shown
- added scars username/password fields
- added job id to show paths window
- get_paths etc. now use internal class methods and increased cache size for some routes
- resize images before showing in separate image window
- set dynamic max zoom based on limits of map tile provider
- improved global keybinds
- bind just 'q' key instead of all keys and code cleanup
- show segmentation image by default
- fixed shortcut to close main window
- dialog boxes now pop up on current window
- updated for python 3.8

### Refactor

- improve imports in components module
- major refactor including datashare cache and components
- refresh time is no longer magic number
- separate login component from ssh to abstract the logic
- moved common mapping functions to map_utils
- access datashare from controller instead of passing it to each object
- moved map funcs to map_utils
- removes ssh from map and JobPage as API handles all of it now
