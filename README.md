# fh402777388.github.io
鱼塘博客
//获取字节码文件对象
		//1:对象名.getClass()
		//2:类名.class属性
		//3:Class.forName("包名.类名")
		/*Student s=new Student();
		Class c1 = s.getClass();
		Class c2=Student.class;
		Class c3=Class.forName("cn.itheima.Student");
		System.out.println(c1==c2 && c2==c3);
		//构造方法
		Constructor[] ct = c3.getConstructors();
		for (Constructor c : ct) {
			System.out.println(c);
		}
		//有参构造
		Constructor c = c3.getConstructor(String.class,int.class,String.class);
		Object obj = c.newInstance("张三",20,"男");
		System.out.println(obj);*/
		Class c=Class.forName("cn.itheima.Student");
		Object obj = c.newInstance();
		Field f = c.getDeclaredField("name");
		System.out.println(f);
		f.setAccessible(true);
		f.set(obj, "李四");
		Object value = f.get(obj);
		System.out.println(value);
		/*Field[] fields = c.getDeclaredFields();
		for (Field field : fields) {
			System.out.println(field);
		}*/
		Method m=c.getMethod("getName");
		Object value1 = m.invoke(obj);
		System.out.println(value1);
