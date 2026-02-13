## Exercise 11.1

The application is written in Java. The CI setup includes multiple tools for linting, testing, and building. The following is my choices for these tools, however, there are many options out there not mentioned here.

### Linting

For linting, I chose Spotless. This tool can enforce coding standard rules but also fix them on demand. This was an easy choice as I am somewhat familiar with the tool from previous projects. Having the tool basically reformat any author's code to fit the same format in the CI pipeline helps the team ship similar code. I also looked at Checkstyle, which I noticed many people use together with Spotless based on my internet search. They seem to mostly have similar features though, excluding that Spotless also fixes the issues found.

### Testing

Testing is done with the popular JUnit testing library. JUnit can be integrated to run in the CI/CD pipeline. This is also familiar to me from previous projects. Mockito can be used together with JUnit if the project needs more advanced mocking for the unit tests.

### Building

The application will be built with Maven. There are other popular options too, like Gradle. The choice comes down to personal preference. I have easily picked up Maven in the past and it is easy to work with.

### Alternatives to Jenkins and GitHub Actions

I found multiple promising alternatives: CircleCI, Travis CI, AWS CodePipeline, Azure DevOps. Without going too much into each, it soudns like AWS CodePipeline and Azure DevOps would be good choices if the application is also hosted there, or other resources from these providers are used. Travis CI especially caught my eye, however. This is a CI tool that is often used for Haskell, which I've learned to write recently.

### Self-hosted or cloud-based?

I'd go for cloud-based here. The release is coming soon, and the CI/CD pipeline would have been best to have in place yesterday. Cloud-based setup is quicker to get working. The team is also quite small with just 6 people, which most likely won't take full advantage of a self-hosted setup. However, if the organization is bigger than just this one team, the teams could decide to setup a self-hosted CI together.