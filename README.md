# ci-cd-notes
Notes for CI/ CD

# What is CI/ CD?
- One of the Approach of SDLC.

## CI (Continuous Integration)
- That means instead of deploying your code at the end of day, week or anytime you want you will deploy it the moment you commit and push it in your remote repository.
- CI includes the build, test, and merge process of your project.

## CD (Continuous Delivery)
- That means making your source code ready to be released in production/ live environment. Also having a specific version of your project ready to be delivered in your client or to your co-workers or deployed in different environments(To be discussed later).

## Why do need CI/ CD?
- First we identify the manual process of how our source code will reach upto deployment
### Steps Build and Deployment Process
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
## Development + Operation Team => DevOps
