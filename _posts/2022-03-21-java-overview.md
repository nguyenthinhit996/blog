---
layout: post
title: Giới thiệu Java
subtitle: Overview, Syntax, Control Statament,...
gh-repo: daattali/beautiful-jekyll
gh-badge: [star, fork, follow]
tags: [structure-algorithm]
comments: true
author: Peter
---

Giới thiệu xung quang Java, Syntax, Key word,  
Exception Handling in Java, JDK, JVM, Data Type, Operator.  
If Else, Switch, For, While, Continue, Break. Các bài tập luyện tập.

# Nội dung
1. [Overview Java](#giới-thiệu-java)
2. [Lịch Sử](#lịch-sử)
3. [Tính năng](#tính-năng)
4. [Chi tiết Run](#chú-ý)
4. [Download Java và set path](#chú-ý)
4. [JDK, JRE và JVM](#chú-ý)
4. [DataType](#chú-ý)
4. [Operator](#chú-ý)
4. [Keyword](#chú-ý)


##  Giới thiệu Java

Java là một **ngôn ngữ lập trình** và là 1 **platform**. Java là ngôn ngữ bậc cao, 
cường tráng, hướng đối tượng (object-oriented) và ngôn ngữ ngữ an toàn.  
Java được phát triển bời Sun MicroSystems (hiện tại là công ty con của Oracle) vào năm 1995. 
James Gosling được biết là cha đẻ của java. Trước Java có tên là Oak, Từ khi mà Oak được đăng kí với tên 1 company,
thì James Gosling và team của ông ấy đã đổi tên thành Java.

**Platform** bất kì phần cứng hoặc phần mềm nào mà ở đó cho chương trình run đó được biết là 1 platform. 
Java có JRE java runtime enviroment và API, đó được call là platform.

Theo Sun, có 3 triệu thiết bị run Java. Có nhiều thiết bị run hiện tại run java, một trong chúng là : 
- Desktop Application such as arobat reader, media player, antivirus, etc,..
- Web application such as javatpoint.com, ...
- Enterprise Application such as banking applications.
- Mobile (Android)
- Embedded System
- Smart Card
- Robotics
- Game

**Platform / Editions**

- *Java SE (Standard Edition)*:  
Nó là một platform của java. Nó bao gồm java APIs such as java.lang, java.io, 
java.net, java.util, java.sql, java.math, etc. Nó bao gồm các core giống như
String, Regex, Exception, Inner Class, Multithreading, I/O Stream, Collection, etc.
- *Java EE (Enterprise Edition)*:  
Nó là một platform enterprise nó là phần chính cho việc phát triển web và ứng dụng enterprise. Nó được 
  xây dựng trên nền SE edition. Nó bao gồm các topic như Servlet, JSP, Web Services, JPA, etc...
- *Java ME (Java Micro Edition)*:  
Nó là một platform nhỏ được tích hợp vào các ứng dụng mobile.
- *Java FX*:    
Nó được sử dụng phát triển các ứng dụng trên internet. Giống như adobe Flash vậy
  
## Lịch Sử  
Hiện tại là java 18 ra mắt vào tháng 3, 2022 ,và phiên bản long term support hiện tại là java 17 ra mắt 
vào tháng 9 năm 2021.  
Kể từ java 8, Oracle relase version chẵn vào tháng 3 và version lẻ vào tháng 9 trong năm.


## Tính năng
Mục tiêu của chính của ngôn ngữ Java là đưa nó trờ nên tiện lợi (portable), đơn giản, và là 
một ngôn ngữ an toàn. Từ đó ta có vài tính năng tuyệt vờ như:
- Simple: Java thì rất dễ học, và cú pháp của nó đơn giản, clean, dễ hiểu. Theo Sun java
dễ hiểu bởi vì. Java đã remove những tính năng phức tạp ít sử dụng vd: con trỏ, ... Và chúng ta
  không cần remove garbage vì hệ thống tự động làm đều đó.
- Object oriented: mọi thứ trong java đều là một object. Hướng đối tượng có nghĩa là tổ chức
ứng dụng kêt hợp nhiều object khác nhau và mỗi object là sự kết hợp của hành vi và dữ liệu. 
  Ngôn ngữ hướng đối tượng là phương thức dễ phát triển và maintain tuân theo 1 số luật như sau: Object, Class, Kế thừa, đa hình, Abstract, đóng gói.
- Platform độc lập: gọi đó là đọc lập bởi vì java viết một lần run mọi nơi, nó không phụ thuộc vào phần cứng,
miễn ở đâu có JRE java runtime enviroment, có 2 loại platform là phần cứng và phần mềm, java hỗ trợ platform phần mềm
  là Runtime Enviroment và API (Application Programming Interface). Java code có thể thực thi trên nhiều platform giống như
  Windown, Linux, Sun Solaris, Mac, etc. Java code được biên dịch bởi complier và converted sáng byteCode. Chính 
  bytecode này là một platform độc lập bởi vì nó có thể run trên nhiều platfrom.
- Secured: Java được biết nhất cho việc an toàn. Với java chúng ta có thể phát triển hệ thống không 
viruss. Because các lí do sau: 
  - No use pointer 
  - Java program run bên trong a virtual machine sandbox.  
  [java-security.png]  
  - Clasloader: là một phần của JRE nó được sử dụng để load java classes vào trong JRE
  nó thể phần bảo vệ bằng các tách package các class ở local ra các resource được import từ network.
  - ByteCode verify: nó check các đoạn code hợp lệ ngăn chặn truy cập bất hợp pháp đến objects.
  - Security manager: Nó xác định những resource gì có thể truy cập như đọc viết vào local disk.
- Manh mẽ: 
  - Sử dụng tốt quản lí bộ nhớ.
  - Tráng được các vấn đề bảo mật của con trỏ.
  - Tự động thu thập garbage. tư động thu hồi bộ nhớ.
- Kiến trúc trung lập: java là một kiến trúc trung lập bởi vì nó không triển khai trên 
các tính năng phụ thuộc. vd như size của primitive được fix cứng: trong C int data type lưu 
  2 byte nếu tầng kiến trúc 32 but, lưu 4 byte nếu tần kiến trúc 64. Tuy nhiên Java lưu cứng 
  là 4 byte cho cả 2 tầng kiến trúc trên.
- Portable (ngọn nhẹ): nó tao điều kiện cho bạn the java bytecode đên any platform.
- High performace: Java thì nhanh hơn các ngôn ngữ diễn giải truyền thống, nhưng chậm 
hơn các ngôn ngư native code như C. but a little bit slower. Java là một ngôn ngữ 
  diễn giải (interperted) còn C là ngôn ngữ biên dịch (complied) nên java chậm hơn 1 tí.
- Distributed (phân phối): RMI và EJB được sử dụng để tạo các ứng dụng phân phối. Tính năng này của java làm cho chúng ta
có thể truy cập các files bằng cách gọi phương thức từ bất kì máy tính nào trên internet.
- Đa luồng: Một Thrad như là một chương trình riêng biệt, thực thi đồng thời. Chúng ta có thể viết một java
program bằng hiều task tại 1 thời điểm bằng định nghĩa multiple threads. Điểm sáng chính của 
  multi-thread là chúng không cấp bộ nhớ riêng cho mỗi thread, mà sử dụng share common memory.
  

## Chi tiết Run

Một ứng dụng java có 2 giai đoạn để thực thi đó là complier và runtime, 
vậy cách complier (không tác động đến OS) như thế nào nào hãy xem bên dưới.   
Complier file.java to file.class  
[javacodecompile.png]  
khi đã có file.class thì ra run file.class vậy lúc run time sẽ theo flow bên dưới: 
[java-runtime-processing.png]  
ClassLoader: là 1 tiến trình con của JRE.
ByteCode Verifier: Kiểm tra đoan code có hợp lệ để tránh truy cập bất hợp pháp đối tượng 
Interpreted: Read bytecode stream sau đó thực thi diễn giải code.  

## Download Java và set path

link: https://jdk.java.net/java-se-ri/18

Có 2 loại set: 
- tạm thời:
   >cmd: set path=C:\Program Files\Java\jdk1.6.0_23\bin
- lâu dài set enviroment:  
  search "environment variables"  
  [evn01.PNG]  
  Thêm dòng JAVA_HOME
  [evn02.PNG]  
  Thêm vào path  
  [evn03.PNG]   
  [evn04.PNG]  

## JDK, JRE và JVM

- JDK, JRE and JVM là platform phụ thuộc vào OS, mỗi OS khác nhau sẽ có sự configuaration khác
nhau, nhưng Java là 1 platform độc lập. có thể run mọi OS, miễn sau ở đó có JVM đã cài đặc.

- JVM viết tắt của Java Virtual Machine là máy 1 máy ảo, được gọi là máy ảo vì nó không tồn tại vật lí.
JVM cung cấp runtime enviroment mà nơi đó thực thi bytecode. Ở đó cũng thực thi được 
  các chương trình được viết từ những ngôn ngữ khác được complier thành java bytecode.
- JRE viết tắt của Java Runtime Environment là bộ công cụ phần mêm được sử dụng bở dev java.
JRE bao ngồm JVM và 1 số thư viện bên trong đó ví dụ: rt.jar.
- JDK viết tắt của Java Development Kit. JDK bao ngồm JRE và thêm 1 số tools như javac, java, ...
[jdk.png]
  
## Variable  
Variable là biến của java, sẽ giữ giá trị trong chương trình java lúc thực thi. Mỗi biến
được chỉ định bằng data type nó mang. Trong java có 3 loại biến local, instance, static.
- Local: biến được tạo trong body của method, bạn có thể chỉ sử dụng biến này trong method này , method khác không thể
thể truy cập. Một biến local không thể tạo với keyword **static**.
- Instance: biến được tạo ngoài method nhưng trong class. Biến Instance không được khởi tạo với keyword **static**.
Nó được gọi là biến Instance bởi bì giá trị của biến thuộc 1 Instance chỉ định và không chia sẽ giá trị này 
  giữa các instance.
- Static: biến static được tạo với từ khóa static. Nó không thể là biến local. Static biến có thể chia sẽ giá trị 
giữa các instance của class nhưng trong bộ nhớ chỉ tạo ra 1 lân và sử dụng nó mặc dù cho có bao nhiên instance đang 
  sử dụng nó.
  
```java 
public class ShareFullCode {

  Integer variableInstance = 10; //this is variable instance
  static Integer variableStatic = 10; // this is variable static
  
  void method () {
    Integer variableLocal = 10; // this is variable local
    //somecode...
  }
  
  public static void main (String [] args){
    ShareFullCode instance1 = new ShareFullCode(); //this is variable instance
    ShareFullCode instance2 = new ShareFullCode(); //this is variable instance
    ShareFullCode instance3 = new ShareFullCode(); //this is variable instance
     
    System.out.println(instance1.variableInstance); // variableInstance of instance instance1 
    System.out.println(instance2.variableInstance); // variableInstance of instance instance2 
    System.out.println(instance3.variableInstance); // variableInstance of instance instance3 
  
    System.out.println(instance1.variableStatic); // they use same variableStatic
    System.out.println(instance1.variableStatic); // they use same variableStatic
    System.out.println(instance1.variableStatic); // they use same variableStatic
  }
}
```

## DataType
Data type xác định sự khác nhau về khích thước và giá trị lưu trữ của biến. Có 2 kiểu của Data Type: 
- Primitive data type: Kiểu nguyên thủy như là *boolean, char, byte, short, int, float, double, long.*
Là những loại đã đựơc xây dựng sẵn trong java, có giá trị default khác null.
- Non Primitive data type: Kiểu không phải nguyên thủy như Classes, Interfaces, Array, String,...
[java-data-types.png]

Primitive Data Type:  

| Syntax      | Default Value | Default size |     Range          |
| ----------- | ------------- | ------------ | ------------------ |
| boolean     | false         | 1 bit        | true or false              |
| char        | '\u0000'      | 2 byte       | between '\u0000' (or 0) to '\uffff' (or 65,535 inclusive)              |
| byte        | 0             | 1 byte       | min: -128 max: 127              |
| short       | 0             | 2 byte       | min: -32,768 max: 32,767                  |
| int         | 0             | 4 byte       | min: -2,147,483,648 max: 2,147,483,647                  |
| long        | 0L            | 8 byte       | min: -9,223,372,036,854,775,808 max: 9,223,372,036,854,775,807                  |
| float       | 0.0f          | 4 byte       | min: 3.4e−038 max: 3.4e+038                  |
| double      | 0.0f          | 8 byte       | min: 1.7e−308 max: 1.7e+308                  |

**Chú ý**  
Đối với kiểu float và double:   
3.43-038 có nghĩa là 3.4 * 10 mũ -38  
3.43+038 có nghĩa là 3.4 * 10 mũ 38.   
Để sử dung kiểu float và double chúng ta nên nói đến độ chính xác (precision) là con số thập phân
sau dấu chấm, kiểu float thì có 6 hoặc 7 con số còn kiểu double thì khoản 15 chữ số sau dấu chấm.  
float : xxx.1234567  
double: xxx.123456789123456

Đối với kiểu Char: Java sử dụng Unicode System.

## Operator

- **Unary**: toán tử 1 ngôi  
  - Prefix: ++expr --expr +expr -expr ~(lật bit) !(cho boolean) : có hiệu ứng thực thi
  hiện tại
  - Postfix: expr++ expr--: sẽ được thực thi sau câu lênh hiện tại   
  
  ```java
    valueA = 10;
    valueB = 10;
    System.out.println(valueA ++); // 10 after that 11
    System.out.println(valueB --); // 10 after that 9
    System.out.println(valueA); //11
    System.out.println(valueB); //9
    
    //reset value
    System.out.println(++ valueA); // 11
    System.out.println(-- valueB); // 9
    System.out.println(valueA); //11
    System.out.println(valueB); //9
    
    //reset value
    System.out.println(+ valueA); // 10
    System.out.println(- valueB); // -10
    System.out.println(valueA); //10
    System.out.println(valueB); //10
    
    //reset value
     valueB = -10;
    System.out.println(~ valueA); // -11
    System.out.println(~ valueB); // 9
    System.out.println(valueA); //10
    System.out.println(valueB); //10
    ```  
    
  Giải thích ~ operator   
  Decimal number to Binary number:   
  10 => 0000000000001010   
  lật bit 0000000000001010 become 1111111111110101 = -11  
  -10 => 1111111111110110  
  lât bit 1111111111110110 become 0000000000001001 = 9  
  

- **Tính toán(Arithmetic)** * / + - %
  
  ```java 
     System.out.println(valueA * valueB); // 100
      //reset value
     System.out.println(valueA / valueB); // 1
      //reset value
     valueB = 7;
     System.out.println(valueA % valueB); // 3
      //reset value;
     System.out.println(valueA + valueB); // 20
      //reset value
     System.out.println(valueA - valueB); // 0
  ```
  
  sdfsad  
    
- **Shift** <<, >>, >>>  
  << = value * (2 mũ số shift)  
  ,>> = value / (2 mũ số shift)  
  ,>>> trường hợp value dương giống với >>  
  ,>>> trường hợp value âm dịch bit:
       get Binary signed 2's complement value thêm đủ 32 bit và sau đó dịch 1 bit
       nhớ là bit thêm vào đầu luôn là số 1
  
  ```java
     System.out.println(valueA >> 2); // 10 / (2^2) = 10 / 4 = 2
     System.out.println(valueA << 2); // 10 * (2^2) = 10 * 4 = 2
     System.out.println(-valueA >>> 1); // 2147483643
     // get get Binary signed 2's complement of -10 = 1111111111110110
     // push đủ 32 bit : 1111111111111111111111111110110
     // dịch 1 bit sang phải: 1111111111111111111111111111011 = 2147483643
  ```  
    
- **Relational**  comparison: < > <= >= instanceof,  equality: == !=
  
  ```java
    class InstanceClass {}
    String str = "str";
    InstanceClass object = null;
    InstanceClass object2 = new InstanceClass();
    System.out.println(str instanceof String); // always return true
    System.out.println(object instanceof InstanceClass); // always return false
    System.out.println(object2 instanceof InstanceClass); // return true
  ```
    
- **Bitwise** & ^ |  
  & : true & true => true , còn lại ra false  
  ^ : giống ra false , khác nhau ra true  
  | : có true thì tất cả ra true. 
  
  ```java 
    valueA = 9 ; // 1001
    valueB = 10; // 1010
    System.out.println(valueA & valueB); // 1000 = 8
    System.out.println(valueA ^ valueB); // 0011 = 3
    System.out.println(valueA | valueB); // 1011 = 11
  ```  
    
- **Logical** && ||  
  logical AND && : all true => true  
  logical OR || : only one condition true => true  
- **Ternary** ? :
  ```java
    if(condition == true) {
      return a;
    }else {
      return b;
    }
    
    tương đươn với 
    return condition == true ? a : b;
  ```  
    
- **Assignment** =  += -= *= /= %= &= ^= |= <<= >>= >>>=  
  Các phép tính như sau value ? = xx   <=>  value = value ? xxx  
  ? là Assignment
  ```java
   System.out.println(valueA %= 7); // valueA = valueA % 7 = 3
  ```  
    
- **Chú ý về operator**
  ```java
  // Operator && vs & : tất cả true thì sẽ true
     && gặp condition false thì sẽ stop ko check điều kiện phía sau 
     & check hết tất cả điều kiện cho dù gặp true hay false
  
  // Operator || vs | : only one true thì sẽ true
     || gặp condition true thì sẽ stop ko check điều kiện phía sau 
     | check hết tất cả điều kiện cho dù gặp true hay false
  
    void fun01 () {
       System.out.println("fun01");
       return true;
    }
    void fun02 () {
       System.out.println("fun02");
       return false;
    }
  
   if( fun02() && fun01() ) {  // gặp false thì dừng lại chỉ call fun02
        //ko vào được trong dây vì ko thoãi all true
    }
    
    if( fun02() & fun01() ) { // gặp false thì run tiếp call fun02 vs fun01
        //ko vào được trong dây vì ko thoãi all true
    }
  
    if( fun01() || fun02() ) {  // gặp true thì dừng lại chỉ call fun01
        //vào được trong dây vì thõa điều kiện, gặp true đầu tiên thì vô
    }
    
    if( fun01() | fun02() ) { // gặp true thì run tiếp call fun02 vs fun01
        //vào được trong dây vì thõa điều kiện, gặp true đầu tiên thì vô
    }
  ```
v5
## Keyword

1. abstract: là keyword để khởi tao một class h

```java
public class ShareFullCode {

  public static void main(String[] args) {
    float a = 123f;
    float b = 123.1234567f;
    float c = 123.12345678934567f;
    System.out.println(a); //123.0
    System.out.println(b); //123.12346
    System.out.println(c); //123.12346

    double aa = 123d;
    double bb = 123.1234567d;
    double cc = 123.12345678901234567890d;
    System.out.println(aa); //123.0
    System.out.println(bb); //123.1234567
    System.out.println(cc); //123.12345678901235
  }
}

```


```java
import java.util.Random;
import java.lang.Math;

public class ShareFullCode {

    // function
    static long sumPow2(int n) {

        if (n < 0 || n > 255) {
            return 0;
        }

        long sum = 0;

        for (int i = 1; i <= n; i++) {
            // round number value nearest
            sum = sum + Math.round(Math.pow(i,2));
        }

        return sum;
    }

    // Only for testing
    public static void main(String[] args) {
        Random random = new Random();
        int n = random.nextInt(255);
        System.out.println("N: " + n);
        long result = sumPow2(n);
        System.out.println("Total pow 2 of N:" + result);
    }
}
```
Để testing online bạn làm như sau: 
+ B1: Copy all code above.
+ B2: Open page [Test](https://www.tutorialspoint.com/compile_java_online.php){:target="_blank"} Jdk 1.8
+ B3: Xoá hêt code (toàn bộ class HelloWorld) có trong page. 
+ B4: Paste code vừa copy ở trên vào console của page. 
+ B5: Chọn Execute và show ra kết quả.



## Chú ý
+ Kiển tra đầu vào đúng là số nguyên dương 0 <= N <= 255


[Link Go back 1000 excercise](https://nguyenthinhit996.github.io/blog/2021-11-17-1000-exercise/)
  
Thanks.