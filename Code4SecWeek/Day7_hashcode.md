![hash.svg](https://peegonggoy.github.io/Code4SecWeek/PicCode4Sec/hash.svg)
# The hashCode() method
## Hash คืออะไร
Hash คือการแปลงข้อมูลจากแบบหนึ่ง สู่อีกแบบหนึ่งโดยใช้ algorithm บางอย่างในการแปลง ซึ่งเมื่อมีการแปลงแล้วจะไม่สามารถแปลงค่าที่ถูก Hash กลับมาเป็นข้อความต้นฉบับได้ แต่จะสามารถนำค่า Hash มา เปรียบเทียบกันได้ว่ามีค่าเหมือนกันหรือไม่ซึ่งถ้าเหมือนกันจะทำให้ทราบว่าข้อมูลที่ได้รับมานั้นคือต้นฉบับจริงหรือไม่  ดังนั้นโดยจุดประสงค์ของการใช้ Hashing คือใช้เพื่อทำการ ยืนยันว่าไม่มีการเปลี่ยนแปลงข้อความ (Integrity) ของข้อมูลนั้นๆ นั่นเอง
## hashCode() ทำงานอย่างไร
ในภาษา Java เพียงแต่ใส่ method hashCode(object) โดย method จะ return ค่าจะเป็นตัวเลขชุดหนึ่งซึ่งสร้างโดย algorithm การ hash ซึ่ง
* ข้อมูลแต่ละตัวจะมีค่า hash ไม่เท่ากัน เพื่อให้ข้อมูล
แต่ละตัว มีผลการ hash เฉพาะตัว หรือเปรียบเสมือนเป็นลายนิ้วมือของข้อมูล ซึ่งค่านี้จะต้อง **_คงที่_** ไม่ว่าจะมีการเรียก method hashCode() มาใช้กี่ครั้งก็ตามภายใต้ Application เดียวกัน
* ถ้าข้อมูล 2 ชิ้นมีค่าเท่ากัน ตามวิธีการเปรียบเทียบของ method equal() เมื่อทำการ hash ข้อมูลทั้ง 2 ชิ้นต้อง **_มีค่า hash เดียวกัน_**
* ในทางกลับกันหาข้อมูลทั้ง 2 ชิ้นมีค่าไม่เท่ากันตามวิธีการเปรียบเทียบของ method equal() เมื่อทำการ hash ข้อมูลทั้ง 2 ชิ้นต้อง **_มีค่า hash ไม่เหมือนกัน_**

![equal.png](https://peegonggoy.github.io/Code4SecWeek/PicCode4Sec/equal.png)

## ตัวอย่างการทำงาน
ผมจะกำหนดให้ตัวแปร a และ b มีค่าเท่ากันคือ bhoomjit และ c กับ d มีค่าที่แตกต่างกันคือ bhoomjit และ bhoomjit. ตามลำดับ ซึ่งผมจะนำแต่ละคู่มาเปรียบเทียบโดยใช้ method equal() ในการเปรียบเทียบ

![ex_hash.png](https://peegonggoy.github.io/Code4SecWeek/PicCode4Sec/ex_hash.png)

### Output
ดูค่า hash ที่ได้จะเห็นว่า ตัวแปร a และ b ซึ่งมีค่าเท่ากันค่า hash จะเท่ากัน และตัวแปร c และ d มีค่าไม่เท่ากันจึงทำให้ค่า hash ไม่เท่ากัน

![out_ex_hash.png](https://peegonggoy.github.io/Code4SecWeek/PicCode4Sec/out_ex_hash.png)

## สรุป
Method hashCode() จะใช้ในการแปลงค่าข้อมูลไปเป็นข้อมูลตัวเลขชุดหนึ่งโดยใช้ hash algorithm ซึ่งโดยหลักการสำคัญของการทำงานมีอยู่ 3 ข้อด้วยกันคือใน Application เดียวกันไม่ว่าจะเรียกใช้กี่ครั้งค่า hash ต้องเท่ากัน, ข้อมูลเหมือนกันค่า hash ต้องเท่ากัน และสุดท้ายในทางกลับกันหากข้อมูลไม่เหมือนกันก็ต้องได้ค่า hash ไม่เหมือนกัน ซึ่งด้วยคุณสมบัติของหลักการสำคัญดังกล่าวการทำ hash จึงใช้สำหรับการตรวจสอบความถูกต้องของข้อมูลนั่นเอง

### Reference
* [https://www.educative.io/edpresso/what-is-a-hash-code-in-java](https://www.educative.io/edpresso/what-is-a-hash-code-in-java)
* [https://www.baeldung.com/java-hashcode](https://www.baeldung.com/java-hashcode)

### written by Bhoomjit Bhoominath

### All of my episode
[https://peegonggoy.github.io/Code4SecWeek/Day1_session_start](https://peegonggoy.github.io/Code4SecWeek/Day1_session_start)
[https://peegonggoy.github.io/Code4SecWeek/Day2_session_destroy](https://peegonggoy.github.io/Code4SecWeek/Day2_session_destroy)
[https://peegonggoy.github.io/Code4SecWeek/Day3_error_reporting](https://peegonggoy.github.io/Code4SecWeek/Day3_error_reporting)
[https://peegonggoy.github.io/Code4SecWeek/Day4_%24Post](https://peegonggoy.github.io/Code4SecWeek/Day4_%24Post)
[https://peegonggoy.github.io/Code4SecWeek/Day5_readpassword](https://peegonggoy.github.io/Code4SecWeek/Day5_readpassword)
[https://peegonggoy.github.io/Code4SecWeek/Day6_encode](https://peegonggoy.github.io/Code4SecWeek/Day6_encode)
