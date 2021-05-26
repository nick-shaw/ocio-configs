# ocio-configs
Experimental OpenColorIO v2 configs

These configs are free to download for your own use, but should be considered as "alpha" status. They are just my own experiments, made public for others to look at. No guarantees are provided that they will behave as expected, and you should test the results for yourself.

## aces-0.1.1-ns
A configuration based on the [ACES Reference Config v0.1.1](https://github.com/AcademySoftwareFoundation/OpenColorIO-Config-ACES/releases/tag/v0.1.1). The changes are primarily to reduce the list of view transforms to a more manageable size for use in Nuke, and to add Apple Display P3, including EDR support. A custom SSTS based 500 nit Output Transform is also included for Apple EDR displays such as the 16 inch MacBook Pro.