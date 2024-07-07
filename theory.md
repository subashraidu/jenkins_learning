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

    

# Diffenet types of Jenkins agent.

 In Jenkins, agents (also known as slaves) are worker nodes that execute build jobs dispatched by the master server. Agents can be configured to run on different operating systems, environments, or hardware configurations to accommodate diverse build and test requirements. Here are different types of agents in Jenkins:

    # Static Agents:
    
        Static agents are traditional Jenkins agents that are configured and permanently registered with the Jenkins master. They typically run on dedicated hardware or virtual machines (VMs) and are always available to execute build jobs.

    # Dynamic Agents:
    
        Dynamic agents are provisioned on-demand by Jenkins to handle workload spikes or specific job requirements. Jenkins can dynamically spin up instances of these agents in cloud environments (like AWS, Azure, Google Cloud) using plugins such as Amazon EC2 Plugin, Azure VM Agents Plugin, or Google Compute Engine Plugin.


    # Permanent vs. Temporary Agents:

    Permanent agents are long-lived agents that remain registered with Jenkins indefinitely, available for any job execution. They are typically used for stable environments where consistent availability is required.
    Temporary agents are short-lived agents that Jenkins spawns for specific jobs and releases afterward. They are useful for optimizing resource utilization and scaling based on workload demands.

# Build types in jenkins.

n Jenkins, "build types" generally refer to the different kinds of builds or jobs that can be configured and executed within the Jenkins environment. These build types define the actions Jenkins will perform when a job is triggered, such as compiling code, running tests, packaging artifacts, and deploying applications. Here are some common build types you can define in Jenkins:

      # Freestyle Project:
        A Freestyle project is the simplest form of Jenkins job. It allows you to configure a series of build steps, which can include shell scripts, batch commands, or other build actions. You have flexibility in defining the sequence and execution of these build steps.

       # Pipeline:
        Jenkins Pipeline is a suite of plugins that supports continuous delivery and automation of tasks in Jenkins. Pipelines can be defined using a DSL (Domain-Specific Language) called Groovy, either in a Jenkinsfile stored within your version control system or directly in the Jenkins UI. Pipelines offer robust capabilities for defining complex workflows, including parallel execution, stages, and advanced conditions.

       # Multi-configuration Project:
        Also known as Matrix projects, these allow you to run the same build job on multiple configurations (such as different operating systems, JDK versions, or browser types) in parallel. It's useful for testing software across different environments simultaneously.

       # GitHub Organization:
        This build type allows Jenkins to automatically create and configure jobs for repositories within a GitHub organization or GitHub Enterprise. It scans GitHub repositories and creates jobs based on predefined templates or configurations.

       # GitHub Pull Request Builder:
        This type of build job is triggered automatically when pull requests are opened or updated on GitHub repositories. Jenkins checks out the pull request, builds it, and reports back the status (success, failure, etc.) on GitHub.

       # Maven Project:
        Jenkins provides specific support for Maven-based projects. Maven projects automatically manage dependencies, perform builds according to Maven lifecycle phases (like compile, test, package), and can publish artifacts to Maven repositories.

       # Freestyle Maven Project:
        Similar to a standard Freestyle project but specifically configured to build Maven-based projects. It integrates Maven commands directly into the build steps.

       # Pipeline (Multibranch):
        This type of pipeline job automatically creates a new Jenkins Pipeline job for each branch in a repository. It scans branches and applies the Pipeline configuration defined in the Jenkinsfile within each branch.The definition of a Jenkins Pipeline is written into a text file (called a Jenkinsfile) which in turn can be committed to a project’s source control repository. This is the foundation of "Pipeline-as-code"; treating the CD pipeline as a part of the application to be versioned and reviewed like any other code.

        
These are some of the common build types available in Jenkins, each tailored to different use cases and project requirements. Jenkins' flexibility and extensive plugin ecosystem allow users to customize and extend these build types to suit specific automation needs in software development and deployment pipelines.

# Different types of syntaxes in Jenkins.

In Jenkins, when writing configurations for jobs or pipelines, you primarily work with two syntaxes: Declarative Pipeline Syntax and Scripted Pipeline Syntax (also known as Scripted Pipeline DSL). 

    # Declarative Pipeline Syntax

Declarative Pipeline Syntax is a more structured and opinionated way of defining Jenkins Pipelines. It provides a simpler and more limited syntax but aims to be easier to read and write for straightforward use cases. 

    # Scripted Pipeline Syntax

Scripted Pipeline Syntax provides more flexibility and is based on Groovy scripting language. It allows you to write entire Pipelines as code, with full access to Jenkins' Pipeline API and any Groovy syntax or libraries. 

     # Key Syntax Elements

    Pipeline Block: Defines the entire pipeline structure.
    Agent: Specifies where the pipeline will execute.
    Stages: Divides the pipeline into stages (e.g., build, test, deploy).
    Steps: Actions to be executed within each stage (e.g., shell commands).
    Environment: Sets environment variables for the pipeline.
    Post: Defines actions to be taken after stages (e.g., notifications).
    Triggers: Specifies conditions or schedules to trigger the pipeline.
    Options: Configures pipeline options (e.g., timeout, retry).

These syntaxes provide powerful ways to define automation workflows in Jenkins, allowing developers and teams to automate build, test, and deployment processes effectively. The choice between Declarative and Scripted Pipeline syntax often depends on the complexity and flexibility required by your specific CI/CD pipeline.



