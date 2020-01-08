E3D tool changer slicer tools
===================================

Contains:
- Pre-compiled CuraEngine 4.4.1 with patch for better prime tower generation
- CURA 4.4 profiles for E3D tool changer optimized for Hemera toolheads
- E3D tool changer Duet 2 firmware
- STL files for purge buckets and accesories

CuraEngine 4.4.1 fork build
===================================
Includes:
- better prime tower generation (no skiped layers/priming in the 'air'), no extra tool changes

The new behaviour is:
```
- on tool change, check if the previous extruder has been primed, if not prime into the Prime Tower (avoid gaps)
- prime the new extruder (as before)
- at end of layer processing, check which extruders that have minimum prime tower volume, have not been primed
- use the last active extruder to plug the missing gaps in the prime tower

![Behaviour After Patch](https://github.com/mkudzia84/e3d-toolchanger-profiles/blob/master/after_patch.png)

To install:
- Go to the Ultimaker Cura 4.4 install folder
- Rename the CuraEngine.exe to CuraEngine.vanilla.exe
- Copy the Zipped CuraEngine.exe onto the folder.
- Restart the Cura if needed/
