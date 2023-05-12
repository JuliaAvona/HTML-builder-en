## Build css bundle

In the **index.js** file of the **05-merge-styles** directory, write a script that collects the contents of the **styles** folder into a single file. The output file must be named **bundle.css** and located inside the **project-dist** folder.

### Requirements

- [ ] After the script is finished, the **project-dist** folder should contain the **bundle.css** file containing styles from all the files in the **styles** folder.
- [ ] When adding/removing/changing style files in the **styles** folder and running the script again, the **bundle.css** file is overwritten and contains the actual styles.
- [ ] Any files with extension other than **css** or directories are ignored.
- [ ] Styles found in the **bundle.css** file created during the build process must not be corrupted.

### Task objectives

- Learn to combine information from multiple files with one extension.

### Folder contents:
Please note that inside **05-merge-styles** there is a **test-files** folder designed to test the task and interaction with it is not expected during the solution of the task.
### Description

Possible order of actions to complete the task:

1. Import all required modules
3. Reading the contents of the **styles** folder
4. Checking if the object is a file and if the file has the correct extension
4. Reading the style file
5. Writing the read data to an array
6. Write array of styles to **bundle.css** file

For a visual effect of your script, I recommend installing the [Live Server] extension in vscode (https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) and using it to run the **index.html** file located in the directory **project dist**.
