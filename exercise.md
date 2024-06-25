# WEEK 4 Exercises - Making Queries

![ERD-E-COMMERCE](https://github.com/it-web-pro/django-week3/blob/main/images/WEEK3-ERD(e-commerce).png?raw=true)

<br/>

###  ต่อจากแบบฝึกหัด week3 ให้นักศึกษา run ไฟล์ `shop.sql` เพื่อเป็นการเพิ่มข้อมูลลงใน database

## 1. ให้นักศึกษา Query ค้นหาข้อมูลมาแสดงให้ถูกต้องตามโจทย์ (0 คะแนน)
1.1 query หาข้อมูล `Order` ทั้งหมดที่เกิดขึ้นในเดือน `พฤษภาคม` มาแสดงผล 10 รายการแรก และแสดงผลดังตัวอย่าง

```
ORDER ID:22, DATE: 2024-05-01
ORDER ID:23, DATE: 2024-05-01
ORDER ID:24, DATE: 2024-05-01
ORDER ID:25, DATE: 2024-05-02
ORDER ID:26, DATE: 2024-05-02
ORDER ID:27, DATE: 2024-05-02
ORDER ID:28, DATE: 2024-05-03
ORDER ID:29, DATE: 2024-05-03
ORDER ID:30, DATE: 2024-05-03
ORDER ID:31, DATE: 2024-05-04
```

1.2 query หาข้อมูล `Product` ที่มีคำลงท้ายว่า `features.` ในรายละเอียกสินค้า และแสดงผลดังตัวอย่าง

```
PRODUCT ID: 1, DESCRIPTION: A sleek and powerful smartphone with advanced features.
PRODUCT ID: 7, DESCRIPTION: High-resolution digital camera with advanced photography features.
PRODUCT ID: 10, DESCRIPTION: A stylish smartwatch with health monitoring and notification features.
PRODUCT ID: 14, DESCRIPTION: Split air conditioner with remote control and energy-saving features.
PRODUCT ID: 45, DESCRIPTION: Customizable racing track set with loop and jump features.
```

1.3 query หาข้อมูล `Product` ที่มีราคาสินค้าตั้งแต่ `5000.00` ขึ้นไป และแสดงผลดังตัวอย่าง

```
PRODUCT ID: 1, NAME: Smartphone, PRICE: 5900.00
PRODUCT ID: 2, NAME: Laptop, PRICE: 25999.00
PRODUCT ID: 3, NAME: Smart TV, PRICE: 8900.00
PRODUCT ID: 5, NAME: Tablet, PRICE: 12900.00
PRODUCT ID: 6, NAME: Gaming Console, PRICE: 5000.00
PRODUCT ID: 7, NAME: Digital Camera, PRICE: 32000.00
PRODUCT ID: 11, NAME: Refrigerator, PRICE: 9000.00
PRODUCT ID: 14, NAME: Air Conditioner, PRICE: 18900.00
PRODUCT ID: 31, NAME: Sofa, PRICE: 7000.00
PRODUCT ID: 54, NAME: Automatic Pet Feeder, PRICE: 7900.00
PRODUCT ID: 61, NAME: Diamond Stud Earrings, PRICE: 320000.00
PRODUCT ID: 62, NAME: Silver Charm Bracelet, PRICE: 70000.00
PRODUCT ID: 63, NAME: Gold Pendant Necklace, PRICE: 59000.00
PRODUCT ID: 64, NAME: Gemstone Ring, PRICE: 9000.00
PRODUCT ID: 65, NAME: Rose Gold Hoop Earrings, PRICE: 1200000.00
```

1.4 query หาข้อมูล `Product` ที่มีราคาสินค้าน้อยกว่า `200.00` และแสดงผลดังตัวอย่าง

```
PRODUCT ID: 28, NAME: Women's Sweater, PRICE: 190.00
PRODUCT ID: 53, NAME: Pet Food Bowl Set, PRICE: 90.00
```


## 2. เพิ่ม ลบ แก้ไข สินค้า (0 คะแนน)
### หมวดหมู่สินค้า
- Information technology
- Electronics
- Clothing and Apparel
- Home Appliances
- Furniture
- Toys and Games
- Books and Media
- Pet Supplies
- Jewelry

<br/>

2.1 ให้เพิ่มสินค้าใหม่จากนั้นนำข้อมูลที่เพิ่มล่าสุดมาแสดงผลให้ถูกต้อง โดยให้ ชื่อสินค้า, ราคา และจำนวนคงเหลือ
```
สินค้าที่ 1
ชื่อ: Philosopher's Stone (1997)
หมวดหมู่สินค้า: Books and Media
จำนวนคงเหลือ: 20
รายละเอียดซ: By J. K. Rowling.
ราคา: 790

สินค้าที่ 2
ชื่อ: Me Before You
หมวดหมู่สินค้า: Books and Media
จำนวนคงเหลือ: 40
รายละเอียดซ: A romance novel written by Jojo
ราคา: 390

สินค้าที่ 3
ชื่อ: Notebook HP Pavilion Silver
หมวดหมู่สินค้า: Information technology และ Electronics
จำนวนคงเหลือ: 10
รายละเอียดซ: Display Screen. 16.0
ราคา: 20000
```

2.2 แก้ไขชื่อสินค้า จาก `Philosopher's Stone (1997)` เป็น `Half-Blood Prince (2005)` 

2.3 แก้ไขชื่อหมวดหมู่สินค้า จาก `Books and Media` เป็น `Books` 

2.4 ลบสินค้าทุกตัวที่อยู่ในหมวดหมู่ `Books`
