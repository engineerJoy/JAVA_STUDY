# JAVA_STUDY
hello world!
运算符
a++先引用后自增
++a先自增后引用
example：
          int a=1,b;
          b=a++;
          System.out.println(a);
          System.out.println(b);
结果：2
      1
example：
          int a=1,b;
          b=++a;
          System.out.println(a);
          System.out.println(b);
 结果：2
      2
      
复合赋值运算：内含强转，右部看作一个整体

强制类型转换：向高看齐
不强转不一定不出问题，强转不一定出问题（损失数据）
相同类型：高存储向低存储有事
         低存储向高存储有事
不同类型：高精度向低精度有事
         低精度向高精度有事
         
 比较运算和逻辑运算的运算结果都是布尔型的 
 
 逻辑运算符-短路问题
 &&与运算符：前面条件不成立后面的就不看了
 int a=2,b=3;
 boolean bl=a>4&&++b<3;
 System.out.println(b);
 此时b=3
 &与运算符：前面条件不成立后面的仍然要看
 int a=2,b=3;
 boolean bl=a>4&++b<3;
 System.out.println(b);
 此时b=4
 ||或运算符：前面条件成立后面的就不看了
 int a=2,b=3;
 boolean bl=a<4||++b<3;
 System.out.println(b);
 此时b=3
 |或运算符：前面条件成立后面的仍然要看
 int a=2,b=3;
 boolean bl=a<4|++b<3;
 System.out.println(b);
 此时b=4
 
 数组被当作对象：他有自己的属性length
 数组被声明 int[] array;（建议）或是int array[];
 int[][] array;
 数组被分配空间：被分配空间后默认存储数值0
 int[] array=new int[5];
 int[][] array=new int[2][3];此时array.length=2(二维数组被看作是几个一维数组合并，此时length代表有几个一维数组合并,想要查第一维的length时用array[0].length)
 
 数组下标其实是指偏移量（与指针指向的偏移量（指针指向array[0]））
 
 不规则二维数组：被认为的两个一维数组长度不同是可以存在的
 int[][] array=new int[2][];
 ...
 
 输入密码直到正确用do while
  //输入密码直到正确
          int password=123456;int number=3;
          int input;
          do{
               Scanner sc=new Scanner(System.in);
               System.out.println("请输入密码：");
               input=sc.nextInt();
               number--;
          }while(input!=password&number!=0);
          if(number!=0)
          System.out.println("登录成功");
          else
          System.out.println("错误次数太多，已经冻结您的账号😀");
 
 
 
