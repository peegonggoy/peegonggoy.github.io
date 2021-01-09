# การใช้งาน session ในภาษา PHP ภาค 2 การทำลาย session ด้วย session_destroy()
หลักจากที่เราสร้าง session มาแล้วตามที่เคยเขียนไปแล้วใน [ภาค1](https://peegonggoy.github.io/Code4SecWeek/Day1_session_start) ถึงบทความนี้จะทำการทำลาย session เพื่อไม่ให้หลงหลือ session นั้นอยู่หรือเป็นการล้างค่าตัวแปรทั้งหมดที่ถูกเก็บไว้ใน session ซึ่งเราอาจจะประยุกต์เอาไปใช้ในการป้องกันใครมาสวมรอยในการ login เข้าใช้งานโดยข้อมูลของเราได้

### มาดูตัวอย่างของการ Coding และการทำงาน ของฟังก์ชั่น session_destroy() อย่างง่ายกันน่ะครับ
สร้าง session ขึ้นมาเพื่อเก็บตัวแปรใน session ในครั้งนี้เราจะเก็บค่าตัวแปรแค่ 1 ตัว คือ name1 ซึ่งจะเก็บค่า Bhoomjit ไว้ เมื่อกด next page จะ action ไปที่ page2

![dpage1.png](https://peegonggoy.github.io/Code4SecWeek/PicCode4Sec/dpage1.png)

#### output ของ page1 ก็จะได้ประมาณนี้ครับ

![out1.png](https://peegonggoy.github.io/Code4SecWeek/PicCode4Sec/out1.png)

### page2 เป็นการทดสอบว่าค่าของตัวแปรที่เก็บไว้ใน session ยังมีค่าคงเดิมตามที่เราตั้งค่าไว้ใน page ก่อนหน้า โดยให้ print ค่าของตัวแปร name1 ออกมาดู เมื่อกด logout ก็จะ action ไปที่ page3 ทันที และเพิ่ม function เพื่อใช้ในการตรวจสอบค่าตัวแปร name1 เพื่อใช้ตรวจสอบเมื่อเราทำลาย session ไปแล้วและกลับมาที่หน้า page2 จะต้องปรากฎคำว่า "Please Login!" เพื่อยืนยันว่าค่าของตัวแปรต่างๆ ที่เราเก็บไว้ใน session นั้นหายไปจริงๆ

![dpage1.png](https://peegonggoy.github.io/Code4SecWeek/PicCode4Sec/dpage2.png)

### output ของ page2 ก็จะได้ประมาณนี้ครับ

![out2.png](https://peegonggoy.github.io/Code4SecWeek/PicCode4Sec/dout2.png)

### เมื่อกด logout ใน page ก่อนหน้าก็จะ action ไปที่ page3 ซึ่งจะมี function session_destroy() อยู่ และลองให้ print ค่าของตัวแปรหลังจากทำลาย session ไปแล้ว

![dpage3.png](https://peegonggoy.github.io/Code4SecWeek/PicCode4Sec/dpage3.png)

### output ของ page3 ปรากฎว่าโปรแกรมยังคงจำค่าตัวแปรของ session ที่ถูกทำลายอยู่ดังที่ปรากฎในรูป

![dout3.1.png](https://peegonggoy.github.io/Code4SecWeek/PicCode4Sec/dout3.1.png)
### แต่เมื่อเรากด Back กลับไปยัง page2 ปรากฎว่า session ที่เราสร้างขึ้นมาถูกทำลายไปแล้วพร้อมกับค่าของตัวแปรด้วย จึงปรากฎคำว่า "Please Login"

![dout3.png](https://peegonggoy.github.io/Code4SecWeek/PicCode4Sec/dout3.png)

### สรุป
function ใช้ในการทำลาย session ที่สร้างขึ้นโดยจะดำเนินการลบค่าต่างๆที่อยู่ใน session ทั้งหมดแต่ทั้งนี้ถึงแม้ว่าเราจะดำเนินการทำลาย session ไปแล้วแต่โปรแกรมก็ยังจำค่าของตัวแปรที่เรากำหนดไว้อยู่ดังนั้นหากเราต้องการจะลบค่าตัวแปรออกไปทันทีที่เราทำลาย session ก็ควรใช้ function session_destroy() คู่กับ session_unset()

![unset.png](https://peegonggoy.github.io/Code4SecWeek/PicCode4Sec/unset.png)

ซึ่งใน page2 เมื่อเรากด logout จะได้ผลลัพธ์ดังนี้

![dout4.png](https://peegonggoy.github.io/Code4SecWeek/PicCode4Sec/dout4.png)

### Reference
* https://www.php.net/manual/en/function.session-destroy.php
* https://www.mindphp.com/forums/viewtopic.php?f=72&t=48715
* https://www.unzeen.com/article/171/


