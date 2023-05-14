Copiado del repositorio de Skoruba.IdentityServer4.Admin

# Skoruba.IdentityServer4.Admin

> The administration for the IdentityServer4 and Asp.Net Core Identity

## Project Status

[![Build status](https://ci.appveyor.com/api/projects/status/5yg59bn70399hn6s/branch/master?svg=true)](https://ci.appveyor.com/project/JanSkoruba/identityserver4-admin/branch/master)
[![Build Status](https://dev.azure.com/skoruba/IdentityServer4.Admin/_apis/build/status/IdentityServer4.Admin-CI?branchName=master)](https://dev.azure.com/skoruba/IdentityServer4.Admin/_build/latest?definitionId=2?branchName=master)
[![Join the chat at https://gitter.im/skoruba/IdentityServer4.Admin](https://badges.gitter.im/skoruba/IdentityServer4.Admin.svg)](https://gitter.im/skoruba/IdentityServer4.Admin?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

The application is written in the **Asp.Net Core MVC - using .NET 6**

## 🎉  New version of Duende IdentityServer Admin UI available [here](https://github.com/skoruba/Duende.IdentityServer.Admin) ⚡

## Requirements

- [Install](https://www.microsoft.com/net/download/windows#/current) the latest .NET 6 SDK (using older versions may lead to 502.5 errors when hosted on IIS or application exiting immediately after starting when self-hosted)

## Installation via dotnet new template

- Install the dotnet new template:

### Version 2.0.0 and higher works with **IdentityServer4 version 4** 🚀

- 🔒 **NOTE:** This version affects your database data if you use the default database migrations that are part of the project - double check the migrations according to your database provider and create a database backup

```sh
dotnet new -i Skoruba.IdentityServer4.Admin.Templates::2.1.0
```

### Create new project:

```sh
dotnet new skoruba.is4admin --name MyProject --title MyProject --adminemail "admin@example.com" --adminpassword "Pa$$word123" --adminrole MyRole --adminclientid MyClientId --adminclientsecret MyClientSecret --dockersupport true
```

Project template options:

```
--name: [string value] for project name
--adminpassword: [string value] admin password
--adminemail: [string value] admin email
--title: [string value] for title and footer of the administration in UI
--adminrole: [string value] for name of admin role, that is used to authorize the administration
--adminclientid: [string value] for client name, that is used in the IdentityServer4 configuration for admin client
--adminclientsecret: [string value] for client secret, that is used in the IdentityServer4 configuration for admin client
--dockersupport: [boolean value] include docker support
```

## How to configure the Administration - IdentityServer4 and Asp.Net Core Identity

- [Follow these steps for setup project to use existing IdentityServer4 and Asp.Net Core Identity](docs/Configure-Administration.md)

### Template uses following list of nuget packages

- [Available nuget packages](https://www.nuget.org/profiles/skoruba)

### Running in Visual Studio

- Set Startup projects:
  - Skoruba.IdentityServer4.Admin
  - Skoruba.IdentityServer4.Admin.Api
  - Skoruba.IdentityServer4.STS.Identity

## Configuration of Administration for Deployment
