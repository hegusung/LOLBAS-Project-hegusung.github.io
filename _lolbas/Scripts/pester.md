---
Name: Pester.bat
Description: Used as part of the Powershell pester
Author: 'Oddvar Moe'
Created: 2018-05-25
Commands:
  - Command: Pester.bat [/help|?|-?|/?] "$null; notepad"
    Description: Execute code using Pester. The third parameter can be anything. The fourth is the payload. Example here executes notepad
    Usecase: Proxy execution
    Category: Execute
    Privileges: User
    MitreID: T1216
    OperatingSystem: Windows 10, Windows 11
    Tags:
      - Execute: EXE
  - Command: Pester.bat ;calc.exe
    Description: Execute code using Pester. Example here executes calc.exe
    Usecase: Proxy execution
    Category: Execute
    Privileges: User
    MitreID: T1216
    OperatingSystem: Windows 10, Windows 11
    Tags:
      - Execute: EXE
Full_Path:
  - Path: c:\Program Files\WindowsPowerShell\Modules\Pester\<version>\bin\Pester.bat
Code_Sample:
  - Code:
Detection:
  - Sigma: https://github.com/SigmaHQ/sigma/blob/683b63f8184b93c9564c4310d10c571cbe367e1e/rules/windows/process_creation/proc_creation_win_lolbin_pester_1.yml
Resources:
  - Link: https://twitter.com/Oddvarmoe/status/993383596244258816
  - Link: https://twitter.com/_st0pp3r_/status/1560072680887525378
  - Link: https://twitter.com/_st0pp3r_/status/1560072680887525378
Acknowledgement:
  - Person: Emin Atac
    Handle: '@p0w3rsh3ll'
  - Person: Stamatis Chatzimangou
    Handle: '@_st0pp3r_'
---
