# NugetError

This repository includes versions of nuget to show an issue when installing a package. 

This issue occurs when using the -excludeVersion flag and if you have multiple versions of the same package in your packages folder. You get the error message: "An item with the same key has already been added."

To reproduce:
Clone repository
Open command prompt
Navigate to repository

Run the command: 
.\nuget4.4.exe Install stylecop.msbuild -o "packages" -excludeversion
You should see the error message "An item with the same key has already been added."

Run the command: 
.\nuget4.5.exe Install stylecop.msbuild -o "packages" -excludeversion
You should see the error message "An item with the same key has already been added."

Run the command
.\nuget4.3.exe Install stylecop.msbuild -o "packages" -excludeversion
The package should install.

Please note, once installed version 4.4 and 4.5 will work correctly as the package is already installed. To make them fail again please delete the "StyleCop.MsBuild" folder in the packages folder.

