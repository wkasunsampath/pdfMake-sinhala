# pdfMake-sinhala
Sinhala Unicode support for pdfMake - PDF Library
## Usage

> Note: You **don't** need to include `vfs_fonts.js` file from pdfmake library.

```html
<script src="pdfmake.min.js"></script>
<script src="your_dir/pdfmake_sinhala.js"></script>
<script>
  var docDefinition = {
      defaultStyle: {
          font: 'mySinhalaFont'
      },
      pageSize: 'A4',
      pageMargins: [ 60, 65, 60, 70 ],
      content:[ your content here],
      styles: {
          header: {
              bold: true,
          },
          headerfill: {
              bold: true,
              italics: true,
              color: '#FFFFFF',
              fillColor: '#2361AE',
          },
      }
  };
  pdfMake.fonts = {
          mySinhalaFont: {
                  normal: 'iskpota.ttf',
                  bold: 'iskpota.ttf',
                  italics: 'iskpota.ttf',
                  bolditalics: 'iskpota.ttf'
          }
  };
  pdfMake.createPdf(docDefinition).download('myPDF');
</script>
