# รายงานวิชาCN210
## สรุปเนื้อหาการบ้านครั้งที่ 1
**MIPS Instruction format**
MIPS คอมพิวเตอร์ชนิด RISC ผลิตโดย MIPS Technologies ซึ่งในทุกๆคำสั่งของ MIPS จะมีขนาด 32 bit ประกอบด้วย 3 ชนิดด้วยกัน คือ
**R-Format** -เป็นคำสั่งที่ใช้ดำเนินการทางคณิตศาสตร์และตรรกศาสตร์ มีโครงสร้างต่อไปนี้
|**R-Format**|     |     |     |     |     |
|------------|-----|-----|-----|-----|-----|
|     op     | $rs | $rt | $rd |shamt|func |
|     6bit     | 5bit| 5bit| 5bit|5bit |6bit |
|**คำสั่ง**    |     |     |     |     |     |
|ALU| alu | $rd | $rs | $rt |    |
|JR | jr | $rs |   |   |   |

สำหรับ R-Format นั้นส่วนใหญ่จะเป็นคำสั่งทางคณิตศาสตร์ เช่น คำสั่ง add เพื่อบวกกัน sub เพื่อลบ
โดยขั้นตอนในการทำคำสั่ง ADD นั้นจะมีดังนี้
1. ทำการอ่าน op-code ซึ่งสำหรับ R-Format จะเป็น 000000
2. เช็คว่า func มีค่าเป็นอะไรเช่น หาก func มีค่าเป็น 100000 จะเป็นคำสั่ง ADD
3. จากตัวอย่างที่ยกมา ให้ค่า func เป็นคำสั่ง ADD จะทำการบวกกันโดยนำค่าที่เก็บอยู่ใน $rs และ $rt มาทำการบวกกัน หลังจากนั้นนำผลลัพธ์ที่ได้ไปเก็บใน $rd

**I-Format** -เป็นคำสั่งที่ใช้ย้ายข้อมูล
|**I-Format**|     |     |     |
|------------|-----|-----|-----|
|     op     | $rs | $rt | offset |
|     6bit   | 5bit| 5bit| 16bit  |
|**คำสั่ง**    |     |     |        |         |  
|ALUi        |alui | $rt | $rs     | value   |
|Data Transfer | lw | $rt | offset($rs)  |   |   |
|             |  sw | $rt | offset($rs)  |   |   |
|Branch      |  beq | $rs | $rt | offset |   |   |


* งานครั้งที่ 1
  [คลิปงานครั้งที่ 1](https://www.youtube.com/watch?v=uxKd0FtUXx8&t=9s)
* งานครั้งที่ 2
  [คลิปงานครั้งที่ 2](https://www.youtube.com/watch?v=afBzikgJ6VA)
  อธิบายหลักการทำงานของ CPU ในคอมพิวเตอร์
* งานครั้งที่ 3
  [คลิปงานครั้งที่ 3](https://www.youtube.com/watch?v=D7P8hxrkiEY)
  อธิบายความแตกต่าง Single Cycle และ Multi Cycle
* งานครั้งที่ 4
  [คลิปงานครั้งที่ 4](https://www.youtube.com/watch?v=dOmY8EDUxi0&t=19s)
  อธิบายการทำงานของคำสั่ง lw ใน cycle
* งานครั้งที่ 5
  [คลิปงานครั้งที่ 5](https://www.youtube.com/watch?v=IAmkzRGe4yQ&t=14s)
  อธิบายการทำงานของคำสั่ง beq ใน cycle
* งานครั้งที่ 6
  [คลิปงานครั้งที่ 6](https://www.youtube.com/watch?v=kINS_f38R6I&t=9s)
* งานครั้งที่ 7
  [คลิปงานครั้งที่ 7](https://www.youtube.com/watch?v=NQ4u19d90rE&t=1s)
