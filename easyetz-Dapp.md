# install dependencies
npm install

npm start
# build for production with minification
npm run build

make web3 instance 
import Web3 from 'web3'
let  provider = new Web3.providers.HttpProvider('http://etzrpc.org:80')
let web3 = new Web3(provider)
Vue.prototype.$web3 = web3

easyetz dapp interface:
1,easyetz.getAddress() //return address 
2，easyetz.etzTransaction(jsons)   //send transaction to your contract
let datas = contractInstance.methods.methodName().encodeABI(); 
//contractInstance is the instance of web3，
//methodName is the name of contract method
let jsons = {"contractAddress": contractAddress,"etzValue": etzValue,"datas":datas,"keyTime":keyTime,"gasLimit":gasLimit,"gasPrice":gasPrice};
//contractAddress is your contract address  
//etzValue is then number of you sending forexample you will send 0.1etz  params is  etzValue =0.1*10**18
//keyTime is something your make number to waiting easyetz send successful return params
jsons = JSON.stringify(jsons); //you must transfer string type

when your transaction is successful ,easyetz will get your public method name "makeSaveData(hash,keyTime)"  you can get hash of this transaction to and keyTime you are sent;

check device android or ios
let flat = navigator.userAgent.match(/(phone|pad|pod|iPhone|iPod|ios|iPad|Android|Mobile|BlackBerry|IEMobile|MQQBrowser|JUC|Fennec|wOSBrowser|BrowserNG|WebOS|Symbian|Windows Phone)/i);

finnally
please download easyetz ,and choose "Discover" and look for last click "development"  now you can test your dapp ,or submit dapp to Official


