#FROM microsoft/aspnetcore:1.1
#FROM smurfdocker/dotnet:1.1.2-sdk-clrdbg
FROM smurfdocker/aspnetcore:1.1-clrdbg
ARG source
WORKDIR /app

EXPOSE 5003/tcp
#ENV ASPNETCORE_URLS http://*:5003
ENV ASPNETCORE_URLS http://ubuntu-docker-remote.cloudapp.net:5003

COPY ${source:-obj/Docker/publish} .
COPY ${source:-clrdbg} .
ENTRYPOINT ["dotnet", "MyCoreTest.dll"]
#
#COPY . /app
#COPY . /app1234
#
#WORKDIR /app/MyCoreTest
#RUN ["dotnet", "restore"]
#
#RUN ["dotnet", "build"]
#
#EXPOSE 5003/tcp
#ENV ASPNETCORE_URLS http://*:5003
#
#ENTRYPOINT ["dotnet", "run"]