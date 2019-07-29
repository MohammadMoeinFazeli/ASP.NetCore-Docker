FROM mcr.microsoft.com/dotnet/core/sdk:2.2-stretch

RUN mkdir /app
WORKDIR /app

COPY DockerASPnetCore.csproj .
RUN dotnet restore

COPY . .
RUN dotnet publish -c Release -o out

EXPOSE 5000/tcp
CMD ["dotnet", "out/DockerASPnetCore.dll"]
