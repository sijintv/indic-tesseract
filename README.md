# Indic Tesseract
Repository containing tessdata, source training data and other materials and hacks for improving accuracy of Indic Languages recognition (initially Malayalam) in Tesseract OCR Engine.

## Tesseract
[Tesseract](https://github.com/tesseract-ocr/tesseract) was originally developed at Hewlett-Packard Laboratories Bristol and at Hewlett-Packard Co, Greeley Colorado between 1985 and 1994, with some more changes made in 1996 to port to Windows, and some C++izing in 1998.

In 2005 Tesseract was open sourced by HP. Since 2006 it is developed by Google.

## Installation
You may need to grab some dependecies.

For Ubuntu or Debian,
```bash
sudo apt-get install libleptonica-dev libicu-dev libcairo-dev libpango1.0-dev automake libtool libtiff5-dev autoconf pkg-config libpng-dev libjpeg-dev zlib1g-dev
```
Now download the latest stable release of Tesseract source from [here](https://github.com/tesseract-ocr/tesseract/archive/3.05.00.zip).

Extract the zip and **cd** into that folder. Now run,
```
./autogen.sh
./configure
make
sudo make install
make training
sudo make training-install
sudo ldconfig
```
Take control over your tessdata directry.
```
sudo chown `whoami` -R /usr/local/share/tessdata
```
## Running
Tesseract needs language data for character regognition.

Clone this repository.
```
git clone https://github.com/tvsijin/indic-tesseract.git

```
Copy the contents of tessdata to your local tessdata folder.
```
cd indic-tesseract
cp tessdata/* /usr/local/share/tessdata/
```
Now you can run tesseract by,
```
 tesseract imagename outputbase [-l lang] [-psm pagesegmode] [configfile...]
```
So basic usage to do OCR on an image called 'myscan.tiff' which contains Malayalam characters, and save the result to 'out.txt' would be,
```
tesseract myscan.tiff out -l mal
```
## Training
@TODO
## Testing
@TODO
## Contribution
@TODO
## License
Licensed under the [Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0).
