# lab7-4_esp32 การใช้ Component Registry Manager

### หลังจาการใช้ 
#### การค้นหา Component

```bash
# ค้นหา component ที่เกี่ยวกับ sensor
idf.py create-project-from-example "espressif/esp_insights:diagnostics_smoke_test"

# ดู component ที่ติดตั้งแล้ว
idf.py dependency-tree
```

#### การจัดการ Dependencies

```bash
# เพิ่ม component ใหม่
idf.py add-dependency "espressif/led_strip^2.0.0"

# อัพเดท component
idf.py update-dependencies
```

## ความแตกต่างจาก Lab ก่อนหน้า

- **Lab 7-1**: ใช้ local component (อยู่ใน `components/`)  
- **Lab 7-2**: ใช้ managed component จาก GitHub URL  
- **Lab 7-3**: สร้าง component ใหม่เองด้วย `idf.py create-component`  
- **Lab 7-4**: ใช้ **Component Registry Manager** ในการค้นหา/จัดการ dependencies  

## สรุป
การใช้ **Component Registry Manager** ทำให้:
- ค้นหา component ได้จากออนไลน์
- ติดตั้ง/อัปเดตอัตโนมัติ
- ลดเวลาในการตั้งค่าและแชร์ project ระหว่างทีม
- ได้เวอร์ชันที่สอดคล้องและทดสอบแล้วกับ ESP-IDF