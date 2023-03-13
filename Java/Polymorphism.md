java Polymorphism
</br>
```java
// [다형성]
// 1. 하나의 객체가 여러가지 형태를 가질수있는 성질
// 2. 한 타입의 참조변수로 여러타입의 객체를 참조할 수 있도록 하는것
// 3. 상위 클래스 타입의 참조변수로 하위 클래스의 객체를 참조할 수 있도록 허용한 것


//[문제 1]
// Friend 클래스를 상속받는 2개의 클래스 BoyFriend, GirlFriend 를 정의하고
// friendInfo() 메서드를 오버라이딩해라
class Friend {
    public void friendInfo() {
        System.out.println("나는 당신의 친구입니다.");
    }
}

class BoyFriend extends Friend {
    public void friendInfo() {
        System.out.println("나는 당신의 남자친구입니다.");
    }
}

class GirlFriend extends Friend {
    public void friendInfo() {
        System.out.println("나는 당신이 여자친구입니다.");
    }
}

// [문제 2]
// 2-1.Friend 데이터타입의 참조변수(객체_ friend에 생성하고, 이에 Friend() 생성자를 할당해라.
// 2-2. BoyFriend 데이터타입의 참조변수 boyfriend를 생성하고 이에 BoyFriend() 생성자를 할당해라.
// 2-3. Friemd 데이터타입의 참조변수 girlfriend를 생성하고 이에 GirlFriedn() 생성자를 할당해라.
public class Polymorphism {
    public static void main(String[] args) {
        Friend friend = new Friend();
        BoyFriend boyfriend = new BoyFriend();
        Friend girlfriend = new GirlFriend(); // 상위클래스를 참조변수 타입으로 지정했기떄문에
                                              // 참조변수가 사용할수있는 멤버의 개수는 상위클래스 멤버수가됨.

        friend.friendInfo();
        boyfriend.friendInfo();
        girlfriend.friendInfo();
        //girlfriend.friend.friendInfo(); <- 이렇게는 안됨!

    }
}


```
