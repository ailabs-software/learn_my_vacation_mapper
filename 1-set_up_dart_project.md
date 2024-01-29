# Set up our Dart project
**Goal: ** At the end of this section, you will have a [hello world](https://en.wikipedia.org/wiki/%22Hello,_World!%22_program) running in Dart! This will set you up with a suitable project structure for building an SPA web application.

Open your terminal.

Change directories (`cd`) to the directory where you'd like to work on this project, if desired.

```
mkdir vacation_planner/

cd  vacation_planner/
```



Create a few directories we will use:

```
mkdir lib/

mkdir bin/

mkdir static/
```



With your favourite text editor (such as vim/vscode), create the file `pubspec.yaml` with the following text:

```
name: vacation_planner # Name must match project directory name
description: A web application demonstrating SPA architecture & REST API use.
version: 1.0.0

environment:
  sdk: ^3.0.1

# Add regular dependencies here.
dependencies:

```

This file is somewhat analogous to a package.json file in a NodeJS project.

It allows you to specify the version of your package (project), all of its dependencies & their versions, and the minimum Dart SDK version your package will build on.

A good Dart project also has a `.gitignore` file to keep unwanted temp files from appearing in the git repo. Create this file with this text:

```
.dart_tool/
```



Now, we are ready to start writing Dart code.

Create the file `lib/main.dart` as follows:

```
void main(List<String> arguments) {
  print("Oh, looks like this worked.");
}
```



#### Building our project

Now, we can build `main.dart` to a native executable with:

```
dart compile exe lib/main.dart -o bin/vacation_planner
```

If your source doesn't contain any syntax errors, unresolved dependencies, bad imports, or type-level static analysis errors, this will output the file specified by the -o switch as an executable.

You can then run the executable with:

```
./bin/vacation_planner
```

Voila! You should see a string of text printed to the console.

You now have a working Dart project.

Now, to save us time later, let's create a `build.sh` file that will batch all commands needed to build our app:

```
#!/bin/sh

dart compile exe lib/main.dart -o bin/vacation_planner
```

Make build.sh executable with:

```
chmod +x build.sh
```

You now can build the app with just:

```
./build.sh
```

When we later need to also compile (or rather *transpile*) code to run in the browser, this will help us save time by building both client and server code from one succinct command.

In the next section, we will start writing Dart code to build it out.

**Note**: It is also possible to run Dart directly from the source code without compiling first, but we won't touch on that in this guide. See https://dart.dev/tools/dart-compile for more details on available options.

`dart compile` is able to output JIT code (just-in-time, good for web applications typically), AOT code (minimises startup/warmup time so good for mobile apps with warmup could cause animation jank), or JavaScript (runs in the browser)

*transpile* is the process of converting code from one programming language to another (source code). This process enables us to target the browser's JS engine much like a CPU architecture.



**[Go to next](https://github.com/ailabs-software/learn_vacation_planner/blob/main/2-build_web_server.md)**

