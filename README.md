# PDFMerger for PHP (PHP 5 amd 7 Compatible)

Original written by http://pdfmerger.codeplex.com/team/view<br />
Forked from https://github.com/hpolthof/pdf-merger which forked from https://github.com/clegginabox/pdf-merger which forked from https://github.com/myokyawhtun/PDFMerger

# What's different from the other forks

This has up an up to date version of `setasign/fpdi-fpdf` as older versions have code not compatible with PHP 7. Thank you to all the previous forks for allowing an easy upgrade.  

### Example Usage
```php

$pdf = new \Mayden\PDFMerger\PDFMerger;

$pdf->addPDF('samplepdfs/one.pdf', '1, 3, 4');
$pdf->addPDF('samplepdfs/two.pdf', '1-2');
$pdf->addPDF('samplepdfs/three.pdf', 'all');

//You can optionally specify a different orientation for each PDF
$pdf->addPDF('samplepdfs/one.pdf', '1, 3, 4', 'L');
$pdf->addPDF('samplepdfs/two.pdf', '1-2', 'P);

$pdf->merge('file', 'samplepdfs/TEST2.pdf', 'P');

// REPLACE 'file' WITH 'browser', 'download', 'string', or 'file' for output options
// Last parameter is for orientation (P for protrait, L for Landscape). 
// This will be used for every PDF that doesn't have an orientation specified
```
