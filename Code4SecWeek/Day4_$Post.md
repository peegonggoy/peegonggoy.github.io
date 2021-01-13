![post1.png](https://peegonggoy.github.io/Code4SecWeek/PicCode4Sec/post1.png)
# ใช้ $_POST ในการรับค่าจากฟอร์ม .html
โดยปกติการรับค่าต่างๆ มาประมวลผลด้วยโปรแกรมที่เขียนด้วย PHP ซึ่งส่วนมากเป็นโปรแกรมในฝั่ง server เราจะใช้ HTML Tag ที่ชื่อว่า \<form>\</form> เป็นฟอร์มในการส่งค่าต่างๆ ไปยัง PHP ซึ่งชนิดของการรับข้อมูลในฝั่ง PHP มี 2 แบบ ได้แก่ $_POST และ $_GET ซึ่งทั้ง 2 functions มีความแตกต่างในด้านการรักษาความปลอดภัยของข้อมูลซึ่งผมจะแสดงให้ดูในบทความนี้ ในตัวอย่างแรกนี้ผมจะแสดงให้เห็นผลของการส่งค่าต่างๆ โดยใช้ Function $_GET ในการรับค่าก่อน แล้วจะแสดงให้เห็นผลของการส่งค่าโดยใช้ $_POST พร้อมทั้งชี้ให้เห็นถึงความแตกต่างของการใช้งาน function ทั้ง 2 เพื่อให้เพื่อนๆ นำไปประยุกต์ใช้งานต่อไปครับ
## Form HTML ในการส่งค่าไปให้ PHP เพื่อประมวลผล
ก่อนอื่นเรามาสร้าง Form HTML ในการส่งค่าไปให้ PHP เพื่อประมวลผลกันก่อนครับ สำหรับ Code HTML อย่างง่ายที่เขียนขึ้น จะใช้ method get ในการส่งข้อมูล โดยให้รับค่าที่เป็น text เพื่อใส่ในค่า name_txt ซึ่งเป็นค่า input ที่ผมตั้งชื่อไว้ว่า name หลังจากนั้น HTML จะส่ง action ไปยังไฟล์ show.php เพื่อประมวลผลต่อไปเรามาดูตัวอย่าง Code กันดีกว่า

![form_get.png](https://peegonggoy.github.io/Code4SecWeek/PicCode4Sec/form_get.png)

## หลังจากนั้นเราก็มาสร้างไฟล์ PHP เพื่อประมวลผลข้อความกัน
จะเห็นว่าผมใช้ $_GET เพื่อรับค่า name_txt ซึ่งเป็นค่า input จาก HTML แล้วให้ลองพิมพ์ค่าที่ได้รับมาดู

![show_get.png](https://peegonggoy.github.io/Code4SecWeek/PicCode4Sec/show_get.png) 

## พร้อมแล้วสำหรับการทดสอบการส่งค่าโดยใช้ $_GET
หน้าตาของ output ของ Form HTML ก็ประมาณนี้ครับผมลอง input "bhoomjit" เข้าไปเพื่อที่จะส่งข้อความนี้ไปให้ประมวลผลที่ PHP แล้วกดส่ง

![outform.png](https://peegonggoy.github.io/Code4SecWeek/PicCode4Sec/outform.png)

output ภายหลังประมวลผลด้วย PHP ก็จะได้ประมาณนี้ครับ 

![outshow.png](https://peegonggoy.github.io/Code4SecWeek/PicCode4Sec/outshow.png)

มีข้อน่าสังเกตุในมุมมองด้านความปลอดภัยของการรับส่งข้อมูลเมื่อเราใช้ method get ในการส่งฝั่ง HTML และใช้ $_GET ในการรับข้อมูลฝั่ง PHP เพื่อนๆ ลองสังเกตุตรงที่ผมวงสีแดงไว้น่ะครับ

![outshow_mark.png](https://peegonggoy.github.io/Code4SecWeek/PicCode4Sec/outshow_mark.png)

จะเห็นว่าตรงท้าย URL ปรากฎข้อมูลที่เราส่งและรับกันโดยที่ไม่มีการเข้าระหัสหรือซ่อนข้อความใดๆ ทั้งสิ้นและนี่คือข้อสังเกตุด้านความปลอดภัยเมื่อเราใช้ $_GET ในการรับข้อมูล

## ลองมาดู $_POST กันบ้าง
Form HTML ครับเปลี่ยนมาใช้ post method

![form_post.png](https://peegonggoy.github.io/Code4SecWeek/PicCode4Sec/form_post.png)

PHP ที่จะใช้สั่งให้พิมพ์ค่าที่ได้รับมาโดยใช้ $_POST ครับ

![show_post.png](https://peegonggoy.github.io/Code4SecWeek/PicCode4Sec/show_post.png)

ผลลัพธ์ของการใช้ $_POST ครับ

![out_show_post.png](https://peegonggoy.github.io/Code4SecWeek/PicCode4Sec/out_show_post.png)

สังเกตุที่ URL ครับ จะไม่มีการแสดงค่าตัวแปรต่างๆ ต่อจาก URL เดิมเลย ซึ่งแตกต่างกับแบบ $_GET นะครับ ทำให้วิธีนี้ช่วยเรื่องความปลอดภัยของข้อมูลที่รับ-ส่ง ป้องกัน Data leakage ได้ในระดับหนึ่งครับ

## สรุป
$_POST เป็น function ในการรับส่งข้อมูลซึ่งมีความปลอดภัยซึ่งสามารถป้องกัน Data leakage ได้ในระดับหนึ่งอย่างน้อยก็มีประสิทธิภาพในการใช้มากว่า $_GET แต่อย่างไรก็ตามการใช้ $_POST อย่างเดียวก็ไม่สามรถป้องกันได้ 100% เพราะก็ยังมีวิธีและโปรแกรมเฉพาะในการดักจับข้อมูลต่างๆ ที่รับส่งกันได้ ดังนั้นจึงต้องมีวิธีการอื่นๆ เข้ามาประกอบเพื่อสร้างความปลอดภัยมากขึ้น

## Reference
* [https://www.w3schools.com/php/](https://www.w3schools.com/php/)
* [https://www.php.net/manual/en/reserved.variables.post.php](https://www.php.net/manual/en/reserved.variables.post.php)
* [https://www.tutorialspoint.com/php/php_get_post.htm](https://www.tutorialspoint.com/php/php_get_post.htm)

### written by Bhoomjit Bhoominath
