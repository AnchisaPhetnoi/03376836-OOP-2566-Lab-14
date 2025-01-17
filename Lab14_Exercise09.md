# Lab 14 Exercise 9

## Generic queue

1.สร้าง console application project

```cmd
dotnet new console --name Lab14_Ex09
```

2.เปลี่ยน code ให้เป็นดังต่อไปนี้

```cs
using System;
using System.Collections.Generic;

Queue<string> planets = new Queue<string>();

System.Console.WriteLine("Add planets (Mercury to Pluto)");
planets.Enqueue("Mercury");
planets.Enqueue("Venus");
planets.Enqueue("Earth");
planets.Enqueue("Mars");
planets.Enqueue("Jupiter");
planets.Enqueue("Saturn");
planets.Enqueue("Uranus");
planets.Enqueue("Neptune");
planets.Enqueue("Pluto");

System.Console.WriteLine("Items in queue:");
foreach (var item in planets)
{
    System.Console.WriteLine(item);
}

System.Console.Write("Remove first item in queue : ");
var removeItem = planets.Dequeue();
System.Console.WriteLine(removeItem);

System.Console.WriteLine("Remaining items in queue:");
foreach (var item in planets)
{
    System.Console.WriteLine(item);
}
```

3.Build project โดยการใช้คำสั่ง

```cmd
dotnet build  Lab14_Ex09
```

ถ้ามีที่ผิดพลาดในโปรแกรม ให้แก้ไขให้ถูกต้อง

4.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 3
![image](https://github.com/AnchisaPhetnoi/03376836-OOP-2566-Lab-14/assets/144197034/e56b6e6f-e99c-4a02-8ac2-61cde16af6da)

5.Run project โดยการใช้คำสั่ง

```cmd
dotnet run --project Lab14_Ex09
```

6.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 5
![image](https://github.com/AnchisaPhetnoi/03376836-OOP-2566-Lab-14/assets/144197034/9e021497-3e9b-41fe-b4fc-443cead299ee)

7.อธิบายสิ่งที่พบในการทดลอง

โค้ดสร้าง Queue ชื่อ planets เก็บชื่อดาวเคราะห์
โค้ดใช้ Enqueue เพิ่มชื่อดาวเคราะห์ 9 ดวง (พุธ ถึง พลูโต)
โค้ดใช้ foreach แสดงชื่อดาวเคราะห์ทั้งหมด
โค้ดใช้ Dequeue ลบชื่อดาวเคราะห์ดวงแรกออก
โค้ดใช้ foreach แสดงชื่อดาวเคราะห์ที่เหลือ 
เป็นการจัดเก็บและจัดการองค์ประกอบในลักษณะเข้าก่อนออกก่อน (FIFO) โดยจะแสดงการเพิ่มองค์ประกอบ การลบองค์ประกอบแรกออก และวนซ้ำองค์ประกอบที่เหลือ
