## About:
Tired of always having to look up different versions of file structures while working with hex?

**Veritas** - **V**eraciously **E**ffective **R**enderer **I**n-All **T**ypical **A**rtifact **S**tructures
> is an elementary WIP hex **viewer** made for forensicators, which automatically identifies different artifacts and applies the correct template. These templates are generated dynamically to accurately highlight data with appropriate color markers.

## Features:
* Identify the artifact and load it's template.
* View color coded artifact file structure.
* TODO: Multiple tabs.
* TODO: Finish popups.

## Supported Artifacts:
* Prefetch: XP, Vista, 7, 8.1, 10, 11
* $MFT
* Registry files
* TODO: Images: png, jpeg, jpg, bmp, gif
* TODO: Documents: pdf

## Requirements:
* Python >= 3.10.4
* Kivy >= 2.1.0

## Installation:
```python
python3 -m pip install "kivy[base]"
```

## Special Thanks:
* [Gary Kessler](https://www.linkedin.com/in/garykessler)'s [File Signatures Table](https://www.garykessler.net/library/file_sigs.html)
* [Andrew Rathbun](https://twitter.com/bunsofwrath12)'s [DFIRArtifactMuseum](https://github.com/AndrewRathbun/DFIRArtifactMuseum)
* [Forensics Wiki](https://forensicswiki.xyz/page/Main_Page)