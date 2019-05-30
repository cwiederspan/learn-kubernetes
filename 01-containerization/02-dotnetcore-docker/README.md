# .NET Core Dockerfile

## Add Docker Support

* [Visual Studio 2017](https://docs.microsoft.com/en-us/dotnet/standard/containerized-lifecycle-architecture/design-develop-containerized-apps/visual-studio-tools-for-docker)
* [Visual Studio 2019](https://docs.microsoft.com/en-us/visualstudio/containers/overview?view=vs-2019)
* [VS Code](https://code.visualstudio.com/docs/azure/docker)

## Build and Run the Container

```bash
code ./src

cd ./src

# Build the container image
docker build -t myappweb:dev .

# Check for the image in the list
docker image list

# Pass in an environment variable
docker run -it --rm -p 8090:80 -e CUSTOMER=Acme myappweb:dev
```

## Test the Application

<http://localhost:8090>