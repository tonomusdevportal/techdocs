This is VC4Trust Enablement.

After cloning the code from above link , run the following - 

### Running Wallet Application on local

Move to the below directory after cloning the repo
```
1. cd tel-veramo-wallet/wallet
```
Install dependencies 
```
2. npm install
```

Before starting the wallet application
Install Expo Go on your mobile device
From the root of the wallet application repo, run 
open ~/src/constants/url.js
update your network url as - 

``` 
3. export const ip = `<your ip address>`;
```

To start the Wallet application, run the following command from console

```
4. npx expo start
```


The console will display a QR code.
On iOS, you can scan the QR code with the camera app. This will launch Expo Go. On Android, you can launch Expo Go and scan the QR code from within Expo Go.
Once you've scanned the code once, you can launch Expo Go and the app will be listed in the "Recently Opened" list.

IN the console display, you can see the wallet application will be running on port 19000, stating - 
```
Metro waiting on exp://<your local ip address> 
```
For sequence flow of the wallet, you can refer to the following link 
https://neom.atlassian.net/wiki/spaces/TEL/pages/1218969648/User+Registration+and+Wallet+initialization
