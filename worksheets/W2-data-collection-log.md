<!-- workshop-header -->
<img width="1347" height="127" alt="Coding Thailand 2026 header" src="https://github.com/user-attachments/assets/ba5cf267-f460-4fb0-b69b-c461ae061a3b" />

# 📝 Worksheet W2 — Data Collection Log

> **ทำในช่วง 10:30-12:00**
> บันทึก process ของการเก็บข้อมูล

---

## ข้อมูลทีม + Edge Impulse

- **ชื่อทีม:** WNY"ครูอ๋าบังคับให้มา"
- **Edge Impulse Project URL:**
  ```
  https://studio.edgeimpulse.com/studio/XXXXX
  ```

---

## 1. Setup Log

ก่อนเริ่มเก็บข้อมูล ทีมทำอะไรบ้าง?

| เวลา | ทำอะไร | ผู้รับผิดชอบ |
|---|---|---|
| 10:30 | เตรียมพร้อมระบบ | ด.ช.สรไกร น้อยสืบสาย |
| 10:35 | รวบรวมข้อมูล | ด.ช.ภูมิธรรม ไวคิด |

---

## 2. Data Collection Sessions

บันทึกแต่ละ session การเก็บข้อมูล:

### Session 1

- **เวลา:** 10:30 ถึง 15:00
- **Class:** Smartlight SmartSwitch Sensor
- **จำนวน samples ที่เก็บ:** 2 เลเบล
- **สภาพแวดล้อม:** ห้องเสียงที่มีเสียงรบกวน
- **ใครเป็น subject?:** สมาชิกในทีม 3 คน
- **Variation ที่ลอง:** ระดับเสียง ความเร็วช้าของเสียง
- **ปัญหาที่เจอ:** การเชื่อมต่อบอร์ด Arduino uno q

### Session 2

- **เวลา:** 15:30 ถึง 16:30
- **Class:** Smartlight SmartSwitch Sensor
- **จำนวน samples ที่เก็บ:** 2 ลาเบล
- **สภาพแวดล้อม:** ห้องเสียงที่มีเสียงรบกวน
- **ใครเป็น subject?:** สมาชิกในทีม 3 คน
- **Variation ที่ลอง:** ระดับเสียง ความเร็วช้าของเสียง ระยะห่างจากเสียง
- **ปัญหาที่เจอ:** การเทรนโมเดล

### Session 3

- **เวลา:** 16:30 ถึง 17:00
- **Class:** Smartlight SmartSwitch Sensor
- **จำนวน samples ที่เก็บ:** 3 ลาเบล
- **สภาพแวดล้อม:** ห้องเสียงที่มีเสียงรบกวน
- **ใครเป็น subject?:** สมาชิกในทีม 3 คน
- **Variation ที่ลอง:** ระดับเสียง ความเร็วช้าของเสียง ระยะห่างจากเสียง
- **ปัญหาที่เจอ:** การเทรนโมเดล

> หาก session มากกว่า 3 ให้ copy template เพิ่ม

---

## 3. Dataset Summary

| Class | จำนวน Train | จำนวน Test | สัดส่วน Train:Test |
|---|---|---|---|
| turn_on | 10 | 1 | 10:1 |
| turn_off | 10 | 1 | 10:1 |
| noise | 10 | 1 | 10:1 |
| **รวม** |  | | |

**เป้าหมายตาม W1:** _______ samples × class
**ทำได้จริง:** _______ samples × class
**ห่างจากเป้า:** _______%

---

## 4. Quality Check

ตอบทุกข้อก่อนเริ่ม train:

- [ ] ทุก class มี samples ใกล้เคียงกัน (ไม่ต่างกันเกิน 20%)
- [ ] เก็บใน ≥2 สภาพแวดล้อม
- [ ] เก็บจาก ≥2 subjects (Vision/Audio/Motion ที่มีคน)
- [ ] มี variation ใน angle/distance/lighting
- [ ] ไม่มี mislabeled data (เช็คตัวอย่างแล้ว)
- [ ] Train:Test split = 80:20

---

## 5. Reflection — สิ่งที่เรียนรู้

### a) สิ่งที่ยากที่สุด:
```
[เขียนสั้นๆ]
```

### b) ถ้าทำใหม่จะปรับอะไร:
```
[เขียนสั้นๆ]
```

### c) คาดการณ์: model จะ confuse class ไหนกับอะไรมากที่สุด?
```
[เขียนการคาดเดา — เราจะมาเช็คตอน Train เสร็จ]
```

---

## 📤 วิธี submit

```bash
git add worksheets/W2-data-collection-log.md
git commit -m "docs: data collection log เก็บได้ครบ X samples ใน Y session"
git push
```

---

## 💡 Best Practices

1. **อย่าเก็บข้อมูลที่ "สมบูรณ์แบบ" หมด** — โลกจริงไม่สมบูรณ์แบบ
2. **เก็บข้อมูล "เหมือนไม่ใช่ class ใดเลย" เป็นอีก class** = noise/background class
3. **สลับคนเก็บ** — กัน bias ของ subject เดียว
4. **เช็คตัวอย่างทุก 20 samples** — กัน mislabel
