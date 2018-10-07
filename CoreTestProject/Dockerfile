FROM microsoft/dotnet:2.1-aspnetcore-runtime AS base
WORKDIR /app
EXPOSE 51299
EXPOSE 44328

FROM microsoft/dotnet:2.1-sdk AS build
WORKDIR /src
COPY CoreTestProject/CoreTestProject.csproj CoreTestProject/
RUN dotnet restore CoreTestProject/CoreTestProject.csproj
COPY . .
WORKDIR /src/CoreTestProject
RUN dotnet build CoreTestProject.csproj -c Release -o /app

FROM build AS publish
RUN dotnet publish CoreTestProject.csproj -c Release -o /app

FROM base AS final
WORKDIR /app
COPY --from=publish /app .
ENTRYPOINT ["dotnet", "CoreTestProject.dll"]
