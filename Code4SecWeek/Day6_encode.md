![urlencode.jpg](https://peegonggoy.github.io/Code4SecWeek/PicCode4Sec/urlencode.jpg)

## URL Encode a String in Java
เมื่อเรา submit HTML form โดยการใช้งาน method GET หรือ POST ซึ่งผมได้อธิบายไปใน[บทความก่อนหน้านี้แล้ว](https://peegonggoy.github.io/Code4SecWeek/Day4_%24Post) เราจะสังเกตุเห็นการส่งค่าตัวแปรระหว่าง Application ในรูปแบบของ path parameters ที่ต่อท้าย URL เมื่อเราใช้งาน method GET หรือถ้า Form นั้นมีการส่งค่าตัวแปรหลายๆ ตัว ค่าของตัวแปรเหล่านั้น ก็จะถูกนำมาสร้างให้อยู่ในรูปแบบของ Query string ให้เองโดยอัตโนมัติ ซึ่งเป็นการไม่ดีแน่ หากมีคนใช้ช่องโหว่ตรงนี้กรอกข้อมูลในลักษณะของคำสั่ง SQL ในหน้า HTML form แล้วส่งไปทำการประมวลผลในระบบฐานข้อมูล เพื่อดึงข้อมูลหรือเปลี่ยนแปลงแก้ไขข้อมูลในระบบฐานข้อมูลตามคำสั่ง SQL ที่กรอกลงไป ซึ่งคำสั่งง่ายๆที่พบเห็นบ่อย คือ “OR 1=1” ที่นิยมใช้เพื่อบายพาสการพิสูจน์ตัวตน ดังนั้นจึงจะต้องมีประบวนการในการแปลงอักขระต่างๆ ในระหว่างการ request API (Application Programming Interface) ไปเป็น String

![url.png](https://peegonggoy.github.io/Code4SecWeek/PicCode4Sec/url.png)

ดังนั้นนักพัฒนาซอร์ฟแวร์ส่วนใหญ่จำเป็นต้องทำให้ซอร์ฟแวร์ของตนมีการแสดง URL แบบ URL encoding เพื่อที่จะเข้ารหัส Query string หรือ patch parameters ในขณะที่ทำการรับส่งข้อมูลระหว่าง application URL encoding ทำให้เกิดความปลอดภัยและความน่าเชื่อถือในการรับส่งข้อมูล

## การทำงานของ URLEncoder
เมื่อทำการ Encoding string จะใช้กฎในการเปลี่ยนตัวอักษรดังนี้
* "a - z", "A - Z" และ "0 - 9" ---> ไม่เปลี่ยนแปลง
* อักขระ ".", "-", "*", และ "_" ---> ไม่เปลี่ยนแปลง
* ช่องว่าง " " ---> "+".
* อักขระและตัวอักษรอื่นๆ จะถูกเปลี่ยนไปเป็นรูปแบบการ encode ที่ใช้ ใน 1 byte จะประกอบไปด้วย 3 ตัวอักษร "%xy" เมื่อ xy คือเลขฐาน 16 2 ตัว ซึ่งโดย default ของ Java จะใช้ UTF-8

## ตัวอย่างการใช้งาน URLEncode


### Referencd
* https://www.urlencoder.io/java/
* https://docs.oracle.com/javase/7/docs/api/java/net/URLEncoder.html
