![post1.png](https://peegonggoy.github.io/Code4SecWeek/PicCode4Sec/post1.png)
# ใช้ $_POST ในการรับค่าจากฟอร์ม .html
โดยปกติการรับค่าต่างๆ มาประมวลผลด้วยโปรแกรมที่เขียนด้วย PHP ซึ่งส่วนมากเป็นโปรแกรมในฝั่ง server ซึ่งอาจจะนำไปเก็บไว้ในฐานข้อมูล เราจะใช้ HTML Tah ที่ชื่อว่า \<form>\</form> เป็นฟอร์มในการรับค่าต่างๆ ซึ่งชนิดของการส่งข้อมูลมี 2 แบบ ได้แก่ $_POST และ $_GET ซึ่งทั้ง 2 functions มีความแตกต่างในการรับค่าทางด้านความปลอดภัยของข้อมูลซึ่งผมจะแสดงให้ดูในบทความนี้ครับ ในตัวอย่างแรกนี้ผมจะแสดงให้เห็นผลของการส่งค่าต่างๆ โดยใช้ Function $_GET ในการรับค่าก่อน
## ก่อนอื่นมาสร้าง Form HTML ในการส่งค่าไปให้ PHP เพื่อประมวลผล
ก่อนอื่นเรามาสร้าง Form HTML ในการส่งค่าไปให้ PHP เพื่อประมวลผลกันก่อนครับ สำหรับ Code HTML อย่างง่ายที่เขียนขึ้น จะใช้ method get ในการรับส่งข้อมูล โดยให้รับค่าที่เป็น text เพื่อใส่ในค่า name_txt ซึ่งเป็นค่า input ที่ผมตั้งชื่อไว้ว่า name หลังจากนั้น HTML จะส่ง action ไปยังไฟล์ show.php เพื่อประมวลผลต่อไปเรามาดูตัวอย่าง Code กันดีกว่า

![form_get.png](https://peegonggoy.github.io/Code4SecWeek/PicCode4Sec/form_get.png)

### หน้าตาของ output ของ Form HTML ก็ประมาณนี้ครับ
ผมลอง input "bhoomjit" เข้าไปเพื่อที่จะส่งข้อความนี้ไปให้ประมวลผลที่ PHP

![outform.png](https://peegonggoy.github.io/Code4SecWeek/PicCode4Sec/outform.png)
