<img src="https://github.com/KravitzMC/IntroductionToPDF-/blob/main/file_type_pdf_icon_130274.png"/>

#  Introduction to Render PDF 

พื้นฐานการ Render PDF ความจริงแล้วง่ายแค่ปลายนิ้ว  !!!
หลังจากที่ผมได้ศึกษาวิธีการ Render PDF บนเอกสาร [Adobe Reference 1.7](https://ghostscript.com/~robin/pdf_reference17.pdf)  พบว่ายุ่งยากพอสมควรเนื่องจากใช้เวลาศึกษาเยอะบวกกับทำความเข้าใจใน Strucutre ของมันยากว่าทำอย่างไรถึงจะ Render ไฟล์เป็น PDF แบบง่าย ๆ ได้เพื่อจะนำไปเขียนเป็นโปรแกรม เนื่องจาก ใน Paper ไม่ได้บอกรายละเอียดเอาไว้ (หรือผมหาไม่เจอเองฟระ!?) ผมจึงค้นหาจนได้ไปข้อมูลจาก Web Archive (Wayback Machine) แห่งหนึ่ง ที่เคยถูกลบออกไปนานแล้ว  (ไม่ทราบว่าของดีๆแบบนี้ลบออกไปทำไม??) จนมาเจอวิธีการง่าย ๆ เพียงปลายนิ้วแค่เราทำการสร้าง  PDF Structure แบบ Text ธรรมดาขึ้นมา!!! แล้วเอา โค้ดดังตัวอย่าง ด้านล่างนี้ ไปใส่ใน Notepad หรือ Text Editor อะไรก็ได้  

#### ตัวอย่าง PDF Structure  (โดยให้เราทำการ  Save File)  เป็น  sample.pdf   (All File)

```
%PDF-1.7

1 0 obj  % entry point
<<
  /Type /Catalog
  /Pages 2 0 R

>endobj

2 0 obj
<<
  /Type /Pages
  /MediaBox [ 0 0 200 200 ]
  /Count 1
  /Kids [ 3 0 R ]

>endobj

3 0 obj
<<
  /Type /Page
  /Parent 2 0 R
  /Resources <<
    /Font <<
      /F1 4 0 R 
    >>

  >/Contents 5 0 R
  >
  >endobj

4 0 obj
<<
  /Type /Font
  /Subtype /Type1
  /BaseFont /Times-Roman

>endobj

5 0 obj  % page content
<<
  /Length 44
  
>stream
>BT
>70 50 TD
>/F1 12 Tf
>(Hello, world!) Tj
>ET
>endstream
>endobj

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

>startxref
>492
>%%EOF

```

#### ผลลัพธ์จะออกมาเป็นดังรูป

![image-20210831225121354](https://github.com/KravitzMC/IntroductionToPDF-/blob/main/sample.png)

#### เราสามารถนำวิธีการแนวทางนี้ไปเขียนโปรแกรมด้วยภาษาต่าง ๆ ตามที่เราต้องการสุดจะแล้วแต่ ไม่ว่าจะ Render, Split, Merge แต่ควรทำความเข้าใจ PDF Structure ให้เป็นอย่างดีเสียก่อน
