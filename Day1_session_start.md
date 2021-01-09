# Code4SecDay1
## การใช้งาน session ในภาษา PHP ภาค1 การเริ่มต้น session ด้วย session_start()
### session คืออะไร
เซสชั่น (Session) คือตัวแปรในภาษา PHP ที่มีความพิเศษกว่าตัวแปรปกติคือ ตัวแปรเซสชั่นและค่าตัวแปรจะยังคงอยู่ไม่ว่าเราจะเปลี่ยนหน้าจากหน้าหนึ่งไป สู่อีกหน้าหนึ่งโดยยังมีค่าคงอยู่เสมอจนกระทั่งตัวแปรหมดอายุหรือถูกทำการลบค่า ทิ้งซึ่งเป็นข้อดีขอตัวแปรนี้ ด้วยความพิเศษตัวแปรเซสชั่นจึงนิยมนำมาใช้ในการรับส่งค่าข้อมูลที่เก็บเป็นความลับที่จะต้อง ใช้ในการระบุตัวตนเพื่อใช้สิทธิของระบบเช่น การยืนยันตัวตนด้วย Username และ Password เพื่อให้ได้ค่าตัวแปรนี้มาระบุตัวตนซึ่งทำให้เราไม่จำเป็นต้อง login ในทุกหน้าของการเปลี่ยนแปลงหน้า  ตัวแปรเซสชั่นจึงมีความปลอดภัยในการเก็บรักษาข้อมูลได้อย่างมาก
### การเริ่มต้นใช้งาน session ด้วย session_start()

#### ก่อนการใช้งาน session ต้องใช้คำสั่งเพื่อเปิดใช้งาน session ขึ้นมาก่อน ซึ่งผมกำหนดให้ page1 เป็นการกำหนดค่าของตัวแปรที่เก็บใน session โดยให้ ตัวแปร name1 เก็บค่า Bhoomjit และตัวแปร name2 เก็บค่า Bad Boy และเมือกด next page จะส่ง Action ไปที่ page 2
[![page1.png](https://i.postimg.cc/CLrfDdpS/page1.png)](https://postimg.cc/SJ8sbSKv)

#### page2 เป็นการแสดงผลตัวแปรของ session โดยที่ไม่ต้องไปกำหนดค่าใหม่โดยจะให้ print ค่าของตัวแปร name1 และ name2
[![page2.png](https://i.postimg.cc/vmrBPZk1/page2.png)](https://postimg.cc/v1mbTbQM)

#### มาดู output หน้า page ทั้ง 2 ที่สร้างขึ้นมาบ้างครับ
Page1<br>
[![out1.png](https://i.postimg.cc/YSH2mw0t/out1.png)](https://postimg.cc/JspC9vjF)

Page2<br>
[![out2.png](https://i.postimg.cc/0Q58cd73/out2.png)](https://postimg.cc/PLcsqD3z)

#### สรุป
เราจะเห็นว่า session มีประโยชน์ในการจดจำค่าของตัวแปรซึ่งจะจดจำไปจนกว่า session นั้นถูกทำลายหรือถูกลบไปโดยเราสามารถนำไปประยุกต์ใช้ในเรื่องของการ login แล้วกำหนดสิทธิ์ของผู้ใช้ที่จะให้ทำอะไรหรือไม่ให้ทำอะไรในแต่ละ Page ได้ สำหรับการทำลาย session ลบค่าของตัวแปรทั้งหมดที่อยู่ใน session เมื่อ logout เพื่อไม่ให้คนอื่นสามารถกด back เพื่อกลับไปใช้ user ของเราในการ login ได้ ติดตามต่อกันในภาค 2 น่ะครับ
#### Reference
* https://www.php.net/manual/en/function.session-start.php
* http://www.phpdevthailand.com/2016/05/31/php_session
* https://www.mindphp.com/forums/viewtopic.php?f=72&t=48715

#### written by Bhoomjit Bhoominath