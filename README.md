# FlareVM-Installation ARM-Based MacBook (M1/M2/M3)

What is FLARE VM?

FLARE VM (FireEye Labs Advanced Reverse Engineering Virtual Machine) is a Windows-based security distribution specifically designed for malware analysis, reverse engineering, and penetration testing. It provides a pre-configured environment with numerous forensic, debugging, and reverse engineering tools, making it ideal for cybersecurity professionals and researchers.

Unlike Kali Linux, which is a Linux-based penetration testing OS, FLARE VM is built on Windows and focuses on Windows-based security assessments, malware debugging, and software analysis.

What Can You Do With FLARE VM?

With FLARE VM, cybersecurity analysts and malware researchers can:

✅ Reverse engineer malware using tools like IDA Free, Ghidra, x64dbg, and Radare2.

✅ Analyze Windows-based threats with static and dynamic malware analysis tools.

✅ Debug applications and explore executable files with OllyDbg, x64dbg, and WinDbg.

✅ Perform forensic investigations on compromised Windows systems.

✅ Test security vulnerabilities using tools tailored for penetration testing and exploit research.

✅ Decompile and analyze binaries for threat intelligence and security research.

How to Install FLARE VM on an ARM-Based MacBook (M1/M2/M3)

To install FLARE VM on an ARM-based Mac, follow the step-by-step screenshots provided in my GitHub repository. These screenshots will guide you through:
	•	Setting up a Windows 11 ARM virtual machine
	•	Installing FLARE VM using PowerShell
	•	Configuring necessary settings for optimal performance

Refer to my GitHub project page for detailed installation steps and screenshots to complete the setup.








## FLARE-VM installation (Instructions From Original GitHub Page)

* Open a PowerShell prompt as administrator
* Download the installation script installer.ps1 to your Desktop:
    * (New-Object net.webclient).DownloadFile('https://raw.githubusercontent.com/mandiant/flare-vm/main/install.ps1',"$([Environment]::GetFolderPath("Desktop"))\install.ps1")
* Unblock the installation script:
    * Unblock-File .\install.ps1
* Enable script execution:
    * Set-ExecutionPolicy Unrestricted -Force
        * If you receive an error saying the execution policy is overridden by a policy defined at a more specific scope, you may need to pass a scope in via Set-ExecutionPolicy Unrestricted -Scope CurrentUser -Force. To view execution policies for all scopes, execute Get-ExecutionPolicy -List
* Finally, execute the installer script as follow:
    * .\install.ps1
        * To pass your password as an argument: .\install.ps1 -password <password>
        * To use the CLI-only mode with minimal user interaction: .\install.ps1 -password <password> -noWait -noGui
        * To use the CLI-only mode with minimal user interaction and a custom config file: .\install.ps1 -customConfig <config.xml> -password <password> -noWait -noGui
* After installation it is recommended to switch to host-only networking mode and take a VM snapshot

