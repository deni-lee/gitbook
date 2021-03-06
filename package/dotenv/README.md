---
description: 將 .env 文件中的環境參數加載到 process.env
---

# dotenv

![](../../.gitbook/assets/env.JPG)

### 為什麼需要配置環境變數和模式呢？

所有方法肯定是來源於現實的需求。在一個產品的前端開發過程中，一般來說會經歷本地開發、測試指令碼、開發自測、測試環境、預上線環境，然後才能正式的釋出。對應每一個環境可能都會有所差異，比如說伺服器地址、介面地址、websorket地址…… 等等。在各個環境切換的時候，就需要不同的配置引數，所以就可以用環境變數和模式，來方便我們管理。

### 環境變數

vue cli-3.0總共提供了四種方式來制定環境變數：

在根目錄新增.env檔案，配置所有情況下都會用到的配置（不知道這個存在的意義，所有的都需要的也就不需要配置了吧）。 在根目錄新增.env.local 檔案，配置所有情況下都會用到的配置，與.env的區別是隻會在本地，該檔案不會被git跟蹤。 在根目錄新增.env.\[mode\] 檔案，配置對應某個模式下的配置,比如：.env.development來配置開發環境的配置。 在根目錄新增.env.\[mode\].local檔案，配置對應某個模式下的配置,與.env.\[mode\]的區別也只是會在本地生效，該檔案不會被git跟蹤。

### 使用dotenv管理环境变量

項目開發過程中，經常會涉及到類似數據库密碼、第三方服務密鑰等敏感信息。對于这些信息我們往往不会把它们直接寫到codebase里，通常的做法是將它们以還境變量的形式傳递，儘管這樣能很好的解决敏感信息泄露的問题，但當這類數據有了規模，團隊人元日益變多，修改Profile文件管理還境變量的方法就變得不那麼奏效了，

## 參考文獻

[https://github.com/motdotla/dotenv](https://github.com/motdotla/dotenv)

[https://www.itread01.com/content/1546930290.html](https://www.itread01.com/content/1546930290.html)

[http://lazybios.com/2016/11/how-to-use-dotenv-gem-manage-environment-variables-in-rails/](http://lazybios.com/2016/11/how-to-use-dotenv-gem-manage-environment-variables-in-rails/)

