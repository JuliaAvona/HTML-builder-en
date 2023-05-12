## Display information about files stored in a folder

In the **index.js** file of the **03-files-in-folder** directory, write a script that outputs data about the files contained in the **secret-folder** folder to the console.

### Requirements

- [ ] When executing the command ```node 03-files-in-folder``` in the root directory of the repository, information about the files contained directly inside ***03-files-in-folder/secret-folder*** is displayed in the console . The data should be output in the format <file name>-<file extension>-<file weight>. Example: ```example - txt - 128.369kb``` (no need to round, convert to kb optional!)
- [ ] Information should be displayed only for files contained in ***03-files-in-folder/secret-folder***. The presence of information about directories is considered an error.


### Task objectives

- Learn to get information about files.

### Description

The procedure for completing the task:

1. Import all required modules
2. Reading the contents of the secret-folder
3. Getting data about each object that contains the secret-folder
4. Checking if an object is a file
5. Outputting file data to the console

### Adviсe

Check out [this article](https://www.freecodecamp.org/news/what-is-gitkeep/) to fill in any gaps in your understanding of how git works and get rid of the question of reading files in subfolders.

To read the contents of a folder, use the ```readdir``` function from the module "fs/promises"([link to documentation](https://nodejs.org/dist/latest-v16.x/docs/api /fs.html#fs_fspromises_readdir_path_options)). This function will allow you to get the names of all files in a given directory.

After reading the contents of the folder, if you set the ```{withFileTypes: true}``` option, each object contained in it will be represented as an instance of the [Dirent] class (https://nodejs.org/dist/latest- v16.x/docs/api/fs.html#fs_class_fs_dirent). Its methods will let you know if an object is a file.

You can use the ```extname``` method of the "path" module to determine the file extension. [Documentation](https://nodejs.org/api/path.html#path_path_extname_path)

[stat](https://nodejs.org/dist/latest-v16.x/docs/api/fs.html#fs_fs_stat_path_options_callback) will help you get information about the file.
You can see the full list of data returned by this function in the documentation. Please note that the object returned by this function is an instance of the [Stats] class (https://nodejs.org/dist/latest-v16.x/docs/api/fs.html#fs_class_fs_stats), which also has methods that allow you to check whether whether the object is a file.

##### Useful links
*Please note that translations of the documentation into Russian may be outdated and may not contain all the modern features of the modules. However, the basic concepts described there still work today. Always refer to the official documentation for up-to-date information!*

- [stat in Russian (nodejsdev.ru)](https://nodejsdev.ru/api/fs/#fsstat)
- [readdir in Russian (nodejsdev.ru)](https://nodejsdev.ru/api/fs/#fsreaddir)
- [Stats in Russian (nodejsdev.ru)](https://nodejsdev.ru/api/fs/#fsstats)
