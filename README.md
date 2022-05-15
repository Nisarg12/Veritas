## About
Tired of always having to look up different versions of file structures while working with hex?

#### Veritas - Veraciously Effective Renderer In-All Typical Artifact Structures
is an elementary WIP hex **viewer** made for forensicators, which automatically identifies different artifacts and applies the correct template. These templates are generated dynamically to accurately highlight data with appropriate color markers.

## Features
* Identify the artifact and load it's template.
* View color coded artifact file structure.
* TODO: Multiple tabs.
* TODO: Finish popups.

## Supported Artifacts
* Prefetch: XP, Vista, 7, 8.1, 10, 11
* $MFT
* Registry files
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

## How Can I Contribute?
1. **Programmers**: By writing a module `<artifact>.py` for an artifact that follows the given checklist:
- [x] Define the main function `<artifact>()` which defines a list and a variable **FOR EACH** section of the artifact file structure:
    * A list that contains the template data which is represented by an ordered pair `[x, y]` where `x` is the byte where the section starts in the file structure and `y` is the length in bytes until that section ends.
    * A variable that contains the size of the section.

    Note that because some sections of an artifact file structure might have dynamic sizing with no absolute identifiers that would indicate the beginning of a new section, you must write logic for seeking that part out. Many files are appended to which results in cases like these. If there are absolutely no surefire methods to determine that, parse the sections in reverse and leave out sections as few as possible.
- [x] Since, each section is defined by a relative offset for convenience in code review, use the `toAbsolute()` function defined in `offsetter.py` to convert the relative offsets to absolute ones. It will return a list which you can directly return to `loader.py`. Which also means that all sections should be accounted for their sizes in your `<artifact>()` function, prior to calling this function.
- [x] In `loader.py`, define a function `is<Artifact>()` which checks for the magic numbers of the artifact. Use this one-liner `magic = "".join(hexbytes[b] for b in range(start, end)).upper()` to define the magic bytes. Write logic for special cases or integrity checks if any. The function should return a boolean value.
- [x] Now, you must add a check for your `is<Artifact>()` function in the if-else ladder statement present right above the return statement in `loader.py`. The check should assign the value of the variable `pairlist` by calling your `<artifact>()` function that you defined earlier in `<artifact>.py`

2. **Testers**: By testing the freeware & reporting bugs found in rare corner cases.
3. **Designers**: By removing high contrast colors from `colors.py`, and sort them in a manner that no two consecutive colors are difficult to distinguish, i.e. they have high contrast between them.

## Special Thanks
* [Gary Kessler](https://www.linkedin.com/in/garykessler)'s [File Signatures Table](https://www.garykessler.net/library/file_sigs.html)
* [Andrew Rathbun](https://twitter.com/bunsofwrath12)'s [DFIRArtifactMuseum](https://github.com/AndrewRathbun/DFIRArtifactMuseum)
* [Forensics Wiki](https://forensicswiki.xyz/page/Main_Page)