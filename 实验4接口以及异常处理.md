#实验  接口以及异常处理


实验目的：
1.掌握抽象类、抽象方法的定义
2.掌握Java中接口的定义，掌握接口的定义形式以及接口的实现方法
3.掌握异常的使用方法、并在程序中根据输入情况做异常处理

实验要求：
1.编写上述实体类和测试类
2.在 博士研究生类中实现各个接口定义的抽象方法
3.对年学费和年收入进行统计，求得纳税额
4.根据输入情况做异常处理

核心代码：

public abstract class DRStudent implements Student, Teacher {
	private String name;                                              //姓名
	private String sex;                                              //性别
	private int age;                                                //年龄
	private String zhuanye;                                        //专业
	private String banji;                                         //班级
	private float xuefeiOfTerm;                                  //每学期学费
	private float xinshuiOfMonth;                               //每月薪水
	private float money = 0;                                   //剩余金额

	public DRStudent(String name, String sex, int age,String zhuanye,String banji, float xuefeiOfTerm, float xinshuiOfMonth) {
		this.name = name;
		this.sex = sex;
		this.age = age;
		this.zhuanye = zhuanye;
		this.banji =banji;
		this.xuefeiOfTerm = xuefeiOfTerm;
		this.xinshuiOfMonth = xinshuiOfMonth;
	}

  public String toString() {										//获得学生信息
      return "学生信息 {" + "\n" +
              "姓名='" + name + '\'' + "\n" +
              "性别='" + sex + '\'' + "\n" +
              "年龄=" + age + " 岁\n" +
              "专业='" + zhuanye + '\'' + "\n" +
              "班级='" + banji + '\'' + "\n" +
              "学费=" + xuefeiOfTerm + " 元/学期\n" +
              "工资=" + xinshuiOfMonth+ " 元/月\n" +
              "余额=" + money + " 元\n" +
              '}';
  }
	
	public void statistics() {
		float tax = Zhujiao.getTax(getMoney());
		System.out.println("信息统计：\n学生：" + getName() + "\n" + 
		"每学期学费：" +getXuefeiOfTerm() + "\n" + 
		"每学年学费："+ xuefeiOfYear() +"\n"+
		"每月薪水：" + getxinshuiOfMonth() + "\n" + 
		"每年薪水：" + xuefeiOfYear() + "\n"+ 
		"税前年收入：" + getMoney() + "\n" + 
		"需交税：" + tax + "\n" +
		"税后年收入：" + (money - tax));
	}



实验心得：
1.逐渐熟练掌握Java的设计编程
2.能够熟练实例化对象
3.获得满满的成就感
4.学习过 C语言、Python 后，学到了新的一门编程语言
