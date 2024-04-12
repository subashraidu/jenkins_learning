# jenkins_learning

+ Jenkins is an open source automation server. That facilitates the continuous integration and continuous delivery (CI/CD) of software development projects. It allows developers to automate the building, testing, and deployment of their code, making the development process more efficient and reliable. Jenkins can integrate with various version control systems, such as Git, and supports a wide range of plugins to extend its functionality. It's widely used in software development teams to automate repetitive tasks and streamline the development pipeline It is a server-based system that runs in servlet containers such as Apache Tomcat. Programming language: Java
  
+ Jenkins can be installed through native system packages, Docker, or even run standalone by any machine with a Java Runtime Environment (JRE) installed.

+ Jenkins and its main feature ---> Jenkins Pipeline.
  
+ Prerequisites --> machine 256 MB of RAM, although more than 2 GB is recommended, 10 GB of drive space (for Jenkins and your Docker image).
+ Prerequisites --> software Java 11, 17, or 21, Docker
+ Download and run Jenkins
+ Download Jenkins Generic Java package (.war)
+ Open up a terminal in the download directory
+ Run java -jar jenkins.war --httpPort=8080
+ Browse to http://localhost:8080
+ Follow the instructions to complete the installation

+ What is a Jenkins Pipeline? Jenkins Pipeline (or simply "Pipeline") is a suite of plugins which supports implementing and integrating continuous delivery pipelines into Jenkins.
+ A continuous delivery pipeline is an automated expression of your process for getting software from version control right through to your users and customers.
+ Jenkins Pipeline provides an extensible set of tools for modeling simple-to-complex delivery pipelines "as code". The definition of a Jenkins Pipeline is typically written into a text file (called a Jenkinsfile) which in turn is checked into a project’s source control repository.
+ 
