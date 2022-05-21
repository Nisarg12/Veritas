## About
Tired of always having to look up different versions of file structures & manually mapping the bytes while working with hex?

#### Veritas - Veraciously Effective Renderer In-All Typical Artifact Structures
is an elementary WIP hex **viewer** made for forensicators, which automatically identifies different artifacts and applies the correct template. These templates are generated dynamically to accurately highlight data with appropriate color markers.

#### Last Still
![Screenshot.png](https://raw.githubusercontent.com/Nisarg12/Veritas/main/images/Screenshot.png?)

## Disclaimer
Veritas is not meant to be an advanced hex viewer with functionalities that a real hex editor might have. It **solely** aims for one thing, convenience for data validation. It is suggested that this hex viewer be used in accordance with other good hex editors that offer searching and goto functions. Over time, Veritas will support more file structures; but as of now I'm the only one working on this project when I'm able to.

## Features
* Identify the artifact and load the appropriate template.
* View color coded artifact file structure with sub-sections.
* TODO: Multiple tabs.
* TODO: Finish popups.

## Supported Artifacts
* Prefetch: XP, Vista, 7, 8.1, 10, 11
* TODO: $MFT
* TODO: Registry files
* TODO: Images: png, jpeg, jpg, bmp, gif
* TODO: Documents: pdf

## Requirements
* Python >= 3.10.4
* Kivy >= 2.1.0

## Installation
**Step 1**: Create a virtual environment using:
```python
python3 -m venv veritas
```

**Step 2**: Depending on your OS, activate the virtual environment using:
* Windows: `.\veritas\Scripts\activate`
* Linux: `source veritas/Scripts/activate`

**Step 3**: Install kivy using:
```python
python3 -m pip install "kivy[base]"
```

## Special Thanks
* [Gary Kessler](https://www.linkedin.com/in/garykessler)'s [File Signatures Table](https://www.garykessler.net/library/file_sigs.html), for the very handy cheatsheet for various file signatures.
* [Andrew Rathbun](https://twitter.com/bunsofwrath12)'s [DFIRArtifactMuseum](https://github.com/AndrewRathbun/DFIRArtifactMuseum), for providing numerous artifact samples to validate proper parsing.
* [Forensics Wiki](https://forensicswiki.xyz/page/Main_Page), for additional information on file structures.
* [Libscaa](https://github.com/libyal/libscca), for the prefetch file structure documentation.
* [el3phanten](https://github.com/el3), for invaluable assistance in kivy.