
安装 ndk/26.1.10909125
安装 jdk 17
安装 android sdk 34
安装 cmake

 ~/.gradle/gradle.properties 添加
``` 
org.gradle.caching=true
org.gradle.parallel=true
org.gradle.jvmargs=-Xmx2048m -Dfile.encoding=UTF-8 -XX:+UseParallelGC
android.native.buildOutput=verbose
```

安装 libxposed api
```
git clone https://github.com/libxposed/api.git
cd api
git checkout 100
./gradlew publishToMavenLocal
```

安装 libxposed service
```
git clone https://github.com/libxposed/service.git
cd service
git checkout 100
./gradlew publishToMavenLocal
```


生成全部文件
```
./gradlew zipall
```

生成面具文件
./gradlew flashMagiskAndRebootZygiskRelease

生成ksu文件
./gradlew flashKsuAndRebootZygiskRelease