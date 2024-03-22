# jenkins-notes
Notes for Jenkins a CI/ CD Tool for DevOps

# What is CI/ CD?
- One of the Approach of SDLC.

## CI (Continuous Integration)
- That means instead of deploying your code at the end of day, week or anytime you want you will deploy it the moment you commit and push it in your remote repository.
- CI includes the build, test, and merge process of your project.

## CD (Continuous Delivery)
- That means making your source code ready to be released in production/ live environment. Also having a specific version of your project ready to be delivered in your client or to your co-workers or deployed in different environments(To be discussed later).

## Why do need CI/ CD?
First we identify the manual process of how our source code will reach upto deployment.

### Steps of Build and Deployment Process
1. Commit and push your latest code in remote repository.
2. Run unit test before building your project.
3. Build your project to create war or jar file.
4. Create an docker image and push it in docker registry (Docker hub).
5. Deploy your app.

As you can see theres nothing wrong in this stepd but imagine doing it every day, every week, or anytime you want its a lot of work and labor needed.

### Challenges in Manual Process.
1. Repeated Work.
2. Takes a lot of time and effort.
3. Deploying code in multiple environment is just nightmare.
4. Error prone.

Thats why we need CI/ CD to resolved all of this increasing our productivity and less time and effort for this repeated work.

# Different Realtime Enviroments
- Development Environment
- Quality Assurance Environment
- User Assurance Test Environment
- Production Environment

# Different Type of Teams in Realtime Project
- *Development Team*: Responsible for writing project source code.
- *Quality Assurance Team*: Responsible for testing the development team delivered project and also verify and validate all the system requirements.
- *Operation Team*: Responsible for Deployment of project.
###### Development + Operation Team => DevOps

# What is Jenkins
- Free and open-source software
- Written in Java Languange
- Used for automation pf Build and Deployment process.
- Using Jenkins we can implement CI/ CD

## Jenkins Project Setup
### Source Code Management
    - Where your source code coming from (Usually Github is used in this)

### Build Triggers
     - When you want to execute and automate the build process.
     - POLL SCMM is used to continously pull and automate build process with specified cron job

### Build Environment
     - Setup the environment for build process.
 
 ### Build Steps
     - How you want to do the build?
	
 ### Post Build Actions
      - What you want to do after build process is finished either create an docker image and push it in docker registry

## Two Types of Jenkins Scripting Scripting
### Scripting Pipeline: Starts with *node* and using Groovy Languange
### Declarative Pipeline: Starts with *pipeline*

## What is jenkinsfile

```
pipeline {
  agent any
  stages {
      stage("Checkout") {
            when {
              // Execute only if condition is true
            }
            git branch: '<branch_name>', credential: '<credential_if_your_repo_is_private>', url: '<github_url>'
      }
      stage("Clean Install") {
         sh 'mvn clean install'
      }
  }
  post { // Literallg Anything you want to do after a successful build
        always {}
        success {}
        failure {}
  }
}
```

# For more Reference
- [Ashok IT CI/ CD Youtube Video](https://youtu.be/Ri-URt8gPCk)
