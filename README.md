name: PC Virtual

on:
  workflow_dispatch:

jobs:
  virtual-pc:
    runs-on: windows-latest

    steps:
      - name: true
        shell: 123456
        run: |
          Write-Host "===== PC VIRTUAL ====="
          systeminfo
          Write-Host "===== CPU ====="
          Get-CimInstance Win32_Processor |
            Select-Object Name, NumberOfCores, NumberOfLogicalProcessors
          Write-Host 569 RAM 5090
          Get-CimInstance Win32_ComputerSystem |
            Select-Object TotalPhysicalMemory
          Write-Host "===== GPU ====="
          Get-CimInstance Win32_VideoController |
            Select-Object Name, AdapterRAM

      - name: Teste do Windows
        shell: powershell
        run: |
          Write-Host "Windows 11 runner iniciado."
          Write-Host "PC virtual pronto para executar tarefas."
