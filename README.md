# MSVC toolchain catalog

A list of public GitHub repositories that preserve Microsoft Visual C++ toolchains, from
VC++ 1.0 (16-bit) to Visual Studio 2012: what each one contains (CRT, MFC and ATL sources,
`cl.exe`, Windows headers) and which build it is.

### 16-bit (VC++ 1.x)

| Repository | Product | Versions | CRT\SRC | CRT headers | MFC src | ATL | cl.exe | Windows headers | Notes |
| --- | --- | --- | --- | --- | --: | --: | --- | --- | --- |
| [archaic-toolchains/msvc10](https://github.com/archaic-toolchains/msvc10) | VC++ 1.0 | 16-bit | None | - | 238 | 0 | yes | `include` |  |
| [archaic-toolchains/msvc15](https://github.com/archaic-toolchains/msvc15) | VC++ 1.5 | 16-bit | None | internal.h | 191 | 0 | yes | `include` | Has an unrelated 16-bit internal.h only. |
| [archaic-toolchains/msvc152](https://github.com/archaic-toolchains/msvc152) | VC++ 1.52 | 16-bit | None | - | 0 | 0 | yes | `include` |  |

### VC++ 2.0

| Repository | Product | Versions | CRT\SRC | CRT headers | MFC src | ATL | cl.exe | Windows headers | Notes |
| --- | --- | --- | --- | --- | --: | --: | --- | --- | --- |
| [archaic-msvc/msvc200](https://github.com/archaic-msvc/msvc200) | VC++ 2.0 | cl 9.00 (README product line says 4.10) | None | - | 191 | 0 | yes | `include` |  |

### VC++ 4.x / 5.0

| Repository | Product | Versions | CRT\SRC | CRT headers | MFC src | ATL | cl.exe | Windows headers | Notes |
| --- | --- | --- | --- | --- | --: | --: | --- | --- | --- |
| [archaic-msvc/msvc400](https://github.com/archaic-msvc/msvc400) | VC++ 4.0 | cl 10.00.5270; link 3.00.5270 | Other version's (1397) | all 3, different vs SP6 | 299 | 0 | yes | `include` | Not VC6 headers: _tiddata etc. differ. |
| [archaic-toolchains/msvc400](https://github.com/archaic-toolchains/msvc400) | VC++ 4.0 (full media tree) | cl 10.00.5270 | None | - | 279 | 0 | yes | `include` |  |
| [itsmattkc/MSVC400](https://github.com/itsmattkc/MSVC400) | VC++ 4.0 | 4 | None | - | 279 | 0 | yes | `include` |  |
| [archaic-msvc/msvc410](https://github.com/archaic-msvc/msvc410) | VC++ 4.1 | c1xx 10.10.6038 | None | - | 307 | 0 | yes | `include` |  |
| [archaic-msvc/msvc420](https://github.com/archaic-msvc/msvc420) | VC++ 4.2 | c1xx 10.20.6166 | None | - | 293 | 0 | yes | `include` |  |
| [itsmattkc/MSVC420](https://github.com/itsmattkc/MSVC420) | VC++ 4.2 | 4.2 | None | - | 293 | 0 | yes | `include` | Used by the LEGO Island decomp. |
| [archaic-msvc/msvc500](https://github.com/archaic-msvc/msvc500) | VC++ 5.0 | 5.00.7022 / cl 11.00.7022 | None | - | 316 | 14 | yes | `include` |  |
| [archaic-msvc/msvc500sp1](https://github.com/archaic-msvc/msvc500sp1) | VC++ 5.0 SP1 | cl 11.00.7022; link 5.02.7132 | Other version's (98) | all 3, different vs SP6 | 316 | 14 | yes | `include` | Has the three headers (VC5 versions). |
| [archaic-msvc/msvc500sp2](https://github.com/archaic-msvc/msvc500sp2) | VC++ 5.0 SP2 | cl 11.00.7022; link 5.02.7132 | Other version's (98) | all 3, different vs SP6 | 316 | 14 | yes | `include` | Has the three headers (VC5 versions). |
| [archaic-msvc/msvc500sp3](https://github.com/archaic-msvc/msvc500sp3) | VC++ 5.0 SP3 | README copied from 5.0 RTM | Other version's (98) | all 3, different vs SP6 | 316 | 14 | yes | `include` | Has the three headers (VC5 versions). |

### VC++ 6.0

| Repository | Product | Versions | CRT\SRC | CRT headers | MFC src | ATL | cl.exe | Windows headers | Notes |
| --- | --- | --- | --- | --- | --: | --: | --- | --- | --- |
| [HorvathAlteisen/msvc600sp6](https://github.com/HorvathAlteisen/msvc600sp6) | VC++ 6.0 SP6 Enterprise | cl 12.00.8804; c1/c1xx/c2 12.00.9782; link 6.00.8447 | Best: full SP6 (1266) | all 3, identical vs SP6 | 312 | 19 | yes | `include` | VS98 Enterprise CD1 + Vs6sp6.exe overlay (SHA-256 in README). All paths lower case; 8.3 names renamed as Setup does. Its 20 SP6 CRT files match itsmattkc/MSVC600 byte for byte. |
| [isledecomp/MSVC600-8168](https://github.com/isledecomp/MSVC600-8168) | VC++ 6.0 RTM | cl 12.00.8168; link 6.00.8168 (README heading says 8804) | Full VC6 (1267) | all 3, identical vs SP6 | 333 | 20 | yes | `vc98/include` | Adds msvc-wine wrappers and CMake notes. Keeps CD 8.3 names (ALGRITHM, MAKEFILE, ...). |
| [archaic-toolchains/msvc600_sp1](https://github.com/archaic-toolchains/msvc600_sp1) | VC++ 6.0 SP1 | cl 12.00.8168 | Full VC6 (1267) | all 3, identical vs SP6 | 324 | 20 | yes | `vc98/include` | RTM CD1 CRT sources + SP1 fixes taken from the SP2 payload (SP1 itself is not preserved). |
| [archaic-toolchains/msvc600_sp2](https://github.com/archaic-toolchains/msvc600_sp2) | VC++ 6.0 SP2 | cl 12.00.8168 | Full VC6 (1281) | all 3, identical vs SP6 | 327 | 20 | yes | `vc98/include` | RTM CD1 + official SP2 disc payload. Has a stray duplicate vc98/crt/crt/src (15 files). |
| [archaic-toolchains/msvc600_sp3](https://github.com/archaic-toolchains/msvc600_sp3) | VC++ 6.0 SP3 (with Bin) | cl 12.00.8168 | Full VC6 (1267) | all 3, identical vs SP6 | 333 | 20 | yes | `vc98/include` | archaic-msvc/msvc600_sp3 plus VC98/Bin from the decomp.me msvc6.3 tarball. |
| [archaic-toolchains/msvc600_sp4](https://github.com/archaic-toolchains/msvc600_sp4) | VC++ 6.0 SP4 (with Bin) | cl 12.00.8804 | Full VC6 (1267) | all 3, identical vs SP6 | 333 | 20 | yes | `vc98/include` | archaic-msvc/msvc600_sp4 plus Bin from decomp.me msvc6.4 (README: sha-verified against the SP4 CD). |
| [archaic-msvc/msvc600_sp3](https://github.com/archaic-msvc/msvc600_sp3) | VC++ 6.0 SP3 (headers/libs) | README: product 6.00.8447, c1xx 12.00.8168 | Full VC6 (1267) | all 3, identical vs SP6 | 333 | 20 | no | `vc98/include` | No cl.exe in the tree. Old name: ifarbod/msvc600_sp3. |
| [archaic-msvc/msvc600_sp4](https://github.com/archaic-msvc/msvc600_sp4) | VC++ 6.0 SP4 (headers/libs) | README: cl 12.00.8804, link 6.00.8447 | Full VC6 (1267) | all 3, identical vs SP6 | 333 | 20 | no | `vc98/include` | No cl.exe in the tree. |
| [archaic-msvc/msvc600](https://github.com/archaic-msvc/msvc600) | VC++ 6.0 RTM (stripped) | 6.0.8168 / c1xx 12.0.8168 | None | - | 320 | 20 | yes | `vc98/include` | Mirror: ifarbod/msvc600. |
| [archaic-msvc/msvc600_sp5](https://github.com/archaic-msvc/msvc600_sp5) | VC++ 6.0 SP5 | README: 6.0.8968 / c1xx 12.0.8968 | SP overlay only (19) | - | 320 | 20 | yes | `vc98/include` | Only the SP-updated CRT files. Mirror: ifarbod/msvc600_sp5. |
| [archaic-msvc/msvc600_sp5_vcpp](https://github.com/archaic-msvc/msvc600_sp5_vcpp) | VC++ 6.0 SP5 + Processor Pack | (no README) | SP overlay only (20) | - | 320 | 20 | yes | `vc98/include` |  |
| [archaic-msvc/msvc600_sp6](https://github.com/archaic-msvc/msvc600_sp6) | VC++ 6.0 SP6 | (no README) | SP overlay only (21) | - | 320 | 20 | yes | `vc98/include` | Its 21 CRT\SRC files are identical to itsmattkc/MSVC600's. Mirror: ifarbod/msvc600_sp6. |
| [itsmattkc/MSVC600](https://github.com/itsmattkc/MSVC600) | VC++ 6.0 SP6 Professional | SP6 (last commit: 'upgraded to professional edition sp6') | SP overlay only (21) | - | 320 | 20 | yes | `vc98/include` | Same 21-file CRT\SRC as archaic-msvc/msvc600_sp6. |

### VS .NET 2002 to VS 2012

| Repository | Product | Versions | CRT\SRC | CRT headers | MFC src | ATL | cl.exe | Windows headers | Notes |
| --- | --- | --- | --- | --- | --: | --: | --- | --- | --- |
| [archaic-msvc/msvc700](https://github.com/archaic-msvc/msvc700) | VS .NET 2002 | 7.00.9466 / c1xx 13.00.9466 | Other version's (1278) | all 3, different vs SP6 | 294 | 79 | yes | `vc7/platformsdk` | Includes Vc7/PlatformSDK. |
| [archaic-msvc/msvc700_sp1](https://github.com/archaic-msvc/msvc700_sp1) | VS .NET 2002 SP1 | README: 7.00.9955 | Other version's (1278) | all 3, different vs SP6 | 294 | 79 | yes | `vc7/platformsdk` | Includes Vc7/PlatformSDK. |
| [archaic-msvc/msvc710](https://github.com/archaic-msvc/msvc710) | VS .NET 2003 | 7.10.3077 / c1xx 13.10.3077 | Other version's (1225) | all 3, different vs SP6 | 286 | 81 | yes | `vc7/platformsdk` | Includes Vc7/PlatformSDK. |
| [archaic-msvc/msvc710_sp1](https://github.com/archaic-msvc/msvc710_sp1) | VS .NET 2003 SP1 | README: 7.10.9955 (IDE 7.10.6030) | Other version's (1225) | all 3, different vs SP6 | 286 | 81 | yes | `vc7/platformsdk` | Includes Vc7/PlatformSDK. Mirror: ifarbod/msvc710_sp1. |
| [archaic-msvc/msvc800](https://github.com/archaic-msvc/msvc800) | VS 2005 | cl 14.00.50727.42 | Other version's (1370) | all 3, different vs SP6 | 309 | 85 | yes | `vc/platformsdk` | Includes VC/PlatformSDK. |
| [archaic-msvc/msvc800_sp1](https://github.com/archaic-msvc/msvc800_sp1) | VS 2005 SP1 | (no README) | Other version's (1372) | all 3, different vs SP6 | 310 | 85 | yes | `vc/platformsdk` | Includes VC/PlatformSDK. |
| [widberg/msvc8.0](https://github.com/widberg/msvc8.0) | VS 2005 VC80 x86 | VS2005 Pro media | None | - | 0 | 85 | yes | `platformsdk` | Includes PlatformSDK/ and atlmfc/ (no MFC source). |
| [archaic-msvc/msvc900](https://github.com/archaic-msvc/msvc900) | VS 2008 | c1xx 15.00.21022.08 | Other version's (1522) | all 3, different vs SP6 | 319 | 61 | yes | `microsoft sdks/windows/v6.0a/include` | Includes Microsoft SDKs/Windows/v6.0A. |
| [archaic-toolchains/msvc900_sp1](https://github.com/archaic-toolchains/msvc900_sp1) | VS 2008 SP1 | 15.00.30729 | Other version's (1522) | all 3, different vs SP6 | 319 | 61 | yes | `microsoft sdks/windows/v6.0a/include` | Includes Windows SDK v6.0A. |
| [archaic-msvc/msvc1000](https://github.com/archaic-msvc/msvc1000) | VS 2010 | 16 | Other version's (1302) | all 3, different vs SP6 | 476 | 63 | yes | `microsoft sdks/windows/v7.0a/include` | Includes Microsoft SDKs/Windows/v7.0A. |
| [archaic-msvc/msvc1000_sp1](https://github.com/archaic-msvc/msvc1000_sp1) | VS 2010 SP1 | 16.00 SP1 | Other version's (1303) | all 3, different vs SP6 | 478 | 63 | yes | `microsoft sdks/windows/v7.0a/include` | Includes Windows SDK v7.0A. |
| [archaic-msvc/msvc1100](https://github.com/archaic-msvc/msvc1100) | VS 2012 | cl 17.00.50522.1 | Other version's (1444) | all 3, different vs SP6 | 479 | 59 | yes | `windows kits/8.0/include/um` | Includes Windows Kits/8.0. |

### Multi-version collections

| Repository | Product | Versions | CRT\SRC | CRT headers | MFC src | ATL | cl.exe | Windows headers | Notes |
| --- | --- | --- | --- | --- | --: | --: | --- | --- | --- |
| [nolffan/toolchains](https://github.com/nolffan/toolchains) | VC5 7303, VC6 8168/8447/8966/9782, VC7.1 3077, ICL 4-9, DX8.1 SDK, 3ds Max SDKs | per folder | SP overlay only (21) | - | 320 | 101 | yes | `msvc-7.10-3077/platformsdk` | fetch.sh rebuilds some trees from archive.org media. The VC7.1 tree includes PlatformSDK/. |

## Thanks

Thanks to everyone who preserved these toolchains and shared them:
[HorvathAlteisen](https://github.com/HorvathAlteisen),
[isledecomp](https://github.com/isledecomp),
[archaic-toolchains](https://github.com/archaic-toolchains),
[archaic-msvc](https://github.com/archaic-msvc) / [ifarbod](https://github.com/ifarbod),
[itsmattkc](https://github.com/itsmattkc),
[nolffan](https://github.com/nolffan) and
[widberg](https://github.com/widberg).
