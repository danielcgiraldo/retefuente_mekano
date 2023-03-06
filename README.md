# Retefuente Certificate Splitter

Read a PDF containing all retefuente certificates of the year exported by the Mekano ERP accountability software. Separate the pages of the file and name each page with the NIT of the company for which the certificate was issued. Additionally, the script generates a list of all company NITs.

Since the PDF pages do not have readable text, we are using OCR (optical character recognition) to extract the text.

## Requirements

- Make sure to have installed: PIL, pytesseract, PyPDF2 and [pdf2image](https://pdf2image.readthedocs.io/en/latest/installation.html) (including poppler).
- Use Linux or MacOS (Windows is not supported using this code).
- Make sure to have installed tesseract.

## Steps

- Open a shell in this folder.
- Run `python -m unittest test_build` to make sure everything is working as expected.
- Place PDF file generated by Mekano ERP software in this folder named as certificados.pdf
- Run the `run.py` script. This script will automatically rotate, extract the pages of the PDF file and name each page with the NIT of the company for which the certificate was issued.
- Once the script has finished running, go to the `./certificados` folder to find the extracted pages and `list.csv` with all the NIT numbers (unknown not included). Check all the pages to ensure that they have been named correctly. Be sure to pay special attention to any pages that are named "unknown", as this may indicate that the script was not able to identify the NIT for those pages.

> Recommendation: Install modules using `python -m pip install <module>`. For more information: <https://realpython.com/lessons/why-cant-python-find-my-modules/>

[!["Buy Me A Coffee"](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://www.buymeacoffee.com/danielcgiraldo)
