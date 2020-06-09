# **Cretaceous Park**

#### Author: **_Jessica Hvozdovich_**
#### June 7, 2020

### Description

_This application serves as an introduction to building an API with C#/.NET Core._

### Instructions for use:

1. Open Terminal (macOS) or PowerShell (Windows)
2. To download the project Directory to your desktop enter the following commands:
```
cd Desktop
git clone https://github.com/jhvozdovich/cretaceous-park.git
cd cretaceous-park (or the file name you created for the main Directory of the download)
```
3. To view the downloaded files, open them in a text editor or IDE of your choice.
* if you have VSCode for example, when your terminal is within the main project Directory you can open all of the files with the command:
```
code .
```
4. Create a file within the Honeydukes folder named appsettings.json.
5. Add the following code:
```
{
  "Logging": {
    "LogLevel": {
      "Default": "Warning"
    }
  },
  "AllowedHosts": "*",
  "ConnectionStrings": {
    "DefaultConnection": "Server=localhost;Port=3306;database=cretaceous_park;uid=root;pwd=YOURMYSQLPASSWORDHERE;"
  }
}
```
* Make any other changes needed if you have an alternative server, port, or uid selected. These are the default settings.

6. To install the necessary dependencies and start a local host, after replicating the database steps below run the following commands:
```
dotnet restore
dotnet build
dotnet run
```

#### If you need to install and configure MySQL:
1. Download the MySQL Community Server DMG file [here](https://dev.mysql.com/downloads/file/?id=484914) with the "No thanks, just start my download" link.
2. On the configuration page of the installer select the following options:
* Use legacy password encryption
* Set your password
3. Open the terminal and enter the command:
*'export PATH="/usr/local/mysql/bin:$PATH"' >> ~/.bash_profile
4. Download the MySQL Workbench DMG file [here](https://dev.mysql.com/downloads/file/?id=484391)
5. Open Local Instance 3306 with the password you set.

#### To create a local version of the database:
1. Open MySQL Workbench and Local Instance 3306.
2. Select the SQL + button in the top left of the navigation bar.
3. Paste the following in the query section to create the database:

```
CREATE DATABASE `cretaceous_park` ;

USE `cretaceous_park`;

CREATE TABLE `Animals` (
  `AnimalId` int(11) NOT NULL AUTO_INCREMENT,
  `Name` longtext,
  `Species` longtext,
  `Age` int(11) NOT NULL,
  `Gender` longtext,
  PRIMARY KEY (`AnimalId`)
) ENGINE=InnoDB AUTO_INCREMENT=6 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;

```

4. Press the lightning bolt button to run this command.
5. If the database does not appear, right click in the schemas bar and select Refresh All.

### Known Bugs

No bugs have been identified at the time of this update.


### Support and Contact Information

_Have a bug or an issue with this application? [Open a new issue](https://github.com/jhvozdovich/cretaceous-parkissues) here on GitHub._

### Technologies Used

* C#
* `ASP.NET` Core
* `ASP.NET` Core MVC
* Entity Framework Core
* `ASP.NET` Core Identity
* MySQL
* Git and GitHub

### Specs
| Spec | Input | Output |
| :------------- | :------------- | :------------- |
| **** | User Input:"" | Output: “” |
No front end for specs- database practice only.


#### License

This software is licensed under the MIT license.

Copyright © 2020 **_Jessica Hvozdovich_**
