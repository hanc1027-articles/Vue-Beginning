[Vue 官方網站](https://cn.vuejs.org/v2/guide/#)

### Vue.js 是什麼？
- 它是JavaScript的一個框架，可以讓我們快速的開發專案，且他具有動態資料處理的特色，  
    也無需像原生的JavaScript需透過呼叫DOM元素才可取得元件的值。

### 第一步先佈置好電腦的環境
1. 因為會使用到git，所以先下載、安裝git的comman line  
    [載點](https://git-scm.com/downloads)
2. 因接下來會使用到*npm指令*(Node Package Manager)，來安裝及管理我們所有Vue的專案，需先下載、安裝Node.js的套件。  
    [Node.js載點](https://nodejs.org/en/)(下載10.15.3 LTS版本即可) 
3. 安裝完畢後，打開其應用程式(GIT Bash)：  
    (1) [Vue CLI 官網](https://cli.vuejs.org/zh/)
    在GIT GUI輸入以下指令，安裝Vue-CLI的套件(@vue/cli 3.x 版本)：
    ```bash
    npm install -g @vue/cli
    ``` 
    補充：-g 是指全域安裝  
    (2) 因GIT Bash預設開啟位置在 ```C:\Users\[你的User Name]```，所以先切換到桌面的位置：
    ```bash
    cd Desktop
    ``` 
    (3) 接著，開始創建一個Hello-Word專案，  
    運行以下命令來創建一个新專案：
    ```bash
    vue create hello-world
    ```  
    它會問你一些是否在專案中要安裝的其他dependencies(相依套件)，因為我們現在是先練習，所以按enter，直接進入預設即可。  
    完成後，會看到他推荐你的兩行指令：  
    ```bash
    cd hello-word #此為切換到專案的目錄下
    npm run serve #此命令會編譯專案，讓它在本機跑伺服器，大多在 http://localhost:8080/ 的網址下可以看到自己專案跑的情況
    ```
    不過我們現在要換成用Visual Studio Code來開啟專案編輯。  

### 使用 VS code 編輯專案
1. GIT Bash中，在同一資料夾下(C:\Users\\ [你的User Name] \Desktop)，輸入：
    ```bash
    code hello-word #使用Visual Studio 打開整個專案資料夾
    ```
    打開後，應該會呈這個狀態  
    ![hello-word專案在vs code](01.png)  

2. 了解專案架構：  
    (1) node_modules:各dependencies存放的資料夾，每當我們在GIT Bash下執行 ```npm install [dependencies 的名字]```時，npm就會把我們安裝的依賴存放在這個資料夾，而此資料夾是不必存入git的追蹤的，因為它的總檔案大小太大。  
    (2) public:我自己目前是很少用到他，所以可以參考官網資料。 [public 官網參考](https://cli.vuejs.org/zh/guide/build-targets.html#应用)  
    (3) src: 開發最重要的資料夾，大部分的元件，網頁的編輯檔都在這個資料夾操作。  
    底下包含了：  
        1、 assets:放置生成的静態資源 (js、css、img、fonts)
        2、 components:放置元件。網頁上所看到的任何都是一個個元件所組成的，例如一個Navbar、Container、Footer，他們都是元件，而元件就像積木，讓我們可以堆疊在一個網頁上，做出我們想要的效果。
        3、 App.vue:在此專案中，是網頁的主頁，以路由來講："/"，就是根目錄。
        4、 main.js:掛載router(路由)、store的檔案