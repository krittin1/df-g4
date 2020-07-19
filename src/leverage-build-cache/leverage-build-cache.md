## Leverage build cache

### ใช้ cache ช่วยในการ build image

เวลามีการ build image เกิดขึ้น Docker จะทำตามคำสั่งต่างๆ ที่อยู่ภายใน `Dockerfile` เมื่อมีการสร้าง image Docker จะหา image ใน cache ว่าเคยมีอยู่ก่อนหรือไม่เพื่อทำการ reuse image 
ซึ่งจะช่วยให้การสร้าง image นั้นเร็วขึ้นไม่ต้องเสียเวลาสร้างใหม่อีก แต่ถ้าไม่ต้องการใช้ cache สามารถใช้คำสั่ง `--no-cache=true` ใน `docker build` ได้
