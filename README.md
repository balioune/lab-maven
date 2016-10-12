### lab-maven
Maven is a project management tool which encompasses a project object model,  a set of standards,  a project lifecycle,  a dependency management system,  and
logic for executing plugin goals at defined phases in a lifecycle. When you use Maven, you describe your
project using a well-defined project object model, Maven can then apply cross-cutting logic from a set of
shared (or custom) plugins.

# Creating a simple project

mvn archetype:generate -DgroupId=org.orange.maven \
-DartifactId=simple \
-Dpackage=org.orange.maven \
-DarchetypeArtifactId=maven-archetype-quickstart \
-Dversion=1.0-SNAPSHOT


- The Maven Archetype plugin creates a directory simple that matches the artifactId.  This is known as the project’s base directory
- Every Maven project has what is known as a Project Object Model (POM) in a file named pom.xml . This file describes the project, configures plugins, and declares dependencies
- The project code and source (Java file/ config file) are placed under src/main
- The project’s test cases are located in src/test

        package org.orange.maven;
        
        /**
         * Hello world!
         *
         */
        public class App
        {
            public static void main( String[] args )
            {
                System.out.println( "Hello World!" );
            }
        }

#  Building a Simple Project
        cd simple/
        mvn install

You’ve just created, compiled, tested, packaged, and installed the simplest possible Maven project.
To prove to yourself that this program works, run it from the command line.

        java -cp target/simple-1.0-SNAPSHOT.jar org.orange.maven.App

A maven project is identified by its groupId, artifactId and packaging version

