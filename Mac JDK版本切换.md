# Mac JDK 管理
> [https://stackoverflow.com/questions/21964709/how-to-set-or-change-the-default-java-jdk-version-on-os-x](https://stackoverflow.com/questions/21964709/how-to-set-or-change-the-default-java-jdk-version-on-os-x)
> [https://adoptopenjdk.net/](https://adoptopenjdk.net/)


## 查看版本列表
```bash
/usr/libexec/java_home -V
```

```
Matching Java Virtual Machines (2):
    14.0.2, x86_64:	"AdoptOpenJDK 14"	/Library/Java/JavaVirtualMachines/adoptopenjdk-14.jdk/Contents/Home
    1.8.0_265, x86_64:	"AdoptOpenJDK 8"	/Library/Java/JavaVirtualMachines/adoptopenjdk-8.jdk/Contents/Home

/Library/Java/JavaVirtualMachines/adoptopenjdk-14.jdk/Contents/Home
```
## 设置版本
```bash
# 设置为jdk8
export JAVA_HOME=`/usr/libexec/java_home -v 1.8`

# 设置为jdk14
export JAVA_HOME=`/usr/libexec/java_home -v 14.0`
```

## 修改环境变量
```bash
vim ~/.zshrc
export JAVA_HOME=$(/usr/libexec/java_home -v 1.8)

source ~/.zshrc
echo $JAVA_HOME
java -version
```
