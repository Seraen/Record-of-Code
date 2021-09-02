`描述

有一个员工表employees简况如下: 

![img](https://uploadfiles.nowcoder.com/images/20210204/557336_1612425668678/6D9FFF5B1FDE1BF0E1E9D1396D67CA49)

有一个部门表departments表简况如下: 

![img](https://uploadfiles.nowcoder.com/images/20210204/557336_1612425711152/C24CBBDE019ABEEEB1835C750CAAC219)

有一个，部门员工关系表dept_emp简况如下: 

![img](https://uploadfiles.nowcoder.com/images/20210204/557336_1612426050115/3F560B6ECCA07CE59A293F9B6391D9A5)

请你查找所有员工的last_name和first_name以及对应的dept_name，也包括暂时没有分配部门的员工，以上例子输出如下:

![img](https://uploadfiles.nowcoder.com/images/20210204/557336_1612426091801/F02CEDCA7F2DA40C99E3BB9B269AF5CA)`

解：

`SELECT last_name,first_name,dept_name
FROM dept_emp as a
JOIN departments as b on a.dept_no=b.dept_no
right JOIN employees as c on c.emp_no=a.emp_no`

两度的join