# ocio-configs
Experimental OpenColorIO v2 configs

These configs and utilities are free to download for your own use, but should be considered as "alpha" status. They are just my own experiments, made public for others to look at. No guarantees are provided that they will behave as expected, and you should test the results for yourself.

### aces-0.1.1-ns
A configuration based on the [ACES Reference Config v0.1.1](https://github.com/AcademySoftwareFoundation/OpenColorIO-Config-ACES/releases/tag/v0.1.1). The changes are primarily to reduce the list of view transforms to a more manageable size for use in Nuke, and to add Apple Display P3, including EDR support. A custom SSTS based 500 nit Output Transform is also included for Apple EDR displays such as the 16 inch MacBook Pro.

**Note:** `Display - Apple Display P3` was originally created using the piecewise sRGB transfer function, as specified in the *Display P3* ICC profile. However, since I have measured the EOTF of my 2016 MacBook Pro as being pure gamma 2.2, I commented out the piecewise EOTF line (265) and replaced it with 2.2 gamma. This gives a better match to my BT.1886 monitor.

### studio-config-ns
A configuration based on the [ACES Studio Config v1.0.0](https://github.com/AcademySoftwareFoundation/OpenColorIO-Config-ACES/releases/tag/v1.0.0). The only change is the addition of an HDR capable `Apple Display P3 - Display` space. Unlike the previous config, this uses the two part sRGB EOTF, for compatibility with Macs with XDR displays set to `HDR Video (P3-ST 2084)`.

**Note:** For EDR or XDR display, `gl buffer depth` in Nuke must be set to at least half-float.

### utilities
- EDR Convert Gizmo - A Nuke gizmo for Mac systems with EDR or XDR displays, which converts image data in various output-referred forms (PQ / BT.1886 / HLG) for correct display on the Mac monitor (within limitations for EDR displays).

## About
Copyright Nick Shaw (Antler Post) – [nick@antlerpost.com](mailto:nick@antlerpost.com)


Original Config Copyright Contributors to the OpenColorIO Project – [ocio-dev@lists.aswf.io](mailto:ocio-dev@lists.aswf.io)

This software is released under terms of New BSD License: [https://opensource.org/licenses/BSD-3-Clause](https://opensource.org/licenses/BSD-3-Clause)