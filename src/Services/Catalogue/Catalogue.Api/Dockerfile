#See https://aka.ms/containerfastmode to understand how Visual Studio uses this Dockerfile to build your images for faster debugging.

FROM mcr.microsoft.com/dotnet/aspnet:6.0 AS base
WORKDIR /app
EXPOSE 80
EXPOSE 443

FROM mcr.microsoft.com/dotnet/sdk:6.0 AS build
WORKDIR /src
COPY ["Services/Catalogue/Catalogue.Api/Catalogue.Api.csproj", "Services/Catalogue/Catalogue.Api/"]
RUN dotnet restore "Services/Catalogue/Catalogue.Api/Catalogue.Api.csproj" --disable-parallel
COPY . .
WORKDIR "/src/Services/Catalogue/Catalogue.Api"
RUN dotnet build "Catalogue.Api.csproj" -c Release -o /app/build

FROM build AS publish
RUN dotnet publish "Catalogue.Api.csproj" -c Release -o /app/publish /p:UseAppHost=false

FROM base AS final
WORKDIR /app
COPY --from=publish /app/publish .
ENTRYPOINT ["dotnet", "Catalogue.Api.dll"]