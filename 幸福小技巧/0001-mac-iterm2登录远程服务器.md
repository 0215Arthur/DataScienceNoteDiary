# iterm2登录远程服务器

1. 写个脚本login.sh

   ```shell
   #!/usr/bin/expect
   
   set user <your name>
   set host <your host>
   set password <your password>
   set port <your port>
   
   spawn ssh -p $port $user@$host
   expect "*password:*"
   send "$password\r"
   interact
   expect eof
   ```

2. iterm2新建profile，使用expect执行login.sh

   ![新建profile](img/0001-1.png)

3. 点击菜单栏profile，点击dev，登录，美滋滋

   