### [다형성]
1. 하나의 객체가 여러가지 형태를 가질수있는 성질
2. 한 타입의 참조변수로 여러타입의 객체를 참조할 수 있도록 하는것
3. 상위 클래스 타입의 참조변수로 하위 클래스의 객체를 참조할 수 있도록 허용한 것
</br>

```java
//[문제 1]
// family 클래스를 상속받는 2개의 클래스 Mom, Dad 를 정의하고
// familyInfo() 메서드를 오버라이딩해라
class Family {
    public void familyInfo() {
        System.out.println("나는 당신의 가족입니다.");
    }
}

class Mom extends Family {
    public void familyInfo() {
        System.out.println("나는 당신의 엄마입니다.");
    }
}

class Dad extends Family {
    public void familyInfo() {
        System.out.println("나는 당신이 아빠입니다.");
    }
}

// [문제 2]
// 2-1.Family 데이터타입의 참조변수(객체) family에 생성하고, 이에 family() 생성자를 할당해라.
// 2-2. Mom 데이터타입의 참조변수 mom을 생성하고 이에 Mom() 생성자를 할당해라.
// 2-3. Family 데이터타입의 참조변수 dad를 생성하고 이에 Dad() 생성자를 할당해라.
public class Polymorphism {
    public static void main(String[] args) {
        Family family = new Family();
        Mom mom = new Mom();
        Dad dad = new Dad(); // 상위클래스를 참조변수 타입으로 지정했기떄문에
                                              // 참조변수가 사용할수있는 멤버의 개수는 상위클래스 멤버수가됨.

        family.familyInfo();
        mom.familyInfo();
        dad.familyInfo();
        //mom.family.familyInfo(); <- 이렇게는 안됨!

    }
}
```
