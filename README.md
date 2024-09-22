# OOP Comparison: Java, C++, and Python

# OOP Comparison Table: Java, C++, and Python

| **Features**           | **Java**                                              | **C++**                                               | **Python**                                             |
|------------------------|-------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|
| **Class Declaration**   | `class ClassName { ... }`                             | `class ClassName { ... }`                             | `class ClassName: ...`                                 |
| **Object Creation**     | `ClassName obj = new ClassName();`                    | `ClassName obj;`                                      | `obj = ClassName()`                                    |
| **Encapsulation**       | `private`, `protected`, `public`                      | `private`, `protected`, `public`, `friend`            | `_name` (Private by convention, not enforced)          |
| **Inheritance**         | `class SubClass extends SuperClass { ... }`           | `class SubClass : public SuperClass { ... }`           | `class SubClass(SuperClass): ...`                      |
| **Multiple Inheritance**| Not supported (via interfaces only)                   | Supported                                             | Supported                                              |
| **Polymorphism**        | Method Overriding (`@Override` annotation)            | Virtual functions (with `virtual` and `override`)      | Method Overriding                                      |
| **Memory Management**   | Automatic Garbage Collection                         | Manual (using `new` and `delete`)                     | Automatic Garbage Collection                           |
| **Access Modifiers**    | `private`, `protected`, `public`                      | `private`, `protected`, `public`                      | No strict access control, uses `_` and `__` (name mangling) |
| **Constructor Syntax**  | `ClassName(args) { ... }`                             | `ClassName(args) : member(args) { ... }`              | `def __init__(self, args): ...`                        |
| **Destructor Syntax**   | Not explicitly needed (garbage collection)            | `~ClassName() { ... }`                                | `def __del__(self): ...` (rarely used, garbage collected) |
| **Exception Handling**  | `try { ... } catch(Exception e) { ... }`              | `try { ... } catch(Exception& e) { ... }`             | `try: ... except Exception as e: ...`                 |

---

## Explanation of Key Features

1. **Class Declaration**: ทั้ง 3 ภาษาใช้คำสั่ง `class` ในการประกาศคลาส แต่รูปแบบการเขียนจะต่างกันเล็กน้อย
2. **Object Creation**: การสร้างออบเจ็กต์ใน C++ ไม่ต้องใช้ `new` เหมือนใน Java และ Python
3. **Encapsulation**: Java และ C++ ใช้คำสั่งที่คล้ายกันเพื่อควบคุมการเข้าถึงข้อมูล แต่ Python ใช้หลักการแบบ convention โดยใช้ `_` แทนการใช้คำสั่งอย่างเป็นทางการ
4. **Inheritance**: ทุกภาษาสามารถสืบทอดคลาสได้ แต่ Java ไม่รองรับ Multiple Inheritance แบบตรงๆ (ต้องใช้ Interface)
5. **Memory Management**: Java และ Python มีระบบ garbage collection ในขณะที่ C++ ต้องจัดการหน่วยความจำเอง
6. **Exception Handling**: การจัดการข้อผิดพลาดคล้ายกันในทั้งสามภาษา แต่มีความแตกต่างในรูปแบบการเขียน
