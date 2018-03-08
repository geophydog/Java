:hotel: [Return to Home JAVA Page] (https://github.com/geophydog/Java/blob/master/README.md)

***

### :one: compile JAVA classes in Windows CMD
- #### 1.1
```
javac -d class_path java_src_path
```
```
-d 为编译好的class文件存放之处
```

- #### 1.2
```
javac -cp libxx.jar xxx.java
```
```
当编译xxx.java文件需要另外的库时， -cp libxx.jar即为所需之库
```

***

### :two: run JAVA classes in Windows CMD
- #### 2.1
```
java -cp libxx.jar class_name
```
```
当运行需要另外的库时，-cp libxx.jar即为所需之库
```

- #### 2.2
```
java -cp classes package_name
```
