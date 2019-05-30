FROM mcr.microsoft.com/dotnet/core/aspnet:2.2-stretch-slim AS base
WORKDIR /app

FROM mcr.microsoft.com/dotnet/core/sdk:2.2-stretch AS build
WORKDIR /src
COPY ["MyApp.Web.csproj", ""]
RUN dotnet restore "MyApp.Web.csproj"
COPY . .
WORKDIR "/src/"
RUN dotnet build "MyApp.Web.csproj" -c Release -o /app

FROM build AS publish
RUN dotnet publish "MyApp.Web.csproj" -c Release -o /app

FROM base AS final
WORKDIR /app
COPY --from=publish /app .
ENTRYPOINT ["dotnet", "MyApp.Web.dll"]