## Assembling an HTML page from components and styles

In the **index.js** file of the **06-build-page** directory, write a script that:
1. Creates a folder **project-dist**.
2. Replaces template tags in the **template.html** file with file names from the components folder (example:```{section}}```) with the content of the components of the same name and saves the result in **project-dist/index .html**.
3. Collects the styles from the **styles** folder into a single file and places them in the **project-dist/style.css** file.
4. Copies the **assets** folder to **project-dist/assets**


### General rules:

- It is forbidden to use any third-party modules
- Each of the jobs must be run with the command node <job folder name> executed in the root directory
- It is forbidden to use fs module synchronous functions such as ```fs.statSync(path[, options])```,
```fs.readFileSync(path[, options])``` and others under [synchronous API](https://nodejs.org/api/fs.html#fs_synchronous_api)

### Requirements
- [ ] After the script ends, the **project-dist** folder should be created
- [ ] **project-dist** folder should contain **index.html** and **style.css** files
- [ ] The **project-dist** folder should contain an **assets** folder which is an exact copy of the **assets** folder found in **06-build-page**
- [ ] Do not use fsPromises.cp()
- [ ] The **index.html** file must contain the markup resulting from replacing the template tags in the **template.html** file
- [ ] The **style.css** file must contain styles collected from the files of the **styles** folder
- [ ] When adding a component to the folder and the corresponding tag to the **template.html** source file, re-executing the script will bring the **index.html** file in the **project-dist** folder up to date by overwriting it. The **style.css** file and **assets** folder must also be kept up to date
- [ ] When writing two or more template tags in a row in the **template.html** file, separated by spaces only **without line breaks**, no code execution errors should occur. For example, `{{about}} {{articles}}` should be treated as 2 separate components
- [ ] The source file **template.html** must not be changed during script execution
- [ ] It is an error to write any files except files with **.html** extension to the template
### Task objectives

- Creation of a small utility that allows you to assemble a static HTML page.
- Consolidation of acquired knowledge

### Description

One of the possible order of task execution:

1. Import all required modules
2. Reading and saving in a template file variable
3. Finding all tag names in a template file
4. Replacing template tags with the contents of component files
5. Writing the modified template to the **index.html** file in the **project-dist** folder
6. Use the script written in the **05-merge-styles** task to create the **style.css** file
7. Use the script from the **04-copy-directory** task to move the **assets** folder to the project-dist folder

Please note that you can optimize and change this algorithm at your discretion.
