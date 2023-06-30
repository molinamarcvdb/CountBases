# Project Name: Base Counter

This is a Java-based project that reads a given FASTA file and prints out the count of each nucleotide (A, C, G, T). The project is built using Apache Ant.

## Source Code

The main part of the application is in `Main.java` where the program accepts a path to the FASTA file as an argument, reads the file, and calculates the count of each nucleotide.

## Build File

The build process is managed by the Apache Ant build tool, with the build script written in the `build.xml` file. This file contains various targets that describe the different stages of the build process:

- **init**: This target creates the timestamp and the build directory.
- **compile**: This target compiles the Java source code.
- **dist**: This target creates the distribution directory and generates the JAR file.
- **clean**: This target deletes the build and dist directory trees.

## How to Build and Run the Project

Ensure you have Apache Ant installed on your machine.

To build the project, navigate to the directory containing the `build.xml` file and run the following command:

```
ant
```

This will execute the default target, which is `dist`, generating the JAR file.

To run the application, use the following command, replacing `<path_to_fasta_file>` with the path to your FASTA file:

```
java -jar dist/lib/MyProject-<DSTAMP>.jar <path_to_fasta_file>
```

Replace `<DSTAMP>` with the actual timestamp of the built JAR file.

## Clean Up

To clean up the build and distribution directories, run the following command:

```
ant clean
```

This will delete the `build` and `dist` directories.
