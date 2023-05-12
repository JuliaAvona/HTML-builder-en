#HTML builder
---

### Goals:

In this series of tasks, the main goal is to understand the basics of working with the Node.js platform.
You are invited to complete a series of small tasks with a gradual increase in difficulty. The final touch will be the creation of a small application for assembling a static site.

Please note that most tasks can be done in several ways and at this stage there are no wrong ones. Only the performance of your code and the fulfillment of the set conditions are evaluated.

---

## Execution process:
- Fork the repository
- Submit the link to the repository in crosscheck-submit
- Clone the repository
- Run ```npm install``` to install eslint and node.js typings to help you with your tasks
- Complete tasks. The TOR for each of them is located in the README.md file inside the task folder
- Push the solution to your fork repository

##crosscheck
 
The verification progress is described in the repository wiki. After starting cross-check, go to [github.com/EvgeniiMal/HTML-builder/wiki/HTML-builder-crosscheck] and follow the instructions on the main page.

## General rules!!!:

- When solving problems, it is forbidden to use any third-party modules
- Each of the jobs must be run with the command node <job folder name> executed in the root directory
- It is forbidden to use fs module synchronous functions such as ```fs.statSync(path[, options])```,
```fs.readFileSync(path[, options])``` and others under [synchronous API](https://nodejs.org/api/fs.html#fs_synchronous_api)
- It is forbidden to use the setTimeout() timer
- Execution and verification of the task must be carried out on node LTS version .

## Table of contents
[01 Reading a file with output to the console](https://github.com/EvgeniiMal/HTML-builder/tree/main/01-read-file)  
[02 Write console input to file](https://github.com/EvgeniiMal/HTML-builder/blob/main/02-write-file)  
[03 Displaying information about files stored in a folder](https://github.com/EvgeniiMal/HTML-builder/blob/main/03-files-in-folder)  
[04 Folder Copy](https://github.com/EvgeniiMal/HTML-builder/tree/main/04-copy-directory)  
[05 Build css bundle](https://github.com/EvgeniiMal/HTML-builder/blob/main/05-merge-styles)  
[06 Building an HTML page from components and styles](https://github.com/EvgeniiMal/HTML-builder/tree/main/06-build-page)  
