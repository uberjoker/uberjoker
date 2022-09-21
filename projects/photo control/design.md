## Photo Control

A utility to import photos from any device (camera, USB stick etc), maintain a master of unmodified originals, a set of originals with any modifications or edits and a projects organiser.

### Key features:
- Import from devices
- Create a backup of all imports (master)
- Organise/add photos to different projects (without creating copies)
- Retrieve original as needed (without affecting original)
- UI (Graphical / command line based)

### Things to do to implement:
- Import i.e. copy photos from a USB source (Read RAW, JPEG, PNG etc.)
- Create an edit master and a backup master (i.e. two sets of copies. Backup master location is predefined in config)
- Each import is done to a new folder with name *#Import<datetimestamp>**
- Each import is first tagged to a default project called #PCWaiting. On the PCWaiting screen, photos can be organised into final projects. 
- Photos may remain in PCWaiting indefinitely.
- Each project is a folder
- Each project folder has soft links to actual image that is in the masters folder
- When photos are moved out of one project to another (or from PCWaiting to another project), links are deleted from source project's folder and added to the destination project's folder
