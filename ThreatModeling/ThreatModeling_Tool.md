# **Microsoft Threat Modeling Tool**
Threat Modeling Tool เป็นเครื่องมือหลักของ Security Development Lifecycle (SDL) ที่ช่วยให้นักพัฒนาซอฟต์แวร์สามารถระบุ และแก้ไขปัญาด้านความปลอดภัยที่เกี่ยวข้องกับการซอฟต์แวร์ที่จะพัฒนาขึ้น ตั้งแต่เนิ่นๆ ซึ่งส่งผลให้เป็นการลดต้นทุนทั้งหมดในการพัฒนาซอฟต์แวร์ที่จะนำไปใช้ในภาคธุรกิจ ดังนั้น Micorsoft จึงออกแบบเครื่องมือนี้ขึ้นเพื่อทำให้นักพัฒนาซอฟต์แวร์ได้นำไปใช้ในการสร้างแบบจำลองภัยคุกคาม โดยให้คำแนะนำที่ชัดเจนในการสร้างและวิเคราะห์รูปแบบของภัยคุกคาม ที่อาจจะส่งผลกระทบต่อระบบและซอฟต์แวร์ ซึ่งช่วยสร้างความสะดวกสบายให้แก่นักพัฒนาซอฟต์แวร์ได้ทำการวิเคราะ์ช่องโหว่ของซอฟต์แวร์ที่พัฒนาขึ้นได้ง่ายขึ้น
### **Microsoft Threat Modeling Tool ช่วยให้เราสามารถ :**
* เป็นเครื่องมือในการสื่อสารด้านการออกแบบการรักษาความปลอดภัยของระบบ
* วิเคราะห์ปัญหาด้านความปลอดภัยที่อาจจะกระทบต่อซอฟต์แวร์ที่กำลังออกแบบ
* แนะนำวิธีการจัดการปัญหาด้านความปลอดภัย
### **ความสามารถของ Microsoft Threat Modeling Tool :**
* เป็นระบบอัตโนมัติ : ให้คำแนะนำและข้อเสนอแนะในการวาดแบบจำลองของสภาพแวดล้อมที่จะนำซอฟต์แวร์ไปติดตั้ง
* STRIDE : การวิเคราะห์ภัยคุกคามและข้อเสนอแนะการลดผลกระทบที่จะเกิดขึ้น
* การรายงาน : กิจกรรมด้านความปลอดภัยและการทดสอบในขั้นตอนการตรวจสอบ
* เครื่องมือพิเศษ : ช่วยให้ผู้ใช้เห็นภาพและเข้าใจภัยคุกคามได้ดีขึ้น
* ออกแบบสำหรับผู้พัฒนาซอฟต์แวร์โดยมีศูนย์กลางอยู่ที่ซอฟต์แวร์ : สำหรับการทำ Threat Modeling หลายๆ แนวทางเน้นไปที่ Assets หรือ Attackers แต่ Microsoft Threat Modeling Tool 
* มุ่งเน้นไปที่การวิเคราะห์การออกแบบ : คำว่า Threat Modeling เราสามารถอ้างอิงจาก Requirement หรือ เทคนิคการวิเคราะห์การออกแบบซอฟต์แวร์ และบางครั้งมันถูกอ้างอิงจากความซับซ้อนจากทั้ง 2 อย่าง ซึ่งแนวทางการสร้าง Threat Modeling ของ Microsoft SDL จะมุ่งเน้นไปที่เทคนิคการวิเคราะห์การออกแบบซอฟต์แวร์ 
## **Starting the threat modeling process**
หากสรุปขั้นตอนคร่าวๆ ของ Microsoft Threat Modeling Tool ประกอบด้วย 4 ขั้นตอน คือ
1. สร้าง Diagram
2. การยืนยันภัยคุกคามที่จะเกิดขึ้น (STRIDE)
3. การลดความเสี่ยงที่จะถูกโจมตี
4. การตรวจสอบ

![MSTMT2](https://github.com/peegonggoy/peegonggoy.github.io/blob/main/ThreatModeling/Pic/MSTMT2.png?raw=true)

เราสามารถ Download Microsoft Threat Modeling Tool ได้ที่นี่ [Download program](https://aka.ms/threatmodelingtool) 

## **Lunch the program**
เมื่อเราเปิดโปรแกรม Microsoft Threat Modeling Tool ขึ้นมาหน้าตาก็จะเป็นดังภาพ
![MSTMT1](https://github.com/peegonggoy/peegonggoy.github.io/blob/main/ThreatModeling/Pic/MSTMT1.png?raw=true)

## **Threat model section**
|เครื่องมือ|รายละเอียด|
|------|-------|
|Feedback, Suggestions and Issues Button|จะนำคุณไปยังหน้า page ของ [MSDN](https://social.msdn.microsoft.com/Forums/en-US/home?forum=sdlprocess) ซึ่งจะรวบรวมปัญหาข้อขัดข้องในการใช้งาน Microsoft Threat Modeling Tool ของผู้ใช้ทั่วโลก และคำแนะนำต่างๆ ซึ่งเป็นโอกาสในการแลกเปลี่ยนประสบการณ์การใช้งานเครื่องมือนี้  ถ้าหากยังไม่สามารถแก้ไขปัญหาที่เกิิดขึ้นได้ก็สามารถที่จะ Email ไปถามทีมงานของ Microsoft ได้โดยตรงที่ Email นี้ tmtextsupport@microsoft.com|
|Create a Model|เปิดพื้นที่ว่างเพื่อให้คุณวาด Diagram อย่าลืมเลือกเทมเพลตที่คุณต้องการใช้สำหรับโมเดลของคุณ|
|Template for New Models|คุณต้องเลือกเทมเพลตที่จะใช้ก่อนสร้างโมเดล ซึ่งค่า Default ของ Template คือ Azure Threat Model Template ซึ่งมี stencils เฉพาะของ Azure ซึ่งเราสามารถสร้าง Template ให้เหมาะสมกับงานที่เรากำลังออกแบบอยู่ได้|
|Open a Model|เปิด Model ที่บันทึกไว้ในเครื่องคอมพิวเตอร์ก่อนหน้านี้|
|Getting Started Guide|เปิด คำแนะนำในการใช้งาน Microsoft Threat Modeling Tool|

## **Template section**
|เครื่องมือ|รายละเอียด|
|------|-------|
|Create New Template|เป็นการเปิด Template ใหม่เพื่อสร้างให้เหมาะสมกับสิ่งที่เรากับลังออกแบบ แต่ทาง Microsoft แนะนำให้ใช้ Template ที่มีอยู่ยกเว้นมีความรู้มากพอที่จะสร้าง|
|Open Template|เปิดเทมเพลตที่มีอยู่เพื่อทำการเปลี่ยนแปลง|

## **การสร้าง Model**
ทำการเปิดโปรแกรมขึ้นมา แล้วเลือก Template ในช่อง Template for New Models ทำการคลิ๊กที่ Create Model ก็จะได้หน้าว่างป่าวดังรูป เราก็สามารถทำการสร้างโมเดลได้ตามที่เราต้องการจาก Stencil ทางด้านขวามือ
![MSTMT3](https://github.com/peegonggoy/peegonggoy.github.io/blob/main/ThreatModeling/Pic/MSTMT3.png?raw=true)

ในที่นี่ผมจะใช้ Template ตัวอย่างให้มาด้วยกับตัวโปรแกรมเพื่อจะใช้ทำการวิเคราะห์หน้าตาก็จะเป็นดังรูปครับ
![MSTMT4](https://github.com/peegonggoy/peegonggoy.github.io/blob/main/ThreatModeling/Pic/MSTMT4.png?raw=true)
## **การวิเคราะห์ภัยคุกคาม**
เมื่อคลิกที่มุมมองการวิเคราะห์ (รูปแว่นขยาย)

![MSTMT5](https://github.com/peegonggoy/peegonggoy.github.io/blob/main/ThreatModeling/Pic/MSTMT5.png?raw=true)

ตัวโปรแกรมก็จะเข้าสู่รายการภัยคุกคามที่สร้างขึ้นซึ่งสร้างตามแบบจำลองที่เรียกว่า [STRIDE (Spoofing, Tampering, Info Disclosure, Repudiation, Denial of Service and Elevation of Privilege)](https://en.wikipedia.org/wiki/STRIDE_(security)) วิธีการนี้เป็นการตรวจสอบว่าระบบ หรือ Software ที่สร้างขึ้นมา ถูกปิดช่องโหว่จากการถูกโจมตีก่อนที่จะนำระบบหรือ Software ไปใช้งานจริงๆ ซึ่งหน้าตาก็จะเป็นดังภาพ

![MSTMT7](https://github.com/peegonggoy/peegonggoy.github.io/blob/main/ThreatModeling/Pic/MSTMT7.png?raw=true)

เมื่อเราทำการคลิ๊กเลือกตรงช่อง Threat list ID หมายเลข 1 ก็จะทำให้เราเห็นความสัมพันธ์ ระหว่าง 2 Stencil ที่สร้างขึ้นมา

![MSTMT8](https://github.com/peegonggoy/peegonggoy.github.io/blob/main/ThreatModeling/Pic/MSTMT8.png?raw=true)

และต่อมาก็จะเห็นรายละเอียดของภัยคุกคามที่จะเกิดขึ้นระหว่างระหว่างความสัมพันธ์ของ 2 Stencils 

![MSTMT9](https://github.com/peegonggoy/peegonggoy.github.io/blob/main/ThreatModeling/Pic/MSTMT9.png?raw=true)

ภัยคุกคามที่โปรแกรมสร้างขึ้นช่วยให้เราเข้าใจข้อบกพร่องในการออกแบบที่อาจเกิดขึ้น ในขณะที่คำอธิบายเพิ่มเติมจะบอกเราว่ามีอะไรผิดปกติพร้อมกับวิธีแก้ไขที่เป็นไปได้ เราสามารถกำหนดความเร่งด้วยและแนวทางการแก้ไขแล้วสามารถกรอกลงในช่อง Justification เพื่อเป็นแนวทางในการให้คนอื่นแก้ไข

## **Report & Sharing**
เมื่อเราต้องการทำรายงานเป็นเอกสารเพื่อให้ทีมในการพัฒนาระบบและ Software ได้รับทราบถึงภัยคุกคามต่างๆ ที่อาจจะเกิดขึ้นต่อ ระบบและ Software ที่กำลังออกแบบ รวมถึงแนวทางการแก้ไขและความเร่งด่วนในการแก้ไขที่ถูกสร้างขึ้นในขั้นตอนก่อนหน้า ให้ทำการไปที่เมนู Reports -> Create Full Report -> Save Report ก็จะได้รายงานดังรูป

