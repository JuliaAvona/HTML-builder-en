## Read file with console output

In the **index.js** file of the **01-read-file** directory, write a script that displays the contents of the **text.txt** file.

### General rules:

- It is forbidden to use any external modules
- Random jobs should be run with node <folder name> executed in the root directory
- It is forbidden to use synchronous functions of the fs module, such as ```fs.statSync(path[, options])```,
```fs.readFileSync(path[, options])``` and others found in [synchronous API](https://nodejs.org/api/fs.html#fs_synchronous_api)

### Requirements

- [ ] Inside the folder ***01-read-file*** there are 2 files **index.js** and **text.txt**
- [ ] When executing the ``node 01-read-file``` command in the root directory of the repository, the contents of the **text.txt** file are displayed in the console.
- [ ] Synchronous file reading methods should not be used in the code.
- [ ] Reading a file must be efficient with **ReadStream**.


### Task objectives
- Get acquainted with the basics of working with the file system on the Node.Js platform
- Explore major streams and events
- Familiarize yourself with the Path module and use it to build an absolute path to a file.

### Description
The pre-assignment requires you to write a small script that is expected to output a preloaded text file to the console. To do this, you can follow this procedure:

1. Import the modules necessary to complete the task:
- To interact with the file system in NodeJs, the fs module is used, the documentation of which can be found at this [link] (https://nodejs.org/api/fs.html#fs_file_system) (Russian translation is attached in the "Useful links" section) .
- You will need the [Path](https://nodejs.org/api/path.html#path_path_join_paths) module to correctly specify the path to the file.
2. Create a new **ReadStream** from the **text.txt** file.
3. Set the read stream to standard output.

### Adviсe
To import into Node.js, tag [CommonJS modules](https://nodejs.org/docs/latest/api/modules.html#modules_modules_commonjs_modules). Even though Node.js currently has almost complete support for **ECMAScript** modules (import/export), this approach is not yet completely stable and the vast majority of object code you will encounter will be written with * *CommonJS* *.
Note: ```const fs = require('fs');```

To read a file, you use streams ([streams](https://nodejs.org/api/stream.html#stream_readable_streams)) which are an efficient and useful part of the platform. Thanks to them, you can increase the amount of a large amount of data in parts at times, while consuming a significant amount of resources, instead of increasing their memory in the flora. In the future, you will encounter them more than once in your work.
It will also be important to get acquainted with another basic concept of the Node.js platform, namely **Events** (events). Node.js uses almost existing events, and the remaining objects are inherited from the **EventEmitter** class. For a more complete disclosure of the thread, it is recommended that you first familiarize yourself with the events, since each thread inherits **EventEmitter**.
Materials on these topics are also added to the "Useful Links" section.


When creating a **ReadStream**, please note that your product startup command must be executed in the root directory of the repository, and therefore it is important to correctly pass the path to the file for reading. Node.js, in the case of passing a relative path to a file like ```./text.txt```, will look for its relative directories in which the process was launched. The **join** function from the [Path](https://nodejs.org/api/path.html#path_path_join_paths) module allows you to create a full path to a text file that is easily found by [__dirname](https://js-node .ru/site/article?id=24#globals_dirname) containing the path to the directory where your script file is located. So the directory you're running the code from doesn't point to where to find the file you're looking for, and you always create a source on **text.txt** next to **index.js**. Also, the [Path](https://node.js.org/api/path.html#path_path_join_paths) module contains other useful functions for managing paths, and therefore it is recommended to use its capabilities.

You can learn more about the flow of threads [here] D1%82%D0%BD%D1%8B%D0%B5_%D0%BF%D0%BE%D1%82% D0%BE%D0%BA%D0%B8)),
You can either use the high-level [console.log()](https://nodejs.org/api/console.html#console_console_log_data_args) or work directly with the output stream [process.stdout](https://nodejs.org /api/process.html#process_process_stdout).

##### Useful links
*Please note that translations of the documentation into Russian may be outdated and may not contain all the modern features of the modules. However, the basic concepts described there still work today. Always refer to the official documentation for up-to-date information!*
- Events:
     - [Understanding Node.js Event-Driven Architecture (FreeCodeCamp)](https://www.freecodecamp.org/news/understanding-node-js-event-driven-architecture-223292fcbc2d/)
     - [Event emitter (nodejsdev.ru)](https://nodejsdev.ru/doc/event-emitter/)
     - [Translation of documentation Events (nodejsdev.ru)](https://nodejsdev.ru/api/events/)
     - [Events guide (nodejsdev.ru)](https://nodejsdev.ru/guide/events/)
- Streams:
     - [Stream](https://nodejs.org/api/stream.html)
     - [fs.createReadStream](https://nodejs.org/api/fs.html#fs_fs_createreadstream_path_options)
     - [Streams (nodejsdev.ru)](https://nodejsdev.ru/api/stream/)
     - [Pipe (nodejsdev.ru)](https://nodejsdev.ru/guide/pipe/)
- Path module:
     - [Path](https://nodejs.org/api/path.html)
     - [Path translation into Russian](https://nodejsdev.ru/api/path/)
- Process:
     - [Process](https://nodejs.org/api/process.html)
     - [Process translation into Russian] (https://nodejsdev.ru/api/process/)
