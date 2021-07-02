# Serverless Computing: Taking DevOps to the Next Level
In this repository you can find the demo presented at the [.NET Serverless Day 2021](https://www.aspitalia.com/eventi/89/.NET-Serverless-Day-Online.aspx) event. 

## Demos
Demos are grouped into different foldes:
- __AppServiceReleaseStrategy__: contains a basic ASP.NET Core project with a simple API endpoint (exposed in the root '/') that prints the running version. This is needed so that we can use each of the GitHub Actions _build-release-aspnetcore.yml_, _build-release-aspnetcore-with-blue-green.yml_ or _build-release-aspnetcore-with-canary.yml_ to verify how a different version can be rolled out in production, with or without downtime.
- __FunctionAppClassicReleaseStrategy__: contains a basic Azure Function that after it is running will print "Hello, {name}" where the _name_ variable is coming from the HTTP request in input. However the function is created in conjunction with the GitHub Action _build-release-functionapp.yml_ that demonstrates how the same build/release process used in ASP.NET Core process works.
- __FunctionAppContainerReleaseStrategy__: is the same Azure Function described before, however the distribution and execution will be based on a Docker container. In this case the _build-release-docker-functionapp.yml_ action will show how the deployment differs in this scenario. 
