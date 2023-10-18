# Nolvus AutoDL

When utilizing [Nexus Mods](https://nexusmods.com/) for Game Modding, the typical procedure involves manually clicking the download button each time a new mod is added to the download queue.
However, this manual process can become problematic when dealing with tools such as [Nolvus](https://www.nolvus.net/), which may involve numerous mods, potentially numbering in the hundreds or even thousands.

To address this issue, Nolvus AutoDL serves as an autoclicker designed to streamline and automate this process. While Nolvus AutoDL is active, it continuously monitors the screen for instances when a download button for a Nexus Mod(the "Slow Download" button) or Collections button from Vortex becomes visible.
In such cases, Nolvus AutoDL takes action by automatically clicking the download button, effectively removing the need for manual intervention. This automation significantly enhances the efficiency and convenience of the mod downloading experience.

## Note

Using a bot to download from Nexus is in direct violation of their TOS:

> Attempting to download files or otherwise record data offered through our services (including but not limited to the Nexus Mods website and the Nexus Mods API) in a fashion that drastically exceeds the expected average, through the use of software automation or otherwise, is prohibited without expressed permission. Users found in violation of this policy will have their account suspended.

Use this at your own risk.

## Download

Check [Releases](https://github.com/GreatWizard/nolvus-autodl/releases/)

## Building Nolvus-AutoDL

Install [Python 3](https://www.python.org/downloads/)

### upgrade pip

```
python -m pip install --upgrade pip
```

### Install required dependencies

```
pip install yapf
pip install mypy
pip install pyinstaller
pip install pillow
pip install pyautogui
pip install numpy
pip install click
pip install opencv-python==3.4.18.65
pip install opencv-contrib-python==3.4.18.65
python -m pip install types-Pillow
```

- Install Make from [GnuWin32](https://sourceforge.net/projects/gnuwin32/files/make/3.81/) and add the executable to PATH
- Navigate to folder with makefile
- Edit Makefile and add the Executables required inside
- Run in powershell

```
make all
```

or use

```
C://path//to//make.exe path//to//makefile
```

#### You can replace the images in templates folder and build the project in case nexus decides to change their download button currently it is working as intended to download off of Nolvus.

#### Current code requires python3 use opencv version 3.4 otherwise SIFT does not work could maybe fix using ORB function for newer OpenCV version.
