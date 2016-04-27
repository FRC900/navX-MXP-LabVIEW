# Contributing to the navX LabVIEW Library
The FIRST Robotics Community is a great resource for help and it is what makes the games enjoyable year after year.

## Install GitHub Desktop for Windows
[GitHub Desktop](https://desktop.github.com/)

## Git(Hub) and LabVIEW
Making LabVIEW work with Git is not as simple as it is with text based languages.
Pulled from [Revision Control with Git for FRC Teams](https://docs.google.com/document/pub?id=1Lmx9WI1g_ObB03Vrlfb7QU3ochz1q_YRGM8dPi0R8g8).
#### Enabling Merge and Diff for LabVIEW
```
git config --system merge.labview.name "LabView 3-Way Merge"
git config --system merge.labview.driver '"C:\Program Files\National Instruments\Shared\LabVIEW Merge\LVMerge.exe" "C:\Program Files\National Instruments\LabVIEW 8.6\LabVIEW.exe" %O %B %A %A'
git config --system merge.labview.recursive binary
git config --system diff.labview.command '"C:\Program Files\National Instruments\LabVIEW 8.6\LabVIEW.exe" "C:\path\to\diff.vi" --'
```
__If using Powershell__
```
git config --system merge.labview.name "LabView 3-Way Merge"
git config --system merge.labview.driver "\`"C:\Program Files\National Instruments\Shared\LabVIEW Merge\LVMerge.exe\`" \`"C:\Program Files\National Instruments\LabVIEW 8.6\LabVIEW.exe\`" %O %B %A %A"
git config --system merge.labview.recursive binary
git config --system diff.labview.command "\`"C:\Program Files\National Instruments\LabVIEW 8.6\LabVIEW.exe\`" \`"C:\path\to\diff.vi\`" --"
```

#### .gitattributes
```
# Use a custom driver to diff merge LabVIEW files
*.vi merge=labview diff=labview
```