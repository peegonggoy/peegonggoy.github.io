# Code4SecDay2
## การใช้งาน session ในภาษา PHP ภาค 2 การทำลาย session ด้วย session_destroy()
หลักจากที่เราสร้าง session มาแล้วตามที่เคยเขียนไปแล้วใน [ภาค1](https://peegonggoy.github.io/Code4SecWeek/Day1_session_start) ถึงบทความนี้จะทำการทำลาย session เพื่อไม่ให้หลงหลือ session นั้นอยู่หรือเป็นการล้างค่าตัวแปรทั้งหมดที่เก็บไว้ใน session ซึ่งเราอาจจะประยุกต์เอาไปใช้ในการป้องกันใครมาสวมรอยในการ login เข้าใช้งานโดยข้อมูลของเราได้
