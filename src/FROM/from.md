## FROM

คำสั่ง `FROM` เป็นคำสั่งที่อยู่ภายใน `Dockerfile` ซึ่งจะเป็นการบอกที่มาของ image นั้น โดยจะ initialize การ set image ให้ทำตามคำสั่งต่างๆ ถัดไป
ใน Dockerfile มักเริ่มต้นคำสั่งด้วย คำสั่ง FROM จะมีได้หลายคำสั่งในไฟล์เดียวก็ได้ สำหรับสร้างหลาย image เราสามารถตั้งชื่อให้กับ stage ได้โดยเพิ่ม
`AS name` ใน `FROM` 

**ตัวอย่างคำสั่ง FROM**

```dockerfile
    FROM [--platform=<platform>] <image> [AS <name>]
```
หรือ


```dockerfile
    FROM [--platform=<platform>] <image>[:<tag>] [AS <name>]
```

หรือ

```dockerfile
    FROM [--platform=<platform>] <image>[@<digest>] [AS <name>]

```
การใช้ `tag` หรือ `digest` จะมีหรือไม่มีก็ได้ หากไม่มีการเลือกตัวใดตัวหนึ่ง builder จะใช้ `tag` ตัวล่าสุดเป็นค่า default builder จะคืนค่า 
error ถ้าไม่สามารถหา `tag` เจอ
สามารถใช้ `--platform` flag ในการระบุ platform ของ image ในกรณีที่ `FROM` อ้างอิงถึงหลาย platform
