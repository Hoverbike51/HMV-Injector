# HMV DLL Injector

A .NET 8 Windows injector using a Control Panel design. It only accepts DLLs listed in a manifest signed by HoverMods Vault.

![Cover](Images/HMV_Injector.png)
<p align="center">
<a href="https://www.patreon.com/cw/Hoverbike" rel="nofollow"><img src="https://camo.githubusercontent.com/0446eb970c25513ae0355aed04dce08e9f0d532218eb2fb0f85f34ff7e709e78/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f537570706f72742d50617472656f6e2d6f72616e67653f7374796c653d666f722d7468652d6261646765266c6f676f3d70617472656f6e266c696e6b3d68747470732533412532462532467777772e70617472656f6e2e636f6d2532466377253246486f76657262696b65" alt="Support on Patreon" data-canonical-src="https://img.shields.io/badge/Support-Patreon-orange?logo=patreon&amp;style=for-the-badge" style="max-width: 100%;"></a>
<a href="https://hoverbike.crd.co" rel="nofollow"><img src="https://camo.githubusercontent.com/7e9d281630cdbbe82bf13b2a45a82d899cbe91b925242b61e47ab03521e6bf22/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f486f76657262696b652d576562736974652d7465616c3f7374796c653d666f722d7468652d6261646765266c6f676f3d6361727264266c696e6b3d6874747073253341253246253246686f76657262696b652e6372642e636f" alt="Hoverbike's Website" data-canonical-src="https://img.shields.io/badge/Hoverbike-Website-teal?style=for-the-badge&logo=carrd" style="max-width: 100%;"></a>
</p>

## Features

- executable selection and active-process detection;
- target selection lock while its PID is running;
- x64 architecture validation;
- SHA-256 and ECDSA P-256 manifest-signature verification;
- explicit `LoadLibraryW` injection;
- lightweight single-EXE publishing;
- local timestamped `HoverMods.DLLInjector.log` file;
- HoverMods Vault branding and a subtle optional visual enhancement.

The **Inject DLL** button remains disabled until the process, architecture, manifest, and exact hash have been validated.

## Quick Start

1. Place `HoverMods.TrustedDlls.json` next to the injector or the DLL.
2. Start `HoverMods.DLLInjector.exe`.
3. Choose the target executable with **Select EXE**.
4. Start the target application. EXE selection is then locked until that PID exits.
5. Select the DLL and confirm that the status reads **HOVERMODS VERIFIED**.
6. Use **Inject DLL**.

## Antivirus Notice

Injection APIs are also used by malicious software, so heuristic detections remain possible, especially for unsigned binaries.

See [CHANGELOG.md](CHANGELOG.md) for the version history.
