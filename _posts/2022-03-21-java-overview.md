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
Interpreted: Read bytecode stream sau đó thưcj thi diễn giải code.  

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