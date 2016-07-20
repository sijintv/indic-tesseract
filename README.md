# Indic Tesseract
Repository containing tessdata, source training data and other materials and hacks for teaching Tesseract OCR Engine Indic Languages, initially Malayalam.

## Tesseract
[Tesseract](https://github.com/tesseract-ocr/tesseract) was originally developed at Hewlett-Packard Laboratories Bristol and at Hewlett-Packard Co, Greeley Colorado between 1985 and 1994, with some more changes made in 1996 to port to Windows, and some C++izing in 1998.

In 2005 Tesseract was open sourced by HP. Since 2006 it is developed by Google.

## Installation
You may need to grab some dependecies.

For Ubuntu 16.04,
```bash
sudo apt-get install libleptonica-dev libicu-dev libcairo-dev libpango1.0-dev
```
Now download the latest stable release of Tesseract source from [here](https://github.com/tesseract-ocr/tesseract/archive/3.04.01.zip).

Extract the zip and **cd** into that folder. Now run,
```
./autogen.sh
./configure
make
sudo make install
make training
sudo make training-install
```
Take control over your tessdata directry.
```
sudo chown `whoami` -R /usr/local/share/tessdata
```
## Running
@TODO
## Training
@TODO
## Testing
@TODO
## Contribution
@TODO
## License
Licensed under the [Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0).
