## 主要内容 NTT挖矿教程


### 1. 获取钱包前期准备

如果没有NAS地址请先获得NAS钱包地址，存储好地址json文件和密码！！！ NAS钱包官网项目（chrome插件）
https://github.com/nebulasio/WebExtensionWallet

NTT地址和NAS地址一样
星图NTT钱包地址https://nasticker.com/#

在钱包中存储至少25个NTT和0.01NAS之后，可以挖矿。

### 2. 克隆项目

首先安装node
```
 brew install node
 ```
然后安装npm
```
npm i
 ```
安装依赖nebulas
 ```
 npm install nebulas
 ```

 克隆项目 https://github.com/dabdevelop/NASTickerToolKit
 项目克隆到本地后

 在<font color=#FF0000 >项目文件夹</font>里新建accounts文件夹
  ```
  mkdir accounts
   ```
 将注册钱包时的keystore文件 钱包名.json文件（n1…….json）放入accounts 文件夹。
 然后在文件夹中新建accounts.json文件，
 里面写入

 ["n1¥¥¥¥¥¥¥¥¥¥¥¥","将password改为自己钱包的密码，保存main"]

 里面的第一个元素 n1¥¥¥¥¥¥¥¥¥¥¥¥ 为自己的NAS地址（ n1……）
第二个元素为 密码 

 cd进入项目文件夹，最后在终端运行
  ```
 node main.js
 ```
 若出现字样：

 n1Mpxne8aiiyK5NQcakpDDNmTdQDZh53xKk call n1sr4JA4e9QPB4opLk2Kjmp8NkP6GGoAmnt @ sellPrice: [0.1] with value: 0 time: 2018/7/7 上午11:26:04
 n1Mpxne8aiiyK5NQcakpDDNmTdQDZh53xKk call n1sr4JA4e9QPB4opLk2Kjmp8NkP6GGoAmnt @ sellPrice: [0.1] with value: 0 time: 2018/7/7 上午11:26:04
 
 
 表示开始挖矿
****
 有可能的问题：

 1.Error: Cannot find module './accounts/accounts.json'
 accounts.json 
 
 文件没存储好

 2，Error: Cannot find module './accounts/n1…….json'
 钱包.json 
 
 文件没存储好

 3，Error: Cannot find module 'nebulas'
 
 安装 npm install nebulas

 4，Error: Key derivation failed - possibly wrong passphrase
 main.js 
 
 第23行的密码没改过来，或者密码记错了

## 挖矿 docker 版本

#### 方法1 直接使用打包好的docker image

可以部署到任何支持docker的服务器。

``` 
docker pull yuxizhe/nastickertoolkit
``` 

运行时设置环境变量  

> KEY : 账号json信息

> PASSWORD : 账号密码


#### 方法2 自己打包使用

修改 Dockerfile 中的变量
KEY 和 PASSWORD 。 格式见文件中的例子
