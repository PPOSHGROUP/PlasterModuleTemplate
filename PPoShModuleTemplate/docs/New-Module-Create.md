# How to create new module
---

```
$PlasterTemplatePath = 'Path to PPoshModule template folder' #Path to where you've downloaded this module
$DestinationPath = 'C:\AdminTools\ModuleTest1' #Path to your git repository folder
Invoke-Plaster -TemplatePath $PlasterTemplatePath -DestinationPath $DestinationPath
```
---
### Will result in:
```
  ____  _           _
 |  _ \| | __ _ ___| |_ ___ _ __
 | |_) | |/ _` / __| __/ _ \ '__|
 |  __/| | (_| \__ \ ||  __/ |
 |_|   |_|\__,_|___/\__\___|_|
                                            v1.1.3
==================================================
Author (Mateusz Czerniawski):
Name of your module: TestModule1
Version Number (0.0.1):
Brief Description of your module: This is for testing purpose
Please select folders to include
[P] Public
[P] Private
[C] Configuration
[?] Help
(default choices are P,P,C)
Choice[0]:
Add Git Support
[Y] Yes  [N] No  [?] Help (default is "Y"):
Select a license for your module
[A] Apache  [M] MIT  [N] None  [?] Help (default is "M"): M
Include Pester Tests?
[Y] Yes  [N] No  [?] Help (default is "Y"):
Include PPoShBuild Support?
[Y] Yes  [N] No  [?] Help (default is "Y"):
Include PPoShTools requirement file?
[Y] Yes  [N] No  [?] Help (default is "Y"):
Add VSCode support?
[Y] Yes  [N] No  [?] Help (default is "Y"):
Add Docs folder?
[Y] Yes  [N] No  [?] Help (default is "Y"):
Destination path: C:\AdminTools\ModuleTest1\
Setting up your project
   Create TestModule1\TestModule1.psd1
   Create TestModule1\TestModule1.psm1
Creating you folders for module:
   Create TestModule1\Public\
   Create TestModule1\Private\
   Create TestModule1\Configuration\
Setting up support for GIT
   Create .gitignore
   Create README.md
   Create LICENSE.txt
Setting up support for Pester
   Verify The required module Pester (minimum version: 3.4.0) is already installed.
   Create Tests\
   Create Tests\TestModule1.tests.ps1
Setting up support for PPoShBuild
   Create build\
   Create build\build.ps1
   Create build\build.depend.psd1
   Create build\appveyor.yml
   Create build\PPoShScriptingStyle.psd1
   Create build\psake.ps1
Setting up Requirements.psd1 file for PPoShTools
   Create requirements.psd1
Setting up support for VSCode
   Create .vscode\settings.json
   Create .vscode\launch.json
Setting up Docs folder
   Create docs\Quick-Start-Installation-and-Example.md
   Create SomeTestModule1\Docs\New-Module-Create.md
PS C:\AdminTools>
PS C:\AdminTools> Set-Location $DestinationPath
PS C:\AdminTools\ModuleTest1> tree /F
Folder PATH listing for volume Windows
C:.
│   .gitignore
│   LICENSE.txt
│   README.md
│   requirements.psd1
│
├───.vscode
│       launch.json
│       settings.json
│
├───build
│       appveyor.yml
│       build.depend.psd1
│       build.ps1
│       PPoShScriptingStyle.psd1
│       psake.ps1
│
├───docs
│       Quick-Start-Installation-and-Example.md
│
├───TestModule1
│   │   TestModule1.psd1
│   │   TestModule1.psm1
│   │
│   ├───Configuration
│   ├───Docs
│   │       New-Module-Create.md
│   │
│   ├───Private
│   └───Public
└───Tests
        TestModule1.tests.ps1

```
---
## Now you're ready to commit your module to Git