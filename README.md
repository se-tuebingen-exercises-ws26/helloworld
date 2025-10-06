# Hello World

A simple "hello world" project with Scala 3.7.3 and sbt.

## Preliminaries
To run the project, you need to have a few things installed:

- a recent version of the JDK (>= 12)
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
[info] welcome to sbt 1.7.1 (Homebrew Java 19)
[info] loading global plugins from /Users/jonathan/.sbt/1.0/plugins
[info] loading project definition from /private/tmp/helloworld/project
[info] loading settings for project helloworld from build.sbt ...
[info] set current project to helloworld (in build file:/private/tmp/helloworld/)
[info] sbt server started at local:///Users/jonathan/.sbt/1.0/server/b4d7872362a29e152887/sock
[info] started sbt server
sbt:helloworld>
```
Here you can run many different commands to interact with your program. The most important ones for now are

- `run` -- this will run the program.
- `compile` -- this will compile the source code into Java byte code (you can find the generated code in the `target` folder)

Simply enter `run`, and sbt will do all the heavy lifting. It downloads the correct version of the Scala language
compiler for you. Afterwards, it compiles the file `hello.scala`. Finally, it runs the method marked with `@main`.
You should see something similar to the following output:
```
sbt:helloworld> run
[info] compiling 1 Scala source to /private/tmp/helloworld/target/scala-3.2.0/classes ...
[info] running sayHello
Hey, what's your name? (please press <Enter> after entering your name)
Jonathan
Hello there, Jonathan!

Seems like you have all dependencies set up correctly.
Apparently, this application is running on Mac OS X with JDK 19.

[success] Total time: 2 s, completed 12 Oct 2022, 17:59:26
sbt:helloworld>
```
The application will ask you for your name and then print back a simple greeting,
and your operating system and JDK versions.
After exiting, sbt is now ready to take the next command.
