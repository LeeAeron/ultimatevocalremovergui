# 🚀 UVR5 - Ultimate Vocal Remover GUI Portable Installer (nVidia GTX10xx-16xx and RTX20xx-50xx GPUs)
<img src="https://raw.githubusercontent.com/LeeAeron/ultimatevocalremovergui/main/gui_data/img/UVR.png?raw=true" />

[![Release](https://img.shields.io/github/release/LeeAeron/ultimatevocalremovergui.svg)](https://github.com/LeeAeron/ultimatevocalremovergui/releases/latest)


## 🔧 About

This application uses state-of-the-art source separation models to remove vocals from audio files. UVR's core developers trained all of the models provided in this package (except for the Demucs v3 and v4 4-stem models).

💠 **Core Developers**
    - [Anjok07](https://github.com/anjok07)
    - [aufr33](https://github.com/aufr33)
    - [LeeAeron](https://github.com/LeeAeron)


## ❇️ UVR5 models overview (Rus/Eng)
[UVR5 models overview (Rus/Eng)](https://github.com/LeeAeron/ultimatevocalremovergui/blob/main/UVR5_models.md) 


## Instalation

### 🖥️ Windows Installation

This UVR will be provided with only *.bat installer/re-installer/starter file, that will download and install all components and build Portable UVR.


➤ Please Note:
    - I'm supporting only nVidia GTX10xx-16xx and RTX20xx-50xx GPUs.
    - This installer is intended for those running Windows 10 or higher. 
    - Application functionality for systems running Windows 7 or lower is not guaranteed.

- Download the UVR .bat installer for Windows in releases.
- Place the BAT-file in any folder in the root of any partition with a short Latin name without spaces or special characters and run it.
- Select INSTALL (2) of .BAT menu for to install onto GTX10xx GPU or (3) to install onto GTX16xx/RTX20xx-50xx GPU.
- The .BAT file will download, prepare and install the fully portable version of UVR, with own FFMPEG, and ask you to restart the .BAT file. Press any key and restart the .BAT file.
- Run it via START (1).


### 🔥 Very important
- DOWNLOAD MODELS MANUALLY VIA THE SETTINGS MENU.

- Models folder: \UltimateVocalRemover\models. You can save them before reinstalling using step (2) or (3) of .BAT menu.

- Reinstalling using step (2) or (3) of .BAT menu WILL COMPLETELY DELETE ALL FOLDERS ON THE PORTABLE DEVICE, LEAVING ONLY THE .BAT FILE!


### 📦 Update

- Download latest .bat file in Releases, replace your old.
- Select UPDATE (4) entry from .BAT menu. UVR will be updated from this Git.
- Launch UVR as always.
➤ NOTE: If there's some files will be warned to be deleted from folders inside while update, please, delete them manually and repeat UPDATE (4) of .BAT menu.


### 🖥 Other Application Notes
- Nvidia GTX 1060 6GB is the minimum requirement for GPU conversions.
- Nvidia GPUs with at least 6GBs of V-RAM are recommended.
- This application is only compatible with 64-bit platforms. 
- This application relies on the Rubber Band library for the Time-Stretch and Pitch-Shift options.
- This application relies on FFmpeg to process non-wav audio files.
- The application will automatically remember your settings when closed.
- Conversion times will significantly depend on your hardware. 
- These models are computationally intensive. 


## ♻️ Changelog
[Changelog here](https://github.com/LeeAeron/ultimatevocalremovergui/blob/main/CHANGELOG.md) 


## 👉 Troubleshooting

### 🆘 Common Issues

- If FFmpeg is not installed, the application will throw an error if the user attempts to convert a non-WAV file.
- Memory allocation errors can usually be resolved by lowering the "Segment" or "Window" sizes.


### 🆘 Issue Reporting

Please be as detailed as possible when posting a new issue. 

If possible, click the "Settings Button" to the left of the "Start Processing" button and click the "Error Log" button for detailed error information that can be provided to us.


## 📝 License

The **Ultimate Vocal Remover GUI** code is [MIT-licensed](LICENSE). 
The **Apollo model** code is [CC-BY-SA 4.0](LICENSE). 

- **Please Note:** For all third-party application developers who wish to use our models, please honor the MIT license by providing credit to UVR and its developers.


## 📺 Credits
- [ZFTurbo](https://github.com/ZFTurbo) - Created & trained the weights for the new MDX23C models. 
- [DilanBoskan](https://github.com/DilanBoskan) - Your contributions at the start of this project were essential to the success of UVR. Thank you!
- [Bas Curtiz](https://www.youtube.com/user/bascurtiz) - Designed the official UVR logo, icon, banner, and splash screen.
- [tsurumeso](https://github.com/tsurumeso) - Developed the original VR Architecture code. 
- [Kuielab & Woosung Choi](https://github.com/kuielab) - Developed the original MDX-Net AI code. 
- [Adefossez & Demucs](https://github.com/facebookresearch/demucs) - Developed the original Demucs AI code. 
- [KimberleyJSN](https://github.com/KimberleyJensen) - Advised and aided the implementation of the training scripts for MDX-Net and Demucs. Thank you!
- [Hv](https://github.com/NaJeongMo/Colab-for-MDX_B) - Helped implement chunks into the MDX-Net AI code. Thank you!


## 🔖 References
- [1] Takahashi et al., "Multi-scale Multi-band DenseNets for Audio Source Separation", https://arxiv.org/pdf/1706.09588.pdf

