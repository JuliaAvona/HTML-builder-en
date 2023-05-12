## Copy folder

In the **index.js** file of the **04-copy-directory** directory, implement the **copyDir** function that copies the contents of the **files** folder to the **files-copy** folder.

### General rules:

- It is forbidden to use any third-party modules
- Each of the jobs must be run with the command node <job folder name> executed in the root directory
- It is forbidden to use fs module synchronous functions such as ```fs.statSync(path[, options])```,
```fs.readFileSync(path[, options])``` and others under [synchronous API](https://nodejs.org/api/fs.html#fs_synchronous_api)


### Requirements
- [ ] After the function ends, the **files-copy** folder is created, the contents of which are an exact copy of the original **files** folder.
- [ ] When adding/removing/changing files in the **files** folder and restarting ```node 04-copy-directory```, the contents of the **files-copy** folder are updated.
- [ ] Do not use fsPromises.cp()

### Task objectives

- Learn to copy files and directories.

### Description

The procedure for completing the task:

1. Import all required modules
2. Create folder **files-copy** if it doesn't exist yet
3. Reading the contents of the **files** folder
4. Copying files from the **files** folder to the **files-copy** folder

### Adviсe

Note the ```recursive``` option that can be passed to ```fsPromises/mkdir```. With it, you can avoid errors in cases where the directory has already been created.

##### Useful links

- [copyFile](https://nodejs.org/api/fs.html#fs_fspromises_copyfile_src_dest_mode)
- [mkdir](https://nodejs.org/api/fs.html#fs_fspromises_mkdir_path_options)
