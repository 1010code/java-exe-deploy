# Java exe deploy
### 使用 javac 編譯並執行
在 `main.java` 檔案目錄下執行以下指令來編譯 `.java` 檔案。

```
#編譯
javac -encoding UTF-8 main.java
```

輸入以下執行指令執行程式。

```
#執行
java main
```

![](https://i.imgur.com/lrPyQ5K.png)



### 使用包裝檔 jar 執行
包裝jar檔時需要建立一個 `MANIFEST.MF` 檔案。記得要多留最後一行，不然執行時可能會有問題。

```
# MANIFEST.MF
Main-Class: main

```

輸入以下指令編譯jar檔。

```
jar -cvfm main.jar  MANIFEST.MF ./
```
編譯完成後會在目錄資料夾底下看到一個`main.jar`，輸入以下指令即可執行程式。
```
java -jar main.jar
```
![](https://i.imgur.com/fPNck65.png)



### 使用 Launch4j 將 jar 包成 exe 檔
這裡使用`launch4j`第三方軟體來編譯jar檔並產生出exe的Java執行檔。首先指定`Output File`的資料夾與檔名(記得要打.exe)，接著放入要轉成exe的jar程式。

![](https://i.imgur.com/TtMBMvA.png)

接著輸入`Min JRE version` 可支援的最低版本。

![](https://i.imgur.com/1ct5eQE.png)

最後再設定exe的執行方式。因為我沒有寫GUI介面所以就點選console(終端機)的執行方式。設定在`Header`選項內。

![](https://i.imgur.com/ZinQFyG.png)

最後在點選上排工具列的齒輪會先儲存一個 xml 設定檔，這也方便稍後修改設定重新產生 exe 檔，不用重新做設定。接著目錄資料夾底下就會產生出一個exe執行檔囉。

![](https://i.imgur.com/CnlAtCv.png)
