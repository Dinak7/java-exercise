---

title: java习题
date: 2020-10-17 14:27:45
tags: 习题 
categories: java

---

# 作业习题

ide: eclipse

## 基础

第一次写笔记，很开心，附上我最喜欢的桌面壁纸:blush:

![](C:\Users\Dina\Desktop\QQ图片20201011142225.jpg)

第二章p41页4.5.9

4.编程求出一个一维int型数组的元素最大值、最小值、平均值和所有元素之和。
5.编程实现 float型数组的冒泡排序。(要求用Scanner和for each） 
9.编程实现从键盘依次输入姓名（字符串）、年龄（整型）性别（字符）和成绩（浮点
型），然后依次显示上述内容。（要求用scanner、布尔型变量）

4.

```java
package text1;
public class shuzu {
    public static void main(String[] args) {
		// TODO Auto-generated method stub
		int []a= {3,7,1,5,8};
		int i,max=0,min=0;int sum=0;
		int aver=0;
		for(i=0;i<a.length;i++)
		{   
            sum=sum+a[i];
			max=a[0];min=a[0];
			if(a[i]>max)
			    max=a[i];
			if(a[i]<min)
				min=a[i];
		}
		aver=sum/a.length;
        System.out.println("最大值为:"+max+"最小值为："+min+"求和为："+sum+"平均值为："+aver);	
  }
}

```

5.

```java
package text1;
import java.util.*;
public class paixu {

	private static String v;
    public static void main(String[] args) {
		// TODO Auto-generated method stub
      float []a;
      a=new float[4];
      int i,j;
      float m;
    Scanner sc=new Scanner(System.in);
    System.out.println("请输入float型数组：");
    for(i=0;i<a.length;i++)
      {	  
        a[i]=sc.nextFloat();
      }
    sc.close();
    for(i=0;i<a.length;i++)
    {
        for(j=0;j<a.length-1;j++)
    	 { 
            if(a[j]>a[j+1])
    		  { 
                  m=a[j];
    	          a[j]=a[j+1];
    	          a[j+1]=m;
    		  } 
    	 }
    }
      System.out.println("冒泡排序输出为：");
      for (float v:a)
      System.out.print(v+" ");
 }
}

```

9.

```java
package text1;
import java.util.*;
public class shuru {
    public static void main(String[] args) {
		// TODO Auto-generated method stub
	     System.out.println("请输入姓名、年龄、性别、成绩：");
	     //姓名字符串，年龄整型，性别字符，成绩浮点型
	     Scanner sc=new Scanner(System.in);
	     String name=sc.nextLine();
	     int age=sc.nextInt(); 
	     sc.nextLine();//整型要回车
	     String sex=sc.nextLine();
	     float score;
	     score=sc.nextFloat();
	     sc.close();
	     System.out.println("姓名年龄性别成绩分别为:"+name+"  "+age+"  "+sex+"  "+score);
   }
}
```

