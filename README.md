# HMV DLL Injector

A .NET 8 Windows injector using a Control Panel design. It only accepts DLLs listed in a manifest signed by HoverMods Vault.

![Cover](Images/HMV_Injector.png)
<p align="center">
<a href="https://www.patreon.com/cw/Hoverbike" rel="nofollow"><img src="https://camo.githubusercontent.com/0446eb970c25513ae0355aed04dce08e9f0d532218eb2fb0f85f34ff7e709e78/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f537570706f72742d50617472656f6e2d6f72616e67653f7374796c653d666f722d7468652d6261646765266c6f676f3d70617472656f6e266c696e6b3d68747470732533412532462532467777772e70617472656f6e2e636f6d2532466377253246486f76657262696b65" alt="Support on Patreon" data-canonical-src="https://img.shields.io/badge/Support-Patreon-orange?logo=patreon&amp;style=for-the-badge" style="max-width: 100%;"></a>
<a href="https://hoverbike.crd.co" rel="nofollow"><img src="https://camo.githubusercontent.com/7e9d281630cdbbe82bf13b2a45a82d899cbe91b925242b61e47ab03521e6bf22/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f486f76657262696b652d576562736974652d7465616c3f7374796c653d666f722d7468652d6261646765266c6f676f3d6361727264266c696e6b3d6874747073253341253246253246686f76657262696b652e6372642e636f" alt="Hoverbike's Website" data-canonical-src="https://img.shields.io/badge/Hoverbike-Website-teal?style=for-the-badge&logo=carrd" style="max-width: 100%;"></a>
</p>

## Features

- Executable selection and active-process detection;
- Target selection lock while its PID is running;
- x64 architecture validation;
- SHA-256 and ECDSA P-256 manifest-signature verification;
- Explicit `LoadLibraryW` injection;
- Lightweight single-EXE publishing;
- Local timestamped `HoverMods.DLLInjector.log` file;
- HoverMods Vault branding and a subtle optional visual enhancement.

The **Inject DLL** button remains disabled until the process, architecture, manifest, and exact hash have been validated.<br>

## Requirements

It need **.NET 8 Desktop Runtime x64**<br>
Open Powershell and do:
```powershell
winget install Microsoft.DotNet.DesktopRuntime.8
```
or
<a href="https://builds.dotnet.microsoft.com/dotnet/WindowsDesktop/8.0.31/windowsdesktop-runtime-8.0.31-win-x64.exe" rel="nofollow"><img src="https://camo.githubusercontent.com/ccb7ac3b628723e1292ef6049956f4b9a83ac4fbfa73f999a8ba4c388b93266c/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f446f776e6c6f61642d2e4e6574253230382d707572706c653f7374796c653d666f722d7468652d6261646765266c696e6b3d68747470732533412532462532466275696c64732e646f746e65742e6d6963726f736f66742e636f6d253246646f746e657425324657696e646f77734465736b746f70253246382e302e333125324677696e646f77736465736b746f702d72756e74696d652d382e302e33312d77696e2d7836342e657865" alt=".NET 8 Download" data-canonical-src="https://img.shields.io/badge/Download-.Net%208-purple?style=for-the-badge" style="max-width: 100%;"></a>


## Quick Start

1. Place `HoverMods.TrustedDlls.json` next to the injector or the DLL.
2. Start `HoverMods.DLLInjector.exe`.
3. Choose the target executable with **Select EXE**.
4. Start the target application. EXE selection is then locked until that PID exits.
5. Select the DLL and confirm that the status reads **HOVERMODS VERIFIED**.
6. Use **Inject DLL**.

## Trusted DLLs List

HMV Injector can only load trusted DLLs, but you are free to use any other injector to load DLLs, including mine<br>

### DragonSword Awakening
- `DSTool.ABlock.dll`<br>*(Prevent Abnormal gameplay to close the game)* INCLUDED
- `DSTool.dll`<br>*(MEGA CHEAT All in One)* Available [Here](https://github.com/lengkonglovelife/DStools-inject/releases)
<br>
## Antivirus Notice

Injection APIs are also used by malicious software, so heuristic detections remain possible, especially for unsigned binaries.

See [CHANGELOG.md](CHANGELOG.md) for the version history.
