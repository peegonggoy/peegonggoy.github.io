![shoulder.png](https://peegonggoy.github.io/Code4SecWeek/PicCode4Sec/shoulder.png)

# ซ่อนข้อความหน้าคอนโซลด้วย readPassword() ใน Java
หากพูดถึงภัยคุกคามด้าน Cyber แล้ว การโจมตีแบบ Shoulder Surfing หรือ การแอบสังเกตุขณะที่เหยื่อกำลังทำการป้อนข้อมูล หรือเข้าถึงข้อมูลที่ต้องการ ถือเป็นเครื่องมือหนึ่งของผู้ไม่ประสงค์ดี ในการโจรกรรมข้อมูลที่เป็นความลับของเหยื่อ โดยไม่จำเป็นต้องใช้ความรู้ด้านคอมพิวเตอร์ใดๆ ทั้งสิ้น ก็สามารถล่วงรู้ความลับเหยื่อได้โดยง่าย สำหรับนักพัฒนาซอร์ฟแวร์ก็จำเป็นที่จะต้องนำแนวคิดด้านความปลอดภัยของการโจมตีลักษณะนี้ไปเป็นพื้นฐานของการออกแบบซอร์ฟแวร์เพื่อให้เกิดความปลอดภัยแก่ผู้ใช้
## readPassword() คืออะไร
สำหรับนักพัฒนาซอร์ฟแวร์ภาษา Java มีฟังก์ชั่นหนึ่งที่เป็นฟังก์ชั่นด้านความปลอดภัยซึ่งสามารถทำงานได้ในลักษณะเชิงป้องกันการโจมตีแบบ Shoulder Surfing คือ readPassword() ซึ่งเป็นเครื่องมือที่ใช้อ่านค่าข้อมูลจาก Console โดยไม่แสดงผลบนหน้าจอ Console หรือพูดให้เข้าใจง่ายๆ ก็คือรับค่าข้อมูลมาจากผู้ใช้แต่ขณะที่ผู้ใช้ป้อนข้อมูลจะไม่แสดงผลบนหน้าจอ Console สำหรับวันนี้ผมจะแสดงการทำงานของ readPassword() ให้ดูเผื่อท่านผู้อ่านสามารถนำไปประยุกต์ใช้กับสิ่งที่ตัวเองกำลังพัฒนาอยู่ได้ครับ

## Syntax
> public char[] readPassword() 

## ตัวอย่าง
ก่อนอื่นมาสร้างโปรแกรมอย่างง่ายด้วยภาษา Java เพื่อให้รับค่าข้อมูลในที่นี้ผมจะสมมุติให้เป็น Password
![code_readpassword.png](https://peegonggoy.github.io/Code4SecWeek/PicCode4Sec/code_readpassword.png)


### Reference
* https://www.javatpoint.com/java-console-readpassword-method
* https://www.geeksforgeeks.org/java-io-console-class-java/
* https://www.tutorialspoint.com/java/io/console_readpassword.htm