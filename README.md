#### scenario with double execution of maven build while using `build-image` goal

Execute `mvn clean package`.

Output (after spring-boot plugin starts it restarts the whole build cycle):
```
...
[INFO] >>> spring-boot-maven-plugin:2.4.5:build-image (default) > package @ spring-boot-build-image-double-build >>>
[INFO] 
[INFO] --- maven-resources-plugin:2.6:resources (default-resources) @ spring-boot-build-image-double-build ---
[WARNING] Using platform encoding (UTF-8 actually) to copy filtered resources, i.e. build is platform dependent!
[INFO] Copying 0 resource
[INFO] 
[INFO] --- maven-compiler-plugin:3.1:compile (default-compile) @ spring-boot-build-image-double-build ---
[INFO] Nothing to compile - all classes are up to date
...
```
