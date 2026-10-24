# บันทึกการแก้โจทย์

ไฟล์นี้ต้องเขียนโดยนักศึกษาด้วยคำพูดของตนเอง

ใช้ template นี้เฉพาะกับโจทย์ OJ ที่ถูกระบุว่าต้องส่ง learning log เท่านั้น

ห้ามให้ AI เขียนไฟล์นี้แทนคุณ AI อาจช่วยตรวจ grammar, formatting หรือความชัดเจนได้ หลังจากที่คุณเขียนเนื้อหาของตนเองแล้ว

ถ้าใช้ AI กับโจทย์ learning-log-required นี้ ต้องทำไฟล์ `ai_reflection.md` ด้วย

---

## 1. ข้อมูล OJ

หมายเลข/ชื่อโจทย์ OJ:

```text
OJ3537 - [LEARNING LOGS] Impostor
```

OJ submission ID ถ้ามีการส่งแล้ว:

```text
	698323
```

สถานะ OJ:

```text
Pass
```

เวลาที่ใช้คิดและทำโจทย์ด้วยตนเอง:

```text
0-15 minutes
```

เลือกหนึ่งข้อ:

```text
0-15 minutes
15-30 minutes
30-60 minutes
1-3 hours
3-6 hours
6-24 hours
1-3 days
4-7 days
1-4 weeks
More than 4 weeks
```

วิธีนับเวลา:

- นับเฉพาะเวลาที่ตั้งใจทำโจทย์นี้ด้วยตนเองจริง ๆ
- เริ่มนับตั้งแต่ตอนที่อ่านโจทย์ครั้งแรก
- ไม่นับเวลาพัก กินข้าว เรียน นอน เวลาที่ทำโจทย์อื่น หรือเวลาที่ไม่ได้ทำโจทย์นี้
- ถ้าใช้ AI ให้นับเฉพาะเวลาที่ทำด้วยตนเองก่อน prompt แรกที่ถาม AI
- ถ้าถามเพื่อน TA หรือผู้สอน ให้นับเฉพาะเวลาที่ทำด้วยตนเองก่อนขอความช่วยเหลือครั้งแรก
- ถ้าใช้ทั้ง AI และความช่วยเหลือจากคน ให้นับเฉพาะเวลาที่ทำด้วยตนเองก่อนขอความช่วยเหลือจากภายนอกครั้งแรก ไม่ว่าจะเป็น AI หรือคน
- ถ้าไม่ได้ใช้ AI และไม่ได้ขอความช่วยเหลือจากคน ให้นับเวลาถึงก่อนเขียน `submission.md`
- ประมาณเวลาได้ แต่ต้องซื่อสัตย์

---

## 2. ความเข้าใจโจทย์ของฉัน

เขียนโจทย์ด้วยคำพูดของตนเอง

ให้อธิบาย input, output และ constraints สำคัญด้วย

ถ้ายังไม่เข้าใจโจทย์ทั้งหมด ให้เขียนสิ่งที่เข้าใจในตอนนี้ ความเข้าใจอาจยังไม่ครบหรืออาจผิดได้ แต่ต้องพยายามอธิบายอย่างจริงใจ

```text
Input:
ส่วนแรก: หลายบรรทัด แต่ละบรรทัดเป็นชื่อและบทบาทของผู้เล่นหนึ่งคน
ในรูปแบบ {"ชื่อ" : "บทบาท"} จนกว่าจะเจอคำว่า Start
ส่วนที่สอง: หลายบรรทัด แต่ละบรรทัดเป็นชื่อของผู้ที่ถูกโหวตไล่ออก จนกว่าจะเจอคำว่า End
Output:
หลายบรรทัด
บรรทัดแรกคือ จำนวน Impostor ที่เหลืออยู่ ตามด้วย Impostor Remains
บรรทัดต่อมาคือ Alive
บรรทัดต่อมาเป็นชื่อผู้รอดชีวิตทุกคนตามด้วยบทบาทระหว่างCrewmate หรือ Impostor จนครบ
บรรทัดต่อมาคือ Dead
บรรทัดที่เหลือคือชื่อผู้ที่เสียชีวิตตามด้วยบทบาทระหว่างCrewmate หรือ Impostor
(เรียงตามตัวอักษร)

Constraints:
ต้องใช้ dict และ dict methods
ชื่อเป็นกุญแจของ dict จึงควรไม่ซ้ำกัน
ถ้าไม่มีใครถูกไล่ออก หรือไม่มีใครรอด ยังต้องพิมพ์หัวข้อ ***Alive*** และ ***Dead*** ตามเดิม
```

---

## 3. แผนแรกของฉัน

เขียนแผนแรกก่อนรับความช่วยเหลือจาก AI เพื่อน TA ผู้สอน หรือก่อนสรุป code สุดท้าย

ถ้าใช้ AI ให้เขียนแผนที่มีอยู่ก่อน prompt แรกที่ถาม AI

ถ้าถามเพื่อน TA หรือผู้สอน ให้เขียนแผนที่มีอยู่ก่อนถาม

ถ้าไม่ได้ใช้ AI และไม่ได้ขอความช่วยเหลือจากคน ให้เขียนแผนที่มีอยู่ก่อนหรือระหว่างเริ่มเขียน code

แผนนี้เขียนแบบคร่าว ๆ ได้ อาจยังไม่สมบูรณ์หรืออาจต่างจากวิธีสุดท้าย

สามารถเขียนเป็น pseudocode, flowchart idea หรือขั้นตอนความคิดได้

```text
Step 1: สร้าง dict ว่าง players ไว้เก็บชื่อและบทบาทของผู้เล่นทุกคน
Step 2: อ่านทีละบรรทัดจนกว่าจะเจอคำว่า Start
Step 3: แต่ละบรรทัดที่อ่านมา ตัดเครื่องหมาย { } และ ออกแยกชื่อกับบทบาทด้วย : แล้วเก็บลง players โดยใช้ชื่อเป็น key และบทบาทเป็น value
Step 4: อ่านรายชื่อผู้ถูกโหวตไล่ออกทีละบรรทัดจนกว่าจะเจอคำว่า End แล้วเก็บไว้ในลิสต์ votes
Step 5: สร้าง dict alive โดยคัดลอกจาก players และสร้าง dict dead ว่างไว้
Step 6: วนดูแต่ละชื่อใน votes ถ้าชื่อนั้นยังอยู่ใน alive ให้ใช้ pop ย้ายออกจาก alive ไปเก็บใน dead พร้อมบทบาทเดิม ถ้าไม่อยู่ใน alive ให้ข้ามไป
Step 7: นับจำนวน Impostor ที่เหลือใน alive โดยใช้ values แล้วนับคำว่า Impostor
Step 8: พิมพ์ จำนวน Impostor Remains
Step 9: พิมพ์ ***Alive*** แล้ววนชื่อใน alive ที่เรียงตามตัวอักษร พิมพ์ในรูปแบบ ชื่อ : บทบาท
Step 10: พิมพ์ ***Dead*** แล้วทำแบบเดียวกันกับ dead
```

---

## 4. วิธีสุดท้ายที่ใช้จริง

อธิบายสั้น ๆ ว่า algorithm หรือวิธีสุดท้ายที่ใช้จริงใน code ที่ส่งคืออะไร

หัวข้อนี้ต่างจาก Section 3:

- Section 3 คือแผนแรกก่อนใช้ AI ก่อนรับความช่วยเหลือจากคน หรือก่อนเขียน code สุดท้าย
- Section 4 คือวิธีสุดท้ายที่ใช้ใน solution จริง
- ถ้าวิธีสุดท้ายเหมือนกับแผนแรก ให้เขียนว่าเหมือนกัน และอธิบายสั้น ๆ ว่าทำไม

ห้ามคัดลอกคำอธิบายจาก AI

ห้ามคัดลอกคำอธิบายจากคนอื่น

```text
เหมือนแผนแรกค้ดอ่านข้อมูลผู้เล่นเก็บใน dict ชื่อเป็น key บทบาทเป็น valu จนเจอ Start แล้วอ่านรายชื่อผู้ถูกโหวตเก็บในลิสต์ จนเจอ end จากนั้นคัดลอก dict เป็น alive และใช้ pop ย้ายผู้ที่ถูกโหวตไป dead
```

---

## 5. การทดสอบของฉัน

เขียน test cases อย่างน้อย 3 กรณีที่ลองเองหรือออกแบบเอง

พยายามเลือก test cases ที่แตกต่างกัน

แต่ละ test case ให้อธิบายว่าทำไมเลือกกรณีนั้น

ถ้า input หรือ output มีหลายบรรทัด ให้เขียนไว้ใน text blocks

### Test Case 1

ทำไมเลือก case นี้:

```text
ไม่มีใครโดนเลยวะ
```

Input:

```text
{"Red" : "Crewmate"}
{"Blue" : "Impostor"}
Start
End
```

Expected output:

```text
1 Impostor Remains
***Alive***
Blue : Impostor
Red : Crewmate
***Dead***
```

Actual output:

```text
1 Impostor Remains
***Alive***
Blue : Impostor
Red : Crewmate
***Dead***
```

Result:

```text
Pass
```

### Test Case 2

ทำไมเลือก case นี้:

```text
โหล่ๆ โวตคนซ้ำได้ไงอะ
```

Input:

```text
{"Red" : "Crewmate"}
{"Blue" : "Impostor"}
{"Lime" : "Crewmate"}
Start
Blue
Blue
Pink
End
```

Expected output:

```text
0 Impostor Remains
***Alive***
Lime : Crewmate
Red : Crewmate
***Dead***
Blue : Impostor
```

Actual output:

```text
0 Impostor Remains
***Alive***
Lime : Crewmate
Red : Crewmate
***Dead***
Blue : Impostor
```

Result:

```text
Pass
```

### Test Case 3

ทำไมเลือก case นี้:

```text
โดนโหวดกันหมดเลย
```

Input:

```text
{"red" : "Crewmate"}
{"Blue" : "Impostor"}
Start
red
Blue
End
```

Expected output:

```text
0 Impostor Remains
***Alive***
***Dead***
Blue : Impostor
red : Crewmate
```

Actual output:

```text
0 Impostor Remains
***Alive***
***Dead***
Blue : Impostor
red : Crewmate
```

Result:

```text
Pass
```

---

## 6. การใช้ AI

ใช้ AI กับโจทย์นี้หรือไม่

```text
No
```

ถ้าใช้ AI ต้องทำไฟล์นี้ด้วย:

```text
ai_reflection.md
```

ถ้าถามเฉพาะเพื่อน TA หรือผู้สอน และไม่ได้ใช้ AI ไม่ต้องทำ `ai_reflection.md`

---

## 7. ความช่วยเหลือจากคน / การร่วมมือ

ได้ถามเพื่อน TA ผู้สอน หรือบุคคลอื่นเพื่อขอความช่วยเหลือในโจทย์นี้หรือไม่

```text
No
```

ถ้าใช่ ให้อธิบายสั้น ๆ ว่าได้รับความช่วยเหลือแบบใด

ตัวอย่างที่อนุญาต:

- อธิบายความหมายของโจทย์
- อธิบาย concept การเขียนโปรแกรม
- ให้ hint เกี่ยวกับแนวทาง
- คุยเรื่อง debugging
- คุยเรื่อง test cases
- ช่วยอธิบาย error message

สิ่งที่ไม่อนุญาต:

- คัดลอก code ของผู้อื่น
- ส่ง solution ของผู้อื่น
- ขอให้ผู้อื่นเขียน solution ให้
- ใช้ OJ submission ของผู้อื่น
- ขอให้ผู้อื่นส่ง OJ แทน

ใครช่วยคุณ

```text

```

เขาช่วยอะไร

```text

```

คุณยังทำอะไรด้วยตนเอง

```text

```

คุณคัดลอก code จากคนอื่นหรือไม่

```text
No
```

---

## 8. คำรับรองของนักศึกษา

เขียน `Yes` ในแต่ละ statement

| Statement | Yes/No |
|---|---|
| I wrote this submission in my own words. | Yes |
| I understand my final code. | Yes |
| I recorded the real OJ status. | Yes |
| I did not copy AI-generated text directly into this file. | Yes |
| I did not copy code from another person. | Yes |
| If I received human help, I disclosed it in this file. | Yes |
| I submitted the final code to the OJ by myself. | Yes |
