---
layout: extra
title: Code 
parent: Writing
nav_exclude: true
nav_order: 7
---
Code Example	
{: .label }

# Ethereum Tipping 

```html 
<a href="#"  id="eth_tip_button" onclick="onEthTipButtonClick();">
// The text on the button 👇
ETHER TIP
</a>
```
```html
<script type="text/javascript">
```

```js
// Replace 0x36eb9A0F170E99350693e09Fa1f3E894C334451A with your Ethereum address 👇
var ETH_ADDRESS = '0x36eb9A0F170E99350693e09Fa1f3E894C334451A';	

// Set the donation amount in Ether 👇
// In this case 0.01 ETH = around $1.35
var ETH_VALUE = '0.01';

// This is the default gas price - feel free to adjust it if the default changes in the future 👇
// Currently this is the standard				
var ETH_DEFAULT_GAS_PRICE = 21000000000;

// Create a confirmation message 👇
var ETH_SUCCESS_MESSAGE = 'Thank you for your donation of 0.01 ETH! 🙌';	

// Creat an error message 👇
var ETH_ERROR_MESSAGE = 'Oh no! 🤦‍♂️ Something went wrong!';	

// set a message to show when MetaMask is not available. 👇
var ETH_WEB3_UNAVAILABLE_MESSAGE = 'Your web3 wallet is unavailable.' 
To donate, please feel free to send Ether to 0x36eb9A0F170E99350693e09Fa1f3E894C334451A - Thank you!';'

</script>
```

```css
<style>
#eth_tip_button {
	position: relative;
	display: inline-block;
	padding: 0.2em 0.4em;
	border-radius: 3px;
	font-weight: 500;
	text-decoration: none;
	color: #ffffff;
	background: #00a968;
}
</style>
```

```html
<script src="https://cdn.jsdelivr.net/gh/ethereum/web3.js@0.20.6/dist/web3.min.js"></script>
<script type="text/javascript">
```

```js
function onEthTipButtonClick() {
	var isWeb3Available = false;
	if (typeof web3 !== 'undefined') {
		web3 = new Web3(web3.currentProvider);
		isWeb3Available = true;
	}
	if (isWeb3Available && web3.eth.defaultAccount) {
		sendEther();
	} else {
		alert(ETH_WEB3_UNAVAILABLE_MESSAGE);
	}	
};
function sendEther() {
	var weiValue = web3.toWei(ETH_VALUE, 'ether');
	var transactionObj = {
		to: ETH_ADDRESS,
		value: weiValue,
		gasPrice: ETH_DEFAULT_GAS_PRICE
	};
	web3.eth.sendTransaction(transactionObj, function(error, txHash) {
		if (error) {
			alert(ETH_ERROR_MESSAGE);
		} else {
			alert(ETH_SUCCESS_MESSAGE);
		}
	});
}
```

```html
</script>
```