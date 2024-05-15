# FullBypass
A tool which bypasses AMSI (AntiMalware Scan Interface) and PowerShell CLM (Constrained Language Mode) and gives you a FullLanguage PowerShell reverse shell.

```batch
P.S Please do not use in unethical hacking and follow all rules and regulations of laws
```

Usage:

First, Download the bypass.csproj file into the victim machine (Find writeable folder such as C:\Windows\Tasks or C:\Windows\Temp). After that just execute it with msbuild.exe.

Example: ```C:\Windows\Microsoft.NET\Framework64\v4.0.30319\msbuild.exe .\FullBypass.csproj```


After that the code will do 2 things.

1. Firstly code will bypass AMSI using memory hijacking method and will rewrite some instructions in AmsiScanBuffer function. With xor instruction the size argument will be 0 and AMSI cannot detect future scripts and command in powershell.

![image](https://github.com/Sh3lldon/FullBypass/assets/78950174/4a444b4d-cfd1-47fd-9cc7-b9e2b92a2f12)


2. Finally it will ask you your IP and port to give you a powershell FullLanguage Mode reverse shell.

![image](https://github.com/Sh3lldon/FullBypass/assets/78950174/5b6e609d-30aa-49ea-9fb1-ce5f82ff082e)



![image](https://github.com/Sh3lldon/FullBypass/assets/78950174/3b81ccdf-b5c9-450d-93f1-b89996a94aee)

As you can see we catch powershell FullLanguageMode reverse shell.
