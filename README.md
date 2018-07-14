# 1. 递归阶乘  
## 解题思路
 
 1. 首先判断用户输入的参数是否为空，若为空则输出usage
 2. 若有参数则调用递归函数factorial()
 3. 当参数不为1时,继续调用factorial()函数向下递归
 4. 参数为1时,将参数与s相乘,并将s返回上一层
 5. 最后将递归阶乘的结果输出    

 ## 运行结果
 ![结果1](./picture/1.png)

 # 2. 自动根据后缀名解压文件
 ## 解题思路

 1. 通过条件判断对传入的参数做不同处理,若传参为空,则输出usage;传参为'--list',则输出该脚本支持的压缩文件格式;传参为文件压缩文件的路径,则调用self_compression()函数
 2. self_compression()函数先获取压缩文件的后缀名,并且根据解压目标路径是否为空选择解压路径为当前路径或用户所给路径
 3. 根据文件的后缀名,选择不同的解压命令对文件进行解压操作

 ## 运行结果
 ![结果2](./picture/2.png)

 # 3. 获取文件夹下最大的前n个文件
 ## 解题思路

 1. 首先用条件判断对传参情况进行区分,若传参格式不正确,则输出usage;若传参格式正确,则调用file_size()函数;若无传参,则以 10 和当前路径为参数传给file_size()函数
 2. file_size()函数通过du命令获取目标文件夹下各个文件的文件名和大小,并通过管道传递给sort命令进行排序,再通过重定向将sort命令的标准输出传入temp.txt文件
 3. 通过cat -n 命令对排序后的temp.txt文件内容进行排序,并重定向输出到temp1.txt文件中
 4. 根据传参n,利用head命令获取temp1.txt文件的前n行并输出
 5. 删除临时文件temp.txt和temp1.txt

 ## 运行结果
 ![结果3](./picture/1.png)