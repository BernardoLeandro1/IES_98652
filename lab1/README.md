In lab1.1 we learn how to set up maven. In my case, I had already used Maven, so it was already setted up. 

In lab1.2 we create and explore our first maven project of this class.

    ex2 is the creation of a maven project.

    d is the exercise d from lab1_2, where we will use an api from IPMA -> http://api.ipma.pt/ 
    
        For this we use 2 different dependencies, to insert in POM file -> Retrofit (https://square.github.io/retrofit/) and Gson (https://github.com/google/gson)
            Retrofit is a type-safe HTTP client for Java, that allows mapping an external REST API into a local (Java) interface.
            Gson is a Java library that can be used to convert Java Objects into their JSON representation.

        In the pom.xml file I inserted developer, changed the java version and inserted character encoder

In lab1.3 we learn about git, add .gitignore files to the projects.

    In this exercise i cloned my repo in location2 and made some changes

In lab1.4 we learned about docker and some important commands. 

    We learned what is a Dockerfile (text document that contains all the commands a user could call on the command line to assemble an image) and a docker-compose.yml file (you use a YAML file to configure your application's services)


In lab 1.5, I needed to put the artifact of ipmaclient on the pom.xml of weatherforecast 

During this lab I also made a general notebook, which will be updated in every lab, that contains the most important/useful commands.

From now on, groupID = labX and artifactID = exY, X being the lab number and Y being the exercise number from labX


QUESTIONS

    A - Maven has three lifecycles: clean, site and default. Explain the main phases in the default lifecycle.
        
        The Default lifecycle of Maven has 23 build phases, the main ones are:
            - validate : validate if the project is correct and all necessary information is available;

            - compile : compile the source code of the project;

            - test : test the compiled source code using a suitable unit testing framework. These tests should not require the code to be packaged or deployed;

            - package : take the compiled code and package it in its distributable format, such as a JAR;

            - verify : run any checks on results of integration tests to ensure quality criteria are met;

            - install : install the package into the local repository, to use as a dependency in other projects locally;

            - deploy : done in the build environment, copies the final package to the remote repository for sharing with other developers and projects.



    B - Maven is a build tool; is it appropriate to run your project to?

        Maven's main purpose is to configure a project and handle the build activities and resulting artifacts. Maven can be used to run a project by using different plugins to execute specific classes.

    C - What would be a likely sequence of Git commands required to contribute with a new feature to a given project? (i.e., get a fresh copy, develop some increment post back the added functionality)

        1 - git clone
        
        2 - git branch [modifications] 
        
        3 - git add 
        
        4 - git commit -m 
        
        5 - git push 

    D - There are strong opinions on how to write Git commit messages... Find some best practices online and give your own informed recommendations on how to write good commit messages (in a team project).

        In a team project, writing good commit messages is crucial to provide useful information about what has changed and why. In order to make good commit messages there are a few steps we can follow:

        - Specify the type of commit;

        - Separate the subject from the body with a blank line. Also separate the various topics with blank lines;

        - Your commit message should not contain any whitespace errors;

        - Remove unnecessary punctuation marks;
        
        - Use the body to explain what changes you have made and why you made them;
        
        - Do not assume the reviewer understands what the original problem was and do not think your code is self-explanatory, ensure you add everything in a way everyone can understand what they are looking at;
        
        - Follow the commit convention defined by your team.


    E - Docker automatically prepares the required volume space as you start a container. Why is it important that you take an extra step configuring the volumes for a (production) database?

        Docker volumes are file systems mounted on Docker containers to preserve data generated by the running container. The volumes are stored on the host, independent of the container life cycle. This makes data safe if a container is deleted and allows users to back up data and share file systems between containers easily.

