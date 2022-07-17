#See https://aka.ms/containerfastmode to understand how Visual Studio uses this Dockerfile to build your images for faster debugging.

#Depending on the operating system of the host machines(s) that will build or run the containers, the image specified in the FROM statement may need to be changed.
#For more information, please see https://aka.ms/containercompat

FROM mcr.microsoft.com/dotnet/aspnet:6.0 AS base
WORKDIR /app
EXPOSE 80
EXPOSE 443

FROM mcr.microsoft.com/dotnet/sdk:6.0 AS build
WORKDIR /src
COPY ["ZecicAPI-1/ZecicAPI-1.csproj", "ZecicAPI-1/"]
RUN dotnet restore "ZecicAPI-1/ZecicAPI-1.csproj"
COPY . .
WORKDIR "/src/ZecicAPI-1"
RUN dotnet build "ZecicAPI-1.csproj" -c Release -o /app/build

FROM build AS publish
RUN dotnet publish "ZecicAPI-1.csproj" -c Release -o /app/publish

FROM base AS final
WORKDIR /app
COPY --from=publish /app/publish .
ENTRYPOINT ["dotnet", "ZecicAPI-1.dll"]