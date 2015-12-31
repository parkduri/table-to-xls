#Table To Xls
## Preview
![HTML Table](/doc/html.png)

Result

![XLS Result](/doc/xls.png)

## Usage

### Add Maven Dependency
```xml
    <dependency>
        <groupId>me.chyxion</groupId>
        <artifactId>table-to-xls</artifactId>
        <version>0.0.1-RELEASE</version>
    </dependency>
```

### Use In Code
```java
    StringBuilder html = new StringBuilder();
    Scanner s = new Scanner(getClass().getResourceAsStream("/sample.html"), "utf-8");
    while (s.hasNext()) {
        html.append(s.nextLine());
    }
    s.close();
    FileOutputStream fout = new FileOutputStream("target/data.xls");
    TableToXls.process(html, fout);
    fout.close();
```

## Contact

chyxion@163.com
