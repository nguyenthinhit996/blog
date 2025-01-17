---
layout: post
title: Giới thiệu Java
subtitle: Overview, Syntax, Control Statament,...
gh-repo: daattali/beautiful-jekyll
gh-badge: [star, fork, follow]
tags: [java]
comments: true
author: Peter
---

Giới thiệu xung quang Java, Syntax, Key word,  
Exception Handling in Java, JDK, JVM, Data Type, Operator.  
If Else, Switch, For, While, Continue, Break. Các bài tập luyện tập.

# Nội dung
- [Overview Java](#giới-thiệu-java)
- [Lịch Sử](#lịch-sử)
- [Tính năng](#tính-năng)
- [Chi tiết Run](#chi-tiết-run)
- [Download Java và set path](#download-java-và-set-path)
- [JDK, JRE và JVM](#jdk-jre-và-jvm)
- [Biến](#variable)
- [DataType](#datatype)
- [Operator](#operator)
- [Trạng thái xử lí](#trạng-thái-xử-lí)
  - [if-else](#if-else)
  - [switch](#switch)
  - [for](#for)
  - [while](#while)
  - [do-while](#do-while)
  - [break](#break)
  - [continue](#continue)
- [Comment](#Comment)    
- [Keyword](#keyword)  
- [Quy ước đặc tên](#quy-ước)  
- [Lời kết](#lời-kết)  

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
  
  ![java-security.png](https://raw.githubusercontent.com/nguyenthinhit996/blog/master/assets/img/java-security.png)
  
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

![javacodecompile.png](https://raw.githubusercontent.com/nguyenthinhit996/blog/master/assets/img/javacodecompile.png)

khi đã có file.class thì ra run file.class vậy lúc run time sẽ theo flow bên dưới:  

![java-runtime-processing.png](https://raw.githubusercontent.com/nguyenthinhit996/blog/master/assets/img/java-runtime-processing.png)

ClassLoader: là 1 tiến trình con của JRE.
ByteCode Verifier: Kiểm tra đoan code có hợp lệ để tránh truy cập bất hợp pháp đối tượng 
Interpreted: Read bytecode stream sau đó thực thi diễn giải code.  

## Download Java và set path

link: https://jdk.java.net/java-se-ri/18

Có 2 loại set: 
- tạm thời:
   > **cmd: set path=C:\Program Files\Java\jdk1.6.0_23\bin**
- lâu dài set enviroment:  
  search "environment variables"  
  
  ![evn01.PNG](https://raw.githubusercontent.com/nguyenthinhit996/blog/master/assets/img/evn01.PNG)  
  Thêm dòng JAVA_HOME  
  
  ![evn02.PNG](https://raw.githubusercontent.com/nguyenthinhit996/blog/master/assets/img/evn02.PNG)  
  
  Thêm vào path    

  ![evn03.PNG](https://raw.githubusercontent.com/nguyenthinhit996/blog/master/assets/img/evn03.PNG)   
  ![evn04.PNG](https://raw.githubusercontent.com/nguyenthinhit996/blog/master/assets/img/evn04.PNG)  

## JDK, JRE và JVM

- JDK, JRE and JVM là platform phụ thuộc vào OS, mỗi OS khác nhau sẽ có sự configuaration khác
nhau, nhưng Java là 1 platform độc lập. có thể run mọi OS, miễn sau ở đó có JVM đã cài đặt.
- JVM viết tắt của Java Virtual Machine là máy 1 máy ảo, được gọi là máy ảo vì nó không tồn tại vật lí.
JVM cung cấp runtime enviroment mà nơi đó thực thi bytecode. Ở đó cũng thực thi được 
  các chương trình được viết từ những ngôn ngữ khác được complier thành java bytecode.
- JRE viết tắt của Java Runtime Environment là bộ công cụ phần mêm được sử dụng bở dev java.
JRE bao ngồm JVM và 1 số thư viện bên trong đó ví dụ: rt.jar.
- JDK viết tắt của Java Development Kit. JDK bao ngồm JRE và thêm 1 số tools như javac, java, ...  

![jdk.png](https://raw.githubusercontent.com/nguyenthinhit996/blog/master/assets/img/jdk.png)
  
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

![java-data-types.png](https://raw.githubusercontent.com/nguyenthinhit996/blog/master/assets/img/java-data-types.png)

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

- **Unary toán tử 1 ngôi**  
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
  

- **Tính toán(Arithmetic) * / + - %**   
  
  ```java 

    valueA = 10;
    valueB = 10;

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
  
  
    
- **Shift <<, >>, >>>**    
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
     // get Binary signed 2's complement of -10 = 1111111111110110
     // push đủ 32 bit : 1111111111111111111111111110110
     // dịch 1 bit sang phải: 1111111111111111111111111111011 = 2147483643
  ```  
    
- **Relational comparison: < > <= >= instanceof,  equality: == !=**  
  
  ```java
    class InstanceClass {}
    String str = "str";
    InstanceClass object = null;
    InstanceClass object2 = new InstanceClass();
    System.out.println(str instanceof String); // always return true
    System.out.println(object instanceof InstanceClass); // always return false
    System.out.println(object2 instanceof InstanceClass); // return true
  ```
    
- **Bitwise & ^ |**     
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
    
- **Logical && ||**     
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
    
- **Assignment** = += -= *= /= %= &= ^= |= <<= >>= >>>= 
  Các phép tính như sau **value ? = xx**   <=>  **value = value ? xxx**    
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

## Trạng thái xử lí

  Java thực thi code từ trên xuống dưới. Trạng thái code được thực thi theo thứ tự xuất hiện của chúng
Tuy nhiên java cung cấp những trạng thái được sử dụng để điều kiển trình tự của java code. Nó là 
một trong những tính năng cơ bản của java.  
  Cung cấp 3 trạng thái của code: 
  - Trang thái quyết định: If else , switch.
  - Trạng thái loop: for, while, do while, for-each.
  - Trạng thái nhảy: continue, break.  
Chúng ta sẽ đi tìm hiểu từng mảng của trạng thái.
    
### if-else
Trong trạng thái quyết định ta có if , if else, if else-if, if lòng if. ta có trạng thái đầu tiên

#### if
  
  ```java
    if(condition) {
        //some code
    }
  ```
  Ta có sơ đồ:  

  ![if.PNG](https://raw.githubusercontent.com/nguyenthinhit996/blog/master/assets/img/if.PNG)

#### if else
  
  ```java
    if(condition) {
        //some code
    }else {
        // some code
    }
  ```
  Ta có sơ đồ:  

  ![if-else.PNG](https://raw.githubusercontent.com/nguyenthinhit996/blog/master/assets/img/if-else.PNG)


#### if else-if else

  ```java
    if (condition) {
        //some code
    } else if (condition 2){
        // some code
    } else if (condition 3){
        // some code
    }
    //...
    } else {
        // some code
    }
  ```
  Ta có sơ đồ:
  
  ![if-else-if-else.PNG](https://raw.githubusercontent.com/nguyenthinhit996/blog/master/assets/img/if-else-if-else.PNG)

#### if lòng if

  ```java
    if (condition) {
        if (condition 2) {
            //some code
        }
    }
  ```
  Ta có sơ đồ:
  
  ![if-if.PNG](https://raw.githubusercontent.com/nguyenthinhit996/blog/master/assets/img/if-if.PNG)


### switch

Switch sẽ thực thi trạng thái giống như if else bậc thang.  
Giá trị của switch có thể mang là cái kiểu primitive, và những kiểu wapper như 
Integer, Boolean,.. enum và string.  
Giá trị của case phải là trực tiếp không được phép là 1 biến.  
Giá trị của case phải là duy nhất nếu trùng giá complier sẽ lỗi.  
Mỗi case có thể break hoặc không, nêu không có break nó sẽ thự thực thi next case.  
Case default có thể có hoặc không. 


  ```java
    switch(condition) {
      case value1 : 
        somecode ;
        somecode ;
      break ;
      case value2 : somecode ; break ;
      case value3 : somecode ; break ;
      default : systax;
    }

  ```
![switch](https://raw.githubusercontent.com/nguyenthinhit996/blog/master/assets/img/switch.png)

Trường hợp chúng ta không sử dụng  break cho switch

  ```java
    int value = 20;
    switch(value) {
      case 10 : 
        somecode1 ;
        somecode2 ;
      case 20 : somecode3 ;
      case 30 : somecode4 ;
      default : somecode-default;
    }
      
    vì sẽ thực thi tất cả statment sau khi match đầu tiên khi không có break. match ở đây là 20 sẽ thưc thi match 20 và những statement sau nó là 30 và default.

  ```


### for

Cách sử dụng for, khi ta xác định được số vòng lặp cố định.  
Khi sử dung for ta phải khởi tạo giá trị bạn đâu cho nó.   

for(khởi tạo giá trị ; điều kiện loop; giá trị tăng hoặc giảm) {}  
for(;;) loop vô tận ;  

  ```java
    for(int i=0; i< 10; i++){
      //some code here
    }

  ```

![for](https://raw.githubusercontent.com/nguyenthinhit996/blog/master/assets/img/for.png)

#### for each 

Dùng cho loop array hoặc list . 

  ```java
    List<Integer> list = new ArrayList<Integer>();
    for(Integer element: list){
      //some code here
    }

    List<Integer> list ;
    for(Integer element: list){
      //some code here
    }

    List<int> list = new ArrayList<int>(); // error unexpected type. should use object.
    int[] arr = new int[] {1,2,3,4}; // array ok.
    for(Integer element: list){
      //some code here
    }

  ```

**Chú ý** biến list không được null, nếu null sẽ throw **exception nullpointer**.  
các element có thể được phép null.  Nếu biến list chưa được khởi tạo case sẽ xuất hiện lỗi stop app
**error: variable a might not have been initialized**


### while

Sử dụng cho việc lập đi lặp lại nếu trạng thái là true. phù hợp cho việc không biết được sẽ loop bao nhiêu lần. 

  ```java

    while(condition){
      // update condition 
      //some code here
    }

  ```

Nếu conditon là true sẽ thực hiện loop, có thể kết hợp với break. 

  ```java
      int a=0;
      while(a<10){
            a++;
            if(a == 5){
                break;
            }
        }

  ```

Nếu condition luôn luôn true thì while sẽ loop vô tận while(true){} .

![while](https://raw.githubusercontent.com/nguyenthinhit996/blog/master/assets/img/while.png)


### do-while

Cũng giống như while sẽ loop khi gặp điều kiện true. nhưng ở đây sẽ thưc thi ít nhất 1 lần cho dù điều kiện ban đầu là true hay false. 

  ```java

      do{    
      //code to be executed / loop body  
      //update statement   
      }while (condition);  

  ```
  ```java

      do{    
      //update statement   
      }while (true);  //loop vô tận

      do{    
      //update statement   
      }while (false);  //thưc thi 1 lần duy nhất

  ```

### break

break được sử dụng để thoát vòng lặp hoặc switch , while, do while. Nhưng chú ý ở đây break sẽ thoát
trạn thái gần nhất, trong trường hợp inner loop thì break sẽ có giá trị trên loop gần break nhất. 

  ```java

      do{    
        for(Integer i : list) {
          break; // chỉ có tác dụng thoát khỏi for chứ không thoát khỏi do while được vì break sẽ 
          // có thoat vòng lặp gần nó nhất.
        }
      }while (true);

  ```

### continue

Được sử dụng trong cấu trúc loop như for hoặc while, do while. Dùng để nhảy đến trạng thái tiếp theo mà không thực thi những dòng code dưới lệnh continue.  
Cũng giống như break thì continue sẽ có giá trị với loop gần nó nhất trong trường hợp inner nhiều loop. 

  ```java

      do{    
        for(Integer i : list) {
            //some code 
            if(condition true){
              continue; // nhảy đến i tiếp theo của for, không thực thi code bên dưới câu lệnh này. 
            }
            // some code 
        }
      }while (true);

  ```

## Comment

Comment chú thích trong java sẽ không được complier và interperter. Dùng để gải thích code 
clean code ...  

 ```java

      comment 1 dòng trong java 
       // single comment 


        comment multi line java
       /*
         this is comment multi-line
         List<Integer> l1 = new ArrayList<Integer>();
         System.out.println(l1);
       */


        comment doc java
       /**... */
       //comment doc:  information for the class, method, constructor, fields etc.

       /**
        * created time: 2022-12-12
        * author: thinh.
       */
       class a {} ;

  ```


## Keyword

- **abstract**: là keyword để khởi tao một class trừu tượng. 1 class trừu tượng không thể
có instance mà phải chỉ lớp implement class trừu tương mới có thể tạo instance. abstract có thể khởi tạo 1 
  method với method không có body và được override bởi class implements.
- **boolean**: là 1 datatype primitive được khởi tạo 1 variable. có thể mang giá trị true hoặc false, mặc định lúc
khởi tạo là false.
- **break**: break được sử dụng thoát khỏi vòng lặp hoặc while gần nhất. Và sử dụng trong switch. những code phía dưới break không được thực thi.
- **byte**: là 1 data type primitive được sử dụng để khởi tạo variable và mang giá trị
  từ min: -128 max: 127.
- **case**: được sử dụng cùng với switch. 
- **catch**: catch được sử dụng để bắt 1 exception. được sử dụng với cú pháp try - catch - catch -.. finally .
- **char**: là 1 data type primitive, được dùng để khai báo variable và được dùng để lưu kí tự, nếu lưu 1 number thì number đó sẽ parse sang Unicode table
[bảng chuyển đổi](https://en.wikipedia.org/wiki/List_of_Unicode_characters).
- **class**: dùng để khởi tạo 1 class.
- **continue**: dùng để tiếp tục loop hoặc while. Nó sẽ tiếp tục loop vòng lặp mới, và 
bỏ các câu lệnh phía sau continue.
- **default**: được sử dụng trong switch, nếu không thoãi các case thì default sẽ được thực thưc thi.
- **do**: sử dụng kết hợp với while, do while(điều kiện) sẽ được thực thi ít nhất 1 lần. nếu thoãi điều kiện sẽ loop.
- **double**: là 1 primitive data type, dùng để khai báo 1 variable lưu trữ 64 bit với 
chữ số thập phân lên đến 15 chữ số sau dấu phẩy.
- **else**: else là 1 nhánh thây thế của if. hoặc else if.
- **enum**: enum dùng để khai báo 1 list cứng. Hàm khởi tạo của enum luôn luôn private
hoặc default. Thường sử dụng kết hợp với switch statement.
- **extends**: là keyword chỉ định ràng 1 class con đang kế thừa 1 class cha. hoặc 1 
interface đang kế thừa 1 interface khác.
- **final**: là keyword được ứng dụng cho class, method, variable. nếu ứng dụng vào class, thì class đó sẽ không
được kế thừa, nếu ứng dụng vào method, thì method đó sẽ không được override, nhưng lưu ý có thể sử dụng lại nhưng không được override.
Còn final ứng dung cho field thì field đó không đươc thay đổi sau khi khởi tạo. 
Chú ý nếu khởi tạo final với List thì ta không được update địa chỉ list đó nhưng vẫn có thể 
  add, remove các element của list đó. 
- **finally**: được sử dụng chung với try catch finally hoặc try finally, là trang thái luôn luôn được thực thi
mặc dù vào try hay catch. Thường dùng để close connection, clean up dữ liệu. 
Thường thì sẽ thực thi sau try, nếu return có trong try thì sẽ thực thi finally trước khi return, còn đối với catch, thực thi sau catch nếu handle đúng exception, và trước nếu ko đúng exception.
- **float**: là 1 primitive data type, được khởi tạo 1 variable mang 32 bit, và với number có 
khoảng 6 or 7 chữ số đăng sau dấu phẩy. 
- **for**: Sử dụng cho loop statement,với cố định số vòng lặp.  
- **if**: Sử dụng với điều kiện, nếu điều kiện true thì sẽ vào thực thi if.
- **implements**: được dùng để 1 class kế thừa 1 interface, lưu ý rằng:   
  1 class sẽ có thể implements nhiều interface nhưng chỉ extends 1 class duy nhất.   
  1 interface chỉ có thể sử dụng keyword extend và có thể extend nhiều interface khác.
- **instanceOf**: được sử dụng để kiểm tra xem liệu 1 object có phải là 1 instance của 1
class hoặc interface không.
- **interface**: Là keyword để khởi tạo 1 interface và mặc định các method của interface là 
1 method trừu tưởng không có body mặc định và public.  
  Từ java 8 interface có thêm default và static method.  
  Từ java 9 có thêm private method.
- **long**: là 1 primitive data type sử dụng để khai báo variable với lưu trữ 64 bit number sô nguyên.
- **new**: được sử dụng để new 1 object
- **null**: chỉ định rằng object không chỉ định bất kì giá trị nào.
- **package**: được sử dụng chỉ định class hiện tại đang ở trong package nào. được khai báo bên trong 1 file java.
- **private**: là key word để khai báo phạm vi truy cập của 1 variable, method, inner class.
không cho phép sử dụng giá trị từ phía ngoài class. Nếu ngoài class chỉ sử dụng get hoặc set để truy cập và điều chỉnh. Chứ 
  không được sử dụng trực tiếp instance.variable .
- **protected**: là keyword chỉ định phạm vi truy cập của 1 variable, method, contructor, inner class.
Cho phép truy cập thông qua phương thức kế thừa.
- **public**: là keyword chỉ định phạm vi truy cập của variable, method, constructor, class.
cho phép truy cập ở bất kì đâu cho dù cùng package hay khác. Nếu không chỉ định phạm vi truy cập của 
  class, variable, method,.. thì sẽ hiểu là các đối tượng cùng package sẽ có thể 
  truy cập được.
- **return**: được sử dụng để thoát method, và trả về giá trị và không chấp nhận return trong void method. Type của return phải 
cùng 1 kiểu với kiểu trả về khai báo ở method.
- **short**: là 1 kiểu data type của primitive, được khai báo variable có thể lưu trữ 16 bit number số nguyên.
- **static**: là keyword ứng dụng cho variable class, method class, block, nested class.
mục tiêu chính của static là việc tiết kiệm bộ nhớ.
- **strictfp**: Java strictfp keyword đẻ đảo bảo tính linh động trong việc tính toán
liên qua đế số thập phân (floating-point). để đảo bảo rằng chúng ta sẽ có cùng kết
 nếu run ở trên nhiều platform khác nhau. Từ đó giúp chúng ta quan lí tốt hơn về 
  tính toàn số thập phân. Có thể ứng dụng cho class, method, interface.
- **super**: là keyword dùng để reference đến class cha. có thể call trực tiếp variable, method của class cha.
có thể sử dụng như sau: super.variable, super.method(), super() ý là call contructor class cha.
- **switch**: kết hợp với case để quyết định case nào dược thực thi. nếu thoãi điều kiện.
- **synchronized**: dùng để xử lí đồng bộ trong chương trình có multiThread. Ứng dụng cho method, block code.
- **this**: là keyword chỉ định đến object hiện tại trong method hoặc contructor.
- **throw**: chỉ định chính xác 1 exception được ném ra. Thường được sử dụng cho việc
customize 1 exception cho 1 bussiness. Sử dụng Throw new ACBException();
- **throws**: thông báo thông tin exception của method hoặc class có thể xảy ra.
Thường sử dụng class A throws ABCException {}. Nếu exception là loại runtime (Nullpointer, Numberformat)
  thì việc sử dung throws là option có cũng được không chỉ định trên method,class cũng được, 
  còn đối với exception complier (IOexception) thì bắt buộc phải có throws. 
- **transient**: được sử dụng trong serialization. Nếu bạn định nghĩa bất kì properties nào 
là transient thì nó sẽ không được serialization.
- **try**: được sử dụng để đảm bảo code được thực thi nếu có bất kì exception nào sảy ra 
ta có thể chủ động catch và xử lí exception. nếu không sử dung try catch thì chương trình 
  sẽ dừng nếu gặp exception.
- **void**: được khai báo với method chỉ định rằng method này không trả về bất kì gía trị nào. 
- **volatile**: Chỉ định rằng variable có thể thay đổi trong asynchonized. Đảm bảo rằng
variable luôn được cập nhật gía trị mới nhất từ các thread đang sử dụng variable đó.
- **while**: sử dung cho việc loop với không xác định số vòng loop. phù hợp cho việc 
loop theo điều kiện nếu true thì sẽ vào trong block while. nếu false stop loop.


## Quy Ước

Có 1 số số quy ước chung về cách đặt tên trong java. Các quy ước này được cộng đồng java cũng như là 
sun Microsystems and Netscape. Đây không phải luật lệ nếu bạn vào project nào có nhưng quy định khác 
thì bãn cũng chấp nhận thôi vì có thể project bạn có quy định riêng thì ta theo thôi. 

**Package** luôn là chữ in thường. Và là danh từ. Ví du: controller, domain, company. 

**Class** Bắt đầu bằng chứ in hoa và in thường hết, nếu có trên 1 từ thì bắt đầu bằng in hoa luôn. Và nó là danh từ hoặc cụm danh từ.  Ví dụ : HocSinh, Ban, Xe. 

**Interface** Giống như class cũng đặt in hoa chữ bắt đầu. Ví dụ: TaiKhoan, NganHang.

**Method** bắt đầu bằng chữ in thường và các chữ sau in hoa và chúng ta sử dụng động từ cho nó. 
Ví dụ. rutTieng(), saoKeLuongHangThang().

**Variable** bắt đầu bằng chữ in thường, và các chữ sau in hoa. Và sẽ đặt tên theo danh từ tương ứng. 
ví dụ: listHocSinh. pigs.

**Constant** Hằng số không thay đổi được sau khi thay đổi.  Các đặt tên là luôn in hoa từ và cách nhau bởi dấu 
_ (underscore) đặt tên giống như variable. Ví dụ: MIN_VALUE, NUMBER_ACCOUNT


## Lời kết

Bàì viết tham khảo các page sau: 
- [javatpoint](https://www.javatpoint.com/java-tutorial)
- [w3schools](https://www.w3schools.com/java/)

Xin cảm ơn. Peter