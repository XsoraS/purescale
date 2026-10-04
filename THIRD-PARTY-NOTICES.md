# Third-party notices

The release packages include NVIDIA Streamline, DLSS, DLSS Frame Generation, Reflex and AMD FidelityFX runtime libraries used by PureScale's native features. These are vendor binaries and retain their respective licenses.

| Files | Notices |
| --- | --- |
| `sl.*.dll` | NVIDIA Streamline license and third-party notices |
| `nvngx_dlss.dll`, `nvngx_dlssg.dll` | NVIDIA RTX / DLSS and NGX licenses |
| `NvLowLatencyVk.dll` | NVIDIA Reflex license |
| `amd_fidelityfx_*.dll` | AMD FidelityFX license |
| `purescale_*.dll` | PureScale's original bridge code, CC0 1.0 |

Keep the files in `licenses` with these binaries when redistributing them. Runtime ZIPs include their own copy of the notices. The optional original Neural Rendering runtime is excluded.
