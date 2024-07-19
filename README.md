### QR-Generator
This App will Generate QR codes based on a user inputted string

## Pyinstaller Instructions
please vist the link for full explanation: 

command to run py installer:
first input this to terminal 

"C:\Python312\Lib\site-packages;customtkinter/"
--onedir
pyinstaller --onedir --windowed --add-data "images/empty.ico;." --add-data "images/Blank_AF.jpg;." --add-data "images/icon.ico;." --add-data "C:\Python312\Lib\site-packages;customtkinter/"  --hidden-import=PIL._imagingtk --icon=images/icon.ico app.py
