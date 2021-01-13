![urlencode.jpg](https://peegonggoy.github.io/Code4SecWeek/PicCode4Sec/urlencode.jpg)

## URL Encode a String in Java
เมื่อเรา submit HTML form โดยการใช้งาน method GET หรือ POST ซึ่งผมได้อธิบายไปใน[บทความก่อนหน้านี้แล้ว](https://peegonggoy.github.io/Code4SecWeek/Day4_%24Post) เราจะสังเกตุเห็นการส่งค่าตัวแปรระหว่าง Application ในรูปแบบของ path parameters ที่ต่อท้าย URL เมื่อเราใช้งาน method GET หรือถ้า Form นั้นมีการส่งค่าตัวแปรหลายๆ ตัว ค่าของตัวแปรเหล่านั้น ก็จะถูกนำมาสร้างให้อยู่ในรูปแบบของ Query string ให้เองโดยอัตโนมัติ ซึ่งเป็นการไม่ดีแน่ หากมีคนใช้ช่องโหว่ตรงนี้กรอกข้อมูลในลักษณะของคำสั่ง SQL ในหน้า URL แล้วส่งไปทำการประมวลผลในระบบฐานข้อมูล เพื่อดึงข้อมูลหรือเปลี่ยนแปลงแก้ไขข้อมูลในระบบฐานข้อมูลตามคำสั่ง SQL ที่กรอกลงไป ซึ่งคำสั่งง่ายๆที่พบเห็นบ่อย คือ “OR 1=1” ที่นิยมใช้เพื่อบายพาสการพิสูจน์ตัวตน ดังนั้นจึงจะต้องมีประบวนการในการแปลงอักขระต่างๆ ในระหว่างการ request API (Application Programming Interface) ไปเป็น String

![url.png](https://peegonggoy.github.io/Code4SecWeek/PicCode4Sec/url.png)

ดังนั้นนักพัฒนาซอร์ฟแวร์ส่วนใหญ่จำเป็นต้องทำให้ซอร์ฟแวร์ของตนมีการแสดง URL แบบ URL encoding เพื่อที่จะเข้ารหัส Query string หรือ patch parameters ในขณะที่ทำการรับส่งข้อมูลระหว่าง application URL encoding ทำให้เกิดความปลอดภัยและความน่าเชื่อถือในการรับส่งข้อมูล

## การทำงานของ URL Encoder
เมื่อทำการ Encoding string จะใช้กฎในการเปลี่ยนตัวอักษรดังนี้
* "a - z", "A - Z" และ "0 - 9" ---> ไม่เปลี่ยนแปลง
* อักขระ ".", "-", "*", และ "_" ---> ไม่เปลี่ยนแปลง
* ช่องว่าง " " ---> "+".
* อักขระและตัวอักษรอื่นๆ จะถูกเปลี่ยนไปเป็นรูปแบบการ encode ที่ใช้ ใน 1 byte จะประกอบไปด้วย 3 ตัวอักษร "%xy" เมื่อ xy คือเลขฐาน 16 2 ตัว ซึ่งโดย default ของ Java จะใช้ UTF-8

## ตัวอย่างการใช้งาน URL Encode
ในภาษา Java มี URL encoder class ใช้สำหรับการ encode query string หรือ path parameters ให้อยู่ในรูปแบบ URL encode ตัวอย่างด้านล่างนี้จะแสดงการใช้งาน method encode() เพื่อที่จะทำ URL encode ในภาษา Java

![urlencode1.png](https://peegonggoy.github.io/Code4SecWeek/PicCode4Sec/urlencode1.png)

จะเห็นได้ว่ารูปแบบการ encode ที่ใช้เป็น UTF-8 ซึ่งเป็น parameter ตัวที่ 2 ที่ต้องใส่ข้อมูลของฟังก์ชั่น URLEncoder.encode() โดยในที่นี้ผมจะดำเนินการ encode หลังเครื่องหมาย "=" ของ URL : https://www.peegonggoy.io/?name= **_URLEncoded_** ซึ่ง Output จะเป็นไปตามรูปด้านล่าง

![urlencode2.png](https://peegonggoy.github.io/Code4SecWeek/PicCode4Sec/urlencode2.png)

## สรุป
encode() เป็น method ในภาษา Java ที่จะใช้ในการ encode query string และ path parameters เมื่อมีการ request API ซึ่งหลักการทำงานจะดำเนินการเปลี่ยนอักขระต่างๆ ของข้อมูลที่ต้องการส่งไปยัง application อื่นไปเป็น string ซึ่งรูปแบบการ encode พื้นฐานของภาษา Java จะใช้ UTF-8 


### Referencd
* [https://www.urlencoder.io/java/](https://www.urlencoder.io/java/)
* [https://docs.oracle.com/javase/7/docs/api/java/net/URLEncoder.html](https://docs.oracle.com/javase/7/docs/api/java/net/URLEncoder.html)
