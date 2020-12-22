# ConfigPrivatePod私有库脚本

iOS组件化私有库发版脚本

### 使用方法

1. git拉下来后和要发布的私有pod放在同一个目录下;
2. 把**templates**和**templates_objc**文件夹下的Podfile中`source 'git@github.com:daichuan/DCPrivatePod.git'`改成你自己的私有Pod源仓库的repo地址;
3. 把**templates**和**templates_objc**文件夹下的**upload.sh**中`DCPrivatePod`改成你自己的私有Pod源仓库的名字；
4. cd到**ConfigPrivatePod**，执行**config.sh**（OC执行**config_objc.sh**）脚本来配置这个私有Pod。脚本会问你要一些信息，`Project Name`就是工程名，要跟你的工程的目录名一致。`HTTPS Repo`、`SSH Repo`网页上都有，`Home Page URL`就填工程 Repo网页的URL就好了。
5. 上一步之后你的工程文件夹里会多出一些文件。如果这个工程要发版，直接cd到工程目录下，执行**upload.sh**就可以了。这个脚本会自动对pod版本+1，如果要配置，在发布前可以去podspec文件里配置；

