---
title: "Using in Out Ref With Parameters"
date: 2020-02-05T17:08:11+09:00
draft: true
---

# The in, ref, and out Modifiers

* ref는 메서드에 의해 수정될 수 있음을 명시하는데 사용된다.

* in은 메서드에 의해 수정될 수 없음을 명시하는데 사용된다.

* out은 메서드에 의해 수정될 것 있음을 명시하는데 사용된다.

## out 한정자
### out 한정자를 사용하면 새 인스턴스를 할당하여 메서드 외부에서 반영할 수 있다.
```
class ReferenceTypeExample
{
  static void Enroll(ref Student student)
  {
    // With ref, all three lines below alter the student variable outside the method.
    student.Enrolled = true;
    student = new Student();
    student.Enrolled = false;
  }

  static void Main()
  {
    var student = new Student
    {
      Name = "Susan",
      Enrolled = false
    };

    Enroll(ref student);

    // student.Name is now null since a value was not passed when declaring new Student() in the Enroll method
    // student.Enrolled is now false due to the ref modifier
  }
}

public class Student {
  public string Name {get;set;}
  public bool Enrolled {get;set;}
}
```