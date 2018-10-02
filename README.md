# PlasterModuleTemplate
Template for module creation with Plaster

# How to create new module
---

```powershell
$PlasterTemplatePath = 'Path to PPoshModule template folder' #Path to where you've downloaded this module
$DestinationPath = 'C:\AdminTools\ModuleTest1' #Path to your git repository folder
Invoke-Plaster -TemplatePath $PlasterTemplatePath -DestinationPath $DestinationPath
```

```
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

## Manual steps
---
After the folder structure is created, insert GUID of your module in line 27 of your module Tests (Tests\TestModule1.tests.ps1 in this example)
 