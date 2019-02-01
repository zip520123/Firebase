## Firebase Cloud Functions 基本安裝步驟 
[reference](https://firebase.google.com/docs/functions/)
***
## 安裝
* vscode
* nodejs
***
1. 建立一個資料夾後
```bash
npm init
npm install -g firebase-tools
firebase login
```
2. 先到firebase 創一個專案，之後
```bash
firebase init functions
```
* 要裝其他功能也可以直接
```bash
firebase init
```
3. 選擇剛剛新建的專案
4. 選javascript
5. ESLint yes
6. Do you want to install dependencies with npm now? Yes
7. 之後出現一個functions的資料夾裡面有一個index.js裡面就可以寫後台程式
8. 之後發佈
```bash
firebase deploy --only functions
```
9. 此時去Firebase 網站主控台就可以看到剛剛發佈的api

***
## Firebase hosting 靜態網站
1. public 資料夾裡面index.html寫好就直接發佈
```bash
firebase deploy --only hosting
```
2. 之後會回傳網站就可以看到剛剛發佈的網站
* 設定txt之後要過一段時間才有用，firebase產生憑證要24小時
![route53](/img/route53.png)
![hosting](/img/hosting.png)
* https://firebase.google.com/docs/hosting/custom-domain
* https://www.youtube.com/watch?v=Bcn5e57PpUc

***
## 本地端測試 Run dynamic content locally

1.
```bash
npm install --save firebase-functions@latest
```
2.
```bash
firebase serve
```
https://firebase.google.com/docs/hosting/functions