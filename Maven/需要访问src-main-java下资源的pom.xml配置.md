控制中心报错找不到指定的文件，但是文件存在于代码目录（src\main\java）中，需在工程目录下pom.xml中增加如下配置即可
```xml
<project>
    <build>
        <resources>
            <resource>
                <!--目录路径，一般指定到java目录-->
                <directory>src/main/java</directory>
                <!--
                    包含的文件，这里直接代表java目录及其子目录下，
                    所有以.xml结尾的文件
                -->
                <includes>
                    <include>**/*.xml</include>
                </includes>
            </resource>
        </resources>
    </build>

</project>

```
