# OOP Comparison: Java, C++, and Python

เปรียบเทียบความเหมือนและความแตกต่างในการเขียนโปรแกรมแบบ OOP ด้วยภาษา Java, C++, Python

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

### 1. **การประกาศคลาส (Class Declaration)**
การประกาศคลาสเป็นหัวใจหลักของ OOP ซึ่งทำหน้าที่กำหนดโครงสร้างของวัตถุ (object) และพฤติกรรม (method)

#### Java
```java
class Animal {
    String name;
    int age;
    
    void speak() {
        System.out.println("This is an animal.");
    }
}
```
#### C++
```cpp
class Animal {
public:
    std::string name;
    int age;

    void speak() {
        std::cout << "This is an animal." << std::endl;
    }
};
```
#### Python
```python
class Animal:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def speak(self):
        print("This is an animal.")
```

### 2. **การสร้างออบเจ็กต์ (Object Creation)**
การสร้างออบเจ็กต์ทำให้สามารถใช้งานคลาสที่ประกาศไว้ได้

#### Java
```java
Animal animal = new Animal();
animal.name = "Buddy";
animal.age = 5;
animal.speak();
```
#### C++
```cpp
Animal animal;
animal.name = "Buddy";
animal.age = 5;
animal.speak();
```
#### Python
```python
animal = Animal("Buddy", 5)
animal.speak()
```

### 3. **การห่อหุ้ม (Encapsulation)**
การห่อหุ้มคือการปกป้องข้อมูลของคลาสจากการเข้าถึงโดยตรงจากภายนอก โดยการใช้ตัวกำหนดการเข้าถึง (access modifier)

#### Java
```java
class Animal {
    private String name;
    private int age;

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }
}
```
#### C++
```cpp
class Animal {
private:
    std::string name;
    int age;

public:
    void setName(std::string name) {
        this->name = name;
    }

    std::string getName() {
        return name;
    }
};
```
#### Python
```python
class Animal:
    def __init__(self, name, age):
        self._name = name  # ใช้ underscore (_) แทนการใช้ private
        self._age = age

    def get_name(self):
        return self._name

    def set_name(self, name):
        self._name = name
```

### 4. **การสืบทอด (Inheritance)**
การสืบทอดคือการสร้างคลาสใหม่ที่มีคุณสมบัติของคลาสเดิม

#### Java
```java
class Dog extends Animal {
    void speak() {
        System.out.println("Bark!");
    }
}
```
#### C++
```cpp
class Dog : public Animal {
public:
    void speak() override {
        std::cout << "Bark!" << std::endl;
    }
};
```
#### Python
```python
class Dog(Animal):
    def speak(self):
        print("Bark!")
```

#### 5. **การจัดการข้อยกเว้น (Exception Handling)**
ทุกภาษามีโครงสร้างที่คล้ายกันในการจัดการข้อยกเว้น (exception) เพื่อป้องกันการทำงานที่ไม่ถูกต้อง

#### Java
```java
try {
    int result = 10 / 0;
} catch (ArithmeticException e) {
    System.out.println("Cannot divide by zero.");
}
```
#### C++
```cpp
try {
    int result = 10 / 0;
} catch (const std::exception& e) {
    std::cerr << "Error: " << e.what() << std::endl;
}
```
#### Python
```python
try:
    result = 10 / 0
except ZeroDivisionError as e:
    print("Cannot divide by zero:", e)
```
