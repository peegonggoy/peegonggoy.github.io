![error.jpg](https://peegonggoy.github.io/Code4SecWeek/PicCode4Sec/error.jpg)

# หา Error ของ Software ที่เขียนด้วย PHP ด้วย error_reporting()
## Intro
PHP เป็นภาษาที่ใช้ในฝั่งของ server ถูกนำมาใช้ในการพัฒนาเวป ซึ่งโดยบางครั้งเราเขียนโปรแกรมจนเสร็จสิ้นแล้ว แต่ผลปรากฎว่า output ที่ออกมาเป็นหน้าว่างๆ หรือมีข้อผิดพลาดแต่ไม่รู้ว่าเกิดขึ้น และจากส่วนไหนของสคริปต์ function error_reporting() ใน PHP สามรถช่วยคุณได้ในการรายงานข้อผิดพลาดที่เกิดขึ้นได้ โดยปกติจะเปิดทันทีหลังจากเปิด <?php.
## PHP Error คืออะไร
PHP error เกิดขึ้นเมื่อมีข้อผิดพลาดใน Code แม้แต่สิ่งเล็กๆ น้อยๆ ก็อาจจะทำให้เกิดข้อผิดพลาดได้ แช่น ข้อผิดพลากที่เกิดจากการเขียน Syntax ไม่ถูกต้อง หรือลืมเครื่องหมาย ; หรือสาเหตุอาจจะซับซ้อนอย่างเช่นการเรียกตัวแปรที่ไม่เหมาะสมซึ่งอาจจะนำไปสู่ข้อผิดพลาดร้ายแรงที่ทำให้ระบบล่มได้

## ตัวอย่างการใช้งาน error_reporting()
    <?php

    // Turn off all error reporting
    error_reporting(0);

    // Report simple running errors
    error_reporting(E_ERROR | E_WARNING | E_PARSE);

    // Reporting E_NOTICE can be good too (to report uninitialized
    // variables or catch variable name misspellings ...)
    error_reporting(E_ERROR | E_WARNING | E_PARSE | E_NOTICE);

    // Report all errors except E_NOTICE
    error_reporting(E_ALL & ~E_NOTICE);

    // Report all PHP errors
    error_reporting(E_ALL);

    // Report all PHP errors
    error_reporting(-1);

    // Same as error_reporting(E_ALL);
    ini_set('error_reporting', E_ALL);

    ?>

## ตัวอย่างการแจ้งเตือนของ error_reporting()
ผมลองเขียน web page ด้วยภาษา PHP และลองใช้คำสั่ง mysql_connect() เพื่อติดต่อไปยังฐานข้อมูลเพื่อดึงข้อมูลออกมาเก็บไว้ในตัวแปร ซึ่งตัวอย่าง code ที่เขียนได้ประมาณนี้ ซึ่งหากสังเกตุดูผมได้ comment function error_reporting() เอาไว้

![dissError.png](https://peegonggoy.github.io/Code4SecWeek/PicCode4Sec/dissError.png)

สำหรับ output ที่ได้ในหน้า web page ก็ได้ประมาณนี้ครับ 

![disErrorOutput.png](https://peegonggoy.github.io/Code4SecWeek/PicCode4Sec/disErrorOutput.png)


ซึ่งถ้าหากผมปลด comment ตรง function error_reporting() ออกซึ่งจะใส่ option level คือให้รายงานข้อผิดพลาดทั้งหมด (E_ALL) และยกเว้นข้อผิดพลาดที่ทำให้เกิด (E_NOTICE)

![error_re.png](https://peegonggoy.github.io/Code4SecWeek/PicCode4Sec/error_re.png)

output ที่ได้ปรากฎว่ามาการแจ้งเตือนข้อผิดพลาดของโปรแกรมขึ้นมาว่า function mysql_connect() อาจจะถูกยกเลิกใช้งานในอนาคตให้มาใช้ mysqli หรือ PDO แทน ดังรูป

![Error.png](https://peegonggoy.github.io/Code4SecWeek/PicCode4Sec/Error.png)

## สรุป
function error_reporting() เป็น function ที่ใช้ในการรายงานข้อผิดพลาดจากการเขียน code ในภาษา PHP ซึ่งเป็นประโยชน์ต่อนักพัฒนาโปรแกรมในการที่จะใช้หาข้อบกพร่องของโปรแกรมและนำไปแก้ไขก่อนที่จะนำไปใช้งานจริง แต่ทั้งนี้เมื่อมีการนำโปรแกรมไปใช้งานจริงก็ควรปิดการแจ้งเตือนหรือลบ function นี้ทิ้งไปเนื่องจากอาจจะเป็น function ที่คอยแจ้งเตือนข้อผิดพลาดซึ่ง Hacker สามารถนำไปใช้ประโยชน์ในการโจมตีได้

### Reference
* https://www.php.net/manual/en/function.error-reporting.php
* https://www.mindphp.com/%E0%B8%84%E0%B8%B9%E0%B9%88%E0%B8%A1%E0%B8%B7%E0%B8%AD/63-%E0%B8%9F%E0%B8%B1%E0%B8%87%E0%B8%81%E0%B9%8C%E0%B8%8A%E0%B8%B1%E0%B9%88%E0%B8%99-php/304-error_reporting.html
* http://www.w3bai.com/th/php/func_error_reporting.html
* https://www.w3schools.com/php/func_error_reporting.asp

### Written by Bhoomjit Bhoominath
