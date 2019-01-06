# PDFMerger for PHP (PHP 5 amd 7 Compatible)

Original written by http://pdfmerger.codeplex.com/team/view<br />
Forked from https://github.com/may-den/pdf-merger which forked form https://github.com/hpolthof/pdf-merger which forked from https://github.com/clegginabox/pdf-merger which forked from https://github.com/myokyawhtun/PDFMerger

# What's different from the other forks

The orientation of each page can be keeped automaticly.

### Example Usage
```php

$pdf = new \Mayden\PDFMerger\PDFMerger;

$pdf->addPDF('samplepdfs/one.pdf', '1, 3, 4');
$pdf->addPDF('samplepdfs/two.pdf', '1-2');
$pdf->addPDF('samplepdfs/three.pdf', 'all');

//You can optionally specify a different orientation for each PDF
$pdf->addPDF('samplepdfs/one.pdf', '1, 3, 4', 'L');
$pdf->addPDF('samplepdfs/two.pdf', '1-2', 'P);

$pdf->merge('file', 'samplepdfs/TEST2.pdf', 'A');

// REPLACE 'file' WITH 'browser', 'download', 'string', or 'file' for output options
// Last parameter is for orientation (P for protrait, L for Landscape, A for auto (can be overriden by the orientation-parameter from "addPage"!)). 
// This will be used for every PDF that doesn't have an orientation specified
```
