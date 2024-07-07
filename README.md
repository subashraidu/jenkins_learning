# jenkins

# What is jenkins

+ Jenkins is an open source automation server. That facilitates the continuous integration and continuous delivery (CI/CD) of software development projects. It allows developers to automate the building, testing, and deployment of their code, making the development process more efficient and reliable. Jenkins can integrate with various version control systems, such as Git, and supports a wide range of plugins to extend its functionality. It's widely used in software development teams to automate repetitive tasks and streamline the development pipeline It is a server-based system that runs in servlet containers such as Apache Tomcat (A servlet is a Java program that runs on a web server and handles client requests to generate dynamic web content.). Programming language: Java
  
+ Jenkins can be installed through native system packages, Docker, or even run standalone by any machine with a Java Runtime Environment (JRE) installed.

# jenkins architecture

Jenkins has a modular architecture that allows it to be highly extensible and customizable according to various automation needs in software development. Here's an overview of its architecture:

    # Master-Slave Architecture:

    Master: The Jenkins master is the central server that coordinates and manages the build process. It schedules jobs, monitors agents (slaves), and provides the web interface for users to interact with Jenkins.
    Agent (Slave): Jenkins agents (also known as slaves) are worker nodes that execute build jobs dispatched by the master. Agents can be set up on different operating systems and environments to execute builds in parallel.

    # Build Jobs:

    Jenkins operates based on jobs or tasks known as "build jobs". These jobs define what Jenkins should do, such as fetching source code from a repository, compiling code, running tests, and deploying applications.
    Jobs are configured via a web interface or by defining Jenkinsfiles (using Jenkins Pipeline), which are stored in version control systems.

    # Plugins:

    Jenkins functionality can be extended through plugins. Plugins integrate Jenkins with various tools and services for source code management, build automation, testing, deployment, monitoring, and more.
    There are thousands of plugins available in the Jenkins plugin ecosystem, allowing users to customize Jenkins to fit their specific needs.

    # Web Interface:

    Jenkins provides a user-friendly web interface that allows users to create, configure, and monitor build jobs. Users can view build logs, manage plugins, set up credentials, and view reports and statistics.

    # Distributed Builds:

    Jenkins supports distributed builds, where different build jobs can be executed on different agents simultaneously. This helps in scaling Jenkins for large projects and optimizing build times.

    



+ Jenkins and its main feature ---> Jenkins Pipeline.
  
+ Jenkins Pipeline (or simply "Pipeline" with a capital "P") is a suite of plugins which supports implementing and integrating continuous delivery pipelines into Jenkins.

+ A continuous delivery (CD) pipeline is an automated expression of your process for getting software from version control right through to your users and customers. Every change to your software (committed in source control) goes through a complex process on its way to being released. This process involves building the software in a reliable and repeatable manner, as well as progressing the built software (called a "build") through multiple stages of testing and deployment.

+ Pipeline provides an extensible set of tools for modeling simple-to-complex delivery pipelines "as code" via the Pipeline domain-specific language (DSL) syntax.

+ The definition of a Jenkins Pipeline is written into a text file (called a Jenkinsfile) which in turn can be committed to a project’s source control repository. [2] This is the foundation of "Pipeline-as-code"; treating the CD pipeline as a part of the application to be versioned and reviewed like any other code.

+Creating a Jenkinsfile and committing it to source control provides a number of immediate benefits:

Automatically creates a Pipeline build process for all branches and pull requests.

Code review/iteration on the Pipeline (along with the remaining source code).

Audit trail for the Pipeline.

Single source of truth [3] for the Pipeline, which can be viewed and edited by multiple members of the project.

While the syntax for defining a Pipeline, either in the web UI or with a Jenkinsfile is the same, it is generally considered best practice to define the Pipeline in a Jenkinsfile and check that in to source control.

+ A Jenkinsfile can be written using two types of syntax — Declarative and Scripted.

Declarative and Scripted Pipelines are constructed fundamentally differently. Declarative Pipeline is a more recent feature of Jenkins Pipeline which:

provides richer syntactical features over Scripted Pipeline syntax, and

is designed to make writing and reading Pipeline code easier.

Many of the individual syntactical components (or "steps") written into a Jenkinsfile, however, are common to both Declarative and Scripted Pipeline.


+ Jenkins is, fundamentally, an automation engine which supports a number of automation patterns. Pipeline adds a powerful set of automation tools onto Jenkins, supporting use cases that span from simple continuous integration to comprehensive CD pipelines. By modeling a series of related tasks, users can take advantage of the many features of Pipeline:

Code: Pipelines are implemented in code and typically checked into source control, giving teams the ability to edit, review, and iterate upon their delivery pipeline.

Durable: Pipelines can survive both planned and unplanned restarts of the Jenkins controller.

Pausable: Pipelines can optionally stop and wait for human input or approval before continuing the Pipeline run.

Versatile: Pipelines support complex real-world CD requirements, including the ability to fork/join, loop, and perform work in parallel.

Extensible: The Pipeline plugin supports custom extensions to its DSL [1] and multiple options for integration with other plugins.

While Jenkins has always allowed rudimentary forms of chaining Freestyle Jobs together to perform sequential tasks, [4] Pipeline makes this concept a first-class citizen in Jenkins.

+ 
