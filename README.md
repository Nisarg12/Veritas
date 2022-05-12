## About:
Tired of always having to look up different versions of file structures while working with hex?

Veritas (Veraciously Effective Renderer Inspecting Typical Artifact Structures) is an elementary and WIP hex **viewer** made for forensicators, which automatically identifies different artifacts and applies the correct template. These templates are generated dynamically to accurately highlight data with appropriate color markers.

## Features:
* Identify the artifact and apply it's template.
* View artifact file structure.
* TODO: Multiple tabs.
* TODO: Finish popups.
* TODO: Implement template loader.

## Supported Artifacts:
* Prefetch: XP, Vista, 7, 8.1
* $MFT
* Registry files
* TODO: Images: png, jpeg, jpg, bmp, gif
* TODO: Documents: pdf

## Installation:
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

Built using python 3.10.4 and kivy 2.1.0