# Multi-PDF-Splitter

This Notebook will break a BIG PDF that is made up of many separate PDFs all bundled together into its many individual embedded PDFs.
No magic here. It just looks for the words "Page 1 of " (ie "Page 1 of 3" or "Page 1 of 6") which is typical in business documents. 
Depending on your use-case, you may need to look for different wording.

It first determines the start and end pages and writes that info to an array (List) and then goes back and reads the array,
writing the indiviual PDFs out to new files based on the start and end pages in the array.  

The original BIG PDF is left intact.

It uses the Azure Document Intelligence Service (specifically the "prebuilt-layout" model) to do the OCR.
