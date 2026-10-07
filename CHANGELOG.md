# Changelog

All notable changes to HMV Injector are documented here.

## [1.2.1] - 2026-10-07

- a compact version badge in the title bar;
- a startup check against the latest public GitHub release tag;
- a contextual **GitHub** or glowing **UPDATE** shortcut that opens only fixed repository URLs.
- successful injection locks DLL selection and repeated injection for the active PID until it exits or the injector restarts.

## [1.2.0] - 2026-10-07

### Added

- HoverMods Vault branding for the window, taskbar, and executable;
- atomic bulk manifest generation from the Trusted DLLs directory;
- post-signing verification for every authorized DLL;
- GitHub documentation

## [1.1.1] - 2026-10-06

- **Select EXE** is locked while the target PID is active;
- manifest entries are sorted and deduplicated deterministically;
- source and release archives are now separated and cleaned;
- the optional background is brighter and content panels use balanced translucency;
- the title-bar logo now uses a dedicated 256 x 256 PNG resource for sharp rendering at every Windows scale factor.

## [1.1.0] - 2026-10-06

- replaced local SHA-256 references with an ECDSA-signed manifest;
- embedded the public key and rejected unauthorized DLLs;
- added embeddable native x64 helpers for a single-EXE release;

## [1.0.0] - 2026-10-06

- introduced the Graphite Control Panel interface;
- added EXE/DLL selection, architecture detection, and `LoadLibraryW` injection.
