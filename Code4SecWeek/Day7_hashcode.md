![hash.svg](https://peegonggoy.github.io/Code4SecWeek/PicCode4Sec/hash.svg)
# The hashCode() method
## Hash คืออะไร
Hash คือการแปลงข้อมูลจากแบบหนึ่ง สู่อีกแบบหนึ่งโดยใช้ algorithm บางอย่างในการแปลง ซึ่งเมื่อมีการแปลงแล้วจะไม่สามารถแปลงค่าที่ถูก Hash กลับมาเป็นข้อความต้นฉบับได้ แต่จะสามารถนำค่า Hash มา เปรียบเทียบกันได้ว่ามีค่าเหมือนกันหรือไม่ซึ่งถ้าเหมือนกันจะทำให้ทราบว่าข้อมูลที่ได้รับมานั้นคือต้นฉบับจริงหรือไม่  ดังนั้นโดยจุดประสงค์ของการใช้ Hashing คือใช้เพื่อทำการ ยืนยันว่าไม่มีการเปลี่ยนแปลงข้อความ (Integrity) ของข้อมูลนั้นๆ นั่นเอง
## hashCode() ทำงานอย่างไร
เพียงแต่ใส่ method hashCode() การ return ค่าจะเป็นตัวเลขชุดหนึ่งซึ่งสร้างโดย algorithm การ hash 
* ข้อมูลแต่ละตัวจะมีค่า hash ไม่เท่ากัน เพื่อให้ข้อมูล
แต่ละตัว มีผลการ hash เฉพาะตัว หรือเปรียบเสมือนเป็นลายนิ้วมือของข้อมูล ซึ่งค่านี้จะต้อง **_คงที่_** ไม่ว่าจะมีการเรียก method hashCode() มาใช้กี่ครั้งก็ตามภายใต้ Application เดียวกัน
* ถ้าข้อมูล 2 ชิ้นมีค่าเท่ากัน ตามวิธีการเปรียบเทียบของ method equal() เมื่อทำการ hash ข้อมูลทั้ง 2 ชิ้นต้อง **_มีค่า hash เดียวกัน_**
* ในทางกลับกันหาข้อมูลทั้ง 2 ชิ้นมีค่าไม่เท่ากันตามวิธีการเปรียบเทียบของ method equal() เมื่อทำการ hash ข้อมูลทั้ง 2 ชิ้นต้อง **_มีค่า hash ไม่เหมือนกัน_**

![equal.png](https://peegonggoy.github.io/Code4SecWeek/PicCode4Sec/equal.png)

### Reference
* [https://www.educative.io/edpresso/what-is-a-hash-code-in-java](https://www.educative.io/edpresso/what-is-a-hash-code-in-java)
* [https://www.baeldung.com/java-hashcode](https://www.baeldung.com/java-hashcode)