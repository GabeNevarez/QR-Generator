# QR-Generator
## Summary
This App will Generate QR codes based on a user inputted strings and allow the user to save the qr code as .jpg.

## Dependancies
### Operating System:
* Windows
* Linux
* macOS

### Python Version:
* Python 3.x (preferably the latest version for compatibility with dependencies).

### Libraries
* tkinter: Included in the standard Python library.
* customtkinter: Needs to be installed separately using pip install customtkinter.
* Pillow (PIL): For image processing, install using pip install pillow.
* qrcode: For generating QR codes, install using pip install qrcode[pil]

```sh
pip install customtkinter pillow qrcode
```

## Directory Structure
### Build Structure
```
qrcode-generator/
│
├── app.py
├── images/
│   └── Blank_AF.jpg
│   └── empty.ico
├── README.md
```


## Pyinstaller Instructions

### 1. Install PyInstaller
   * ***Initiate Installation***
     ```bash
     pip install pyinstaller
     ```
   * ***Confirm installation by checking the version***
     ```sh
     pyinstaller --version
     ```
### 2. Navigate to Directory where ***QR-Gnerator*** is stored in the command line
### 3. Find the file path for `customtkinter` to input into the command. This is necessary for the use of `customtkinter` in any packaged application. For more information, please see the [CustomTkinter Packaging Guide](https://github.com/TomSchimansky/CustomTkinter/wiki/Packaging).
  * **One Method for finding the file path for 'customtkinter' is to an ide run the foloowing command coping the input
    ```Python
    import customtkinter
    print(customtkinter.__file__)
    ```
    
4. "<CustomTkinter Location>/customtkinter;customtkinter/


please vist the link for full explanation: 

command to run py installer:
first input this to terminal 

"C:\Python312\Lib\site-packages;customtkinter/"
--onedir
pyinstaller --onedir --windowed --add-data "images/empty.ico;." --add-data "images/Blank_AF.jpg;." --add-data "images/icon.ico;." --add-data "C:\Python312\Lib\site-packages;customtkinter/"  --hidden-import=PIL._imagingtk --icon=images/icon.ico app.py
