# Hello World

A simple "hello world" project with Scala 3.9.0 and sbt 2.

## Preliminaries
To run the project, you need to have a few things installed:

- a recent version of the JDK (>= 17)
- the sbt build tool

If you are missing a dependency, the [forum](https://ps-forum.cs.uni-tuebingen.de/c/se/anleitungen-und-erklaerungen) will provide detailed guides on how to install them.

## Running the Program
Working with sbt and Scala will be covered in a separate homework, so do not worry about the details, so far.
Here, we will just run our program to see whether all dependencies are installed, correctly.

To run hello world, we first enter the "sbt terminal". Open a terminal of your choice and
navigate (using the `cd` command on Unix systems) to the project directory:

```
$ cd helloworld/
```

From the very root of the directory (not within some other folder), start `sbt`:

```
$ sbt
```
If everything goes well, you will be greeted with a prompt:
```
[info] entering thin client - BEEP WHIRR
[info] starting sbt server in the background
[info] use 'sbt shutdown' to shutdown the server
[info]  
[info] welcome to sbt 2.0.9 (Azul Systems, Inc. Java 21.0.11)
[info] loading project definition from /Users/gaisseml/teaching/se/ws26/homework/helloworld/project
[info] set current project to helloworld (in build file:/Users/gaisseml/teaching/se/ws26/homework/helloworld/)
sbt:helloworld>
```
Here you can run many different commands to interact with your program. The most important ones for now are

- `run` -- this will run the program.
- `compile` -- this will compile the source code into Java byte code (you can find the generated code in the `target` folder)
- `shutdown` -- terminate the background daemon (that makes it faster on subsequent runs, but might consume some resources)

Simply enter `run`, and sbt will do all the heavy lifting. It downloads the correct version of the Scala language
compiler for you. Afterwards, it compiles the file `hello.scala`. Finally, it runs the method marked with `@main`.
You should see something similar to the following output:
```
sbt:helloworld> run
[info] running (fork) sayHello 
Hey, what's your name??? (please press <Enter> after entering your name)
Jonathan
Hello there, Jonathan!

Seems like you have all dependencies set up correctly.
Apparently, this application is running on Mac OS X with JDK 21.0.11.

[success] ok
sbt:helloworld>
```
The application will ask you for your name and then print back a simple greeting,
and your operating system and JDK versions.
After exiting, sbt is now ready to take the next command.
