## Write console input to a file

In the **index.js** file of the **02-write-file** directory, write a script that prints a greeting to the console, waits for text input, and writes the entered text to a file.


### General rules:

- It is forbidden to use any third-party modules
- Each of the jobs must be run with the command node <job folder name> executed in the root directory
- It is forbidden to use fs module synchronous functions such as ```fs.statSync(path[, options])```,
```fs.readFileSync(path[, options])``` and others under [synchronous API](https://nodejs.org/api/fs.html#fs_synchronous_api)

### Requirements

- [ ] Inside the folder 02-write-file there is 1 file **index.js**
- [ ] When executing the command ```node 02-write-file```, a text file is created in the folder ```02-write-file```, and a text prompt is displayed in the console (Your choice)
- [ ] After entering text in the ```02-write-file``` directory, the entered text must be written to the file created earlier. The process does not terminate and waits for new input.
- [ ] After the next input, the initially created text file is supplemented with new text, the process continues to wait for input.
- [ ] Pressing ```ctrl + c``` or typing ```exit``` prints a farewell phrase to the console and terminates the process.


### Task objectives
- Strengthen understanding of the basics of how events and threads work in Node.js
- Working with the global process object

### Description
In this task, you will write a program that reads your console input until the process is forced to exit ```ctrl + c``` or the **exit** keyword is entered. The procedure for completing the task:
1. Import all required modules.
2. Creating a write stream to a text file
3. Outputting a welcome message to the console
4. Waiting for user input, then checking the input for the presence of the keyword **exit**
5. Writing text to a file
6. Waiting for further input
7. Implementation of a farewell message when the process stops

### Adviсe

To successfully complete this task, you will need the knowledge of events and threads acquired earlier, and you should also explore the capabilities of the global process object. Using its events, you can, among other things, intercept signals sent to the process, for example, when you press ``` ctrl + c```.

To read something from a stream line at a time, the Readline module can help you. The standard input stream stdin being a ReadbleStream is great for this.

##### Useful links
*Please note that translations of the documentation into Russian may be outdated and may not contain all the modern features of the modules. However, the basic concepts described there still work today. Always refer to the official documentation for up-to-date information!*
- Process:
     - [Process](https://nodejs.org/api/process.html)
     - [Process translation in Russian (nodejsdev.ru)](https://nodejsdev.ru/api/process/)
     - [Signal events](https://nodejs.org/api/process.html#process_signal_events)
     - [Signal events (nodejsdev.ru)](https://nodejsdev.ru/api/process/#signal-events)
- Readline:
     - [Readline](https://nodejs.org/api/readline.html)
     - [Readline in Russian (nodejsdev.ru)](https://nodejsdev.ru/api/readline/)
- Events:
     - [Metanit Events](https://metanit.com/web/nodejs/2.9.php)
     - [Understanding Node.js Event-Driven Architecture (FreeCodeCamp)](https://www.freecodecamp.org/news/understanding-node-js-event-driven-architecture-223292fcbc2d/)
     - [Event emitter](https://nodejs.dev/learn/the-nodejs-event-emitter)
     - [Translation of documentation Events (nodejsdev.ru)](https://nodejsdev.ru/api/events/)
     - [Events guide (nodejsdev.ru)](https://nodejsdev.ru/guide/events/)
- Streams:
     - [Stream](https://nodejs.org/api/stream.html)
     - [fs.createReadStream](https://nodejs.org/api/fs.html#fs_fs_createreadstream_path_options)
     - [Streams (nodejsdev.ru)](https://nodejsdev.ru/api/stream/)
     - [Pipe (nodejsdev.ru)](https://nodejsdev.ru/guide/pipe/)
     - [Stream by Metanit](https://metanit.com/web/nodejs/2.10.php)
     - [Pipe by Metanit](https://metanit.com/web/nodejs/2.11.php)
- Path module:
     - [Path](https://nodejs.org/api/path.html)
     - [Path translation into Russian](https://nodejsdev.ru/api/path/)
