# Get-CMContentPaths
Quickly get the content paths for Configuration Manager applications and packages

## Installation

Simply download the zip or clone the repository. 

```
git clone https://github.com/tcoliver/Get-CMContentPaths.git
cd Get-CMContentPaths
```

## Usage

### Import the module using Import-Module

```powershell
Import-Module .\Get-CMContentPaths.psm1
```

### Get all Configuration Manager applications content paths

```powershell
Get-CMApplicationContentPaths -SiteServer "mysiteserver.example.com" -SiteCode "S01"
```

### Example Application Output
```
Name            : Example Application
Id              : ScopeId_XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/Application_XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/1
DeploymentTypes : {@{Name=Example Deployment; ContentPaths=System.Collections.ArrayList}}
XML             : Application(ScopeId_XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/Application_XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/1)
```

### Get all Configuration Manager packages content paths

```powershell
Get-CMApplicationContentPaths -SiteServer "mysiteserver.example.com" -SiteCode "S01"
```

### Example Package OutPut
```
Name            : Example Package
Id              : S0100001
ContentPath     : \\myshare\path\to\package\content\
```

## Features
* Get content paths for all applications and packages
* Simple PSObject output format

## Requirements
* Powershell 5.1
* Configuration Manager installed on the local machine
* Access rights to read applications and packages on your Configuration Manager site