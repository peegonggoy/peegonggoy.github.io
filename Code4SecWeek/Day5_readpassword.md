![shoulder.png](https://peegonggoy.github.io/Code4SecWeek/PicCode4Sec/shoulder.png)

# ซ่อนข้อความหน้าคอนโซลด้วย readPassword() ใน Java
หากพูดถึงภัยคุกคามด้าน Cyber แล้ว การโจมตีแบบ Shoulder Surfing หรือ การแอบสังเกตุขณะที่เหยื่อกำลังทำการป้อนข้อมูล หรือเข้าถึงข้อมูลที่ต้องการ ถือเป็นเครื่องมือหนึ่งของผู้ไม่ประสงค์ดี ในการโจรกรรมข้อมูลที่เป็นความลับของเหยื่อ โดยไม่จำเป็นต้องใช้ความรู้ด้านคอมพิวเตอร์ใดๆ ทั้งสิ้น ก็สามารถล่วงรู้ความลับเหยื่อได้โดยง่าย สำหรับนักพัฒนาซอร์ฟแวร์ก็จำเป็นที่จะต้องนำแนวคิดด้านความปลอดภัยของการโจมตีลักษณะนี้ไปเป็นพื้นฐานของการออกแบบซอร์ฟแวร์เพื่อให้เกิดความปลอดภัยแก่ผู้ใช้
## readPassword() คืออะไร
สำหรับนักพัฒนาซอร์ฟแวร์ภาษา Java มีฟังก์ชั่นหนึ่งที่เป็นฟังก์ชั่นด้านความปลอดภัยซึ่งสามารถทำงานได้ในลักษณะเชิงป้องกันการโจมตีแบบ Shoulder Surfing คือ readPassword() ซึ่งเป็นเครื่องมือที่ใช้อ่านค่าข้อมูลจาก Console โดยไม่แสดงผลบนหน้าจอ Console หรือพูดให้เข้าใจง่ายๆ ก็คือรับค่าข้อมูลมาจากผู้ใช้แต่ขณะที่ผู้ใช้ป้อนข้อมูลจะไม่แสดงผลบนหน้าจอ Console สำหรับวันนี้ผมจะแสดงการทำงานของ readPassword() ให้ดูเผื่อท่านผู้อ่านสามารถนำไปประยุกต์ใช้กับสิ่งที่ตัวเองกำลังพัฒนาอยู่ได้ครับ

## Syntax
> public char[] readPassword() 

## ตัวอย่าง
ก่อนอื่นมาสร้างโปรแกรมอย่างง่ายด้วยภาษา Java เพื่อให้รับค่าข้อมูลจาก user ซึ่งผมจะจำลองว่าเป็นโปรแกรมในการรับค่า password เพื่อนำไปประมวลผลต่อ

![code_readpassword.png](https://peegonggoy.github.io/Code4SecWeek/PicCode4Sec/code_readpassword.png)

Output หลังจาก compile โปรแกรมแล้ว ก็จะปรากฎข้อความว่า Enter the password: เพื่อให้เราป้อนข้อมูลเข้าไป ในที่นี้ผมจะป้อนค่า "p33g0ngg0y" ใส่เข้าไปหลังข้อความ Enter the password:

![output1_readpassword.png](https://peegonggoy.github.io/Code4SecWeek/PicCode4Sec/output1_readpassword.png)

จะเห็นได้ว่าระหว่างที่เรากำลังพิมพ์คำว่า "p33g0ngg0y" จะไม่ปรากฎตัวอักษรใดๆ ปรากฎให้เห็นบน console แม่แต่ตัวเดียวจะมีเพียง cursor ที่ประพริบบอกว่าโปรแกรมกำลังทำงานอยู่เท่านั้น หลังจากป้อนค่าเสร็จเรียบร้อยแล้วลองกด Enter เพื่อให้โปรแกรมลองพริ้นท์ ข้อมูลที่ป้อนเข้าไปดูว่าจะตรงกับที่เราป้อนไปจริงๆ หรือไม่ ผลปรากฎตามภาพครับ

![output2_readpassword.png](https://peegonggoy.github.io/Code4SecWeek/PicCode4Sec/output2_readpassword.png)

## สรุป
การโจมตีแบบ Soulder Surfing เป็นการโจมตีที่ง่ายและได้ผลค่อนข้างมีประสิทธิภาพ ซึ่งผู้โจมตีไม่จำเป็นต้องมีความรู้ด้านคอมพิวเตอร์ใดๆ เลย จึงทำให้เกิดขึ้นได้ทุกที่ทุกเวลาหาก user ไม่ระมัดระวัง ดังนั้นฟังก์ชั่น readPassword() เป็นอีกฟังก์ชั่นที่จะช่วยให้นักพัฒนาซอร์ฟแวร์ภาษา Java ใช้ในการพัฒนาซอร์ฟแวร์ของตัวเองให้มีความปลอดภัยจากการโจมตีแบบ Shoulder Surfing ซึ่งจะทำให้ user มีความมั่นใจในเรื่องของความปลอดภัยเมื่อต้องป้อนข้อมูลที่เป็นความลับเข้าสู่ระบบคอมพิวเตอร์



### Reference
* [https://www.javatpoint.com/java-console-readpassword-method](https://www.javatpoint.com/java-console-readpassword-method)
* [https://www.geeksforgeeks.org/java-io-console-class-java/](https://www.geeksforgeeks.org/java-io-console-class-java/)
* [https://www.tutorialspoint.com/java/io/console_readpassword.htm](https://www.tutorialspoint.com/java/io/console_readpassword.htm)

### written by Bhoomjit Bhoominath

### All of my episodes.
[https://peegonggoy.github.io/Code4SecWeek/Day1_session_start](https://peegonggoy.github.io/Code4SecWeek/Day1_session_start)<br>
[https://peegonggoy.github.io/Code4SecWeek/Day2_session_destroy](https://peegonggoy.github.io/Code4SecWeek/Day2_session_destroy)<br>
[https://peegonggoy.github.io/Code4SecWeek/Day3_error_reporting](https://peegonggoy.github.io/Code4SecWeek/Day3_error_reporting)<br>
[https://peegonggoy.github.io/Code4SecWeek/Day4_%24Post](https://peegonggoy.github.io/Code4SecWeek/Day4_%24Post)<br>
[https://peegonggoy.github.io/Code4SecWeek/Day6_encode](https://peegonggoy.github.io/Code4SecWeek/Day6_encode)<br>
[https://peegonggoy.github.io/Code4SecWeek/Day7_hashcode](https://github.com/peegonggoy/peegonggoy.github.io/blob/main/Code4SecWeek/Day7_hashcode.md)<br>