# MagicSophy-NFT-mint-dapp
Installation 🛠️
If you are cloning the project then run this first, otherwise you can download the source code on the release page and skip this step.

git clone https://github.com/HashLips/hashlips_nft_minting_dapp.git
Make sure you have node.js installed so you can use npm, then run:

npm install
Usage ℹ️
In order to make use of this dapp, all you need to do is change the configurations to point to your smart contract as well as update the images and theme file.

For the most part all the changes will be in the public folder.

To link up your existing smart contract, go to the public/config/config.json file and update the following fields to fit your smart contract, network and marketplace details. The cost field should be in wei.

Note: this dapp is designed to work with the intended NFT smart contract, that only takes one parameter in the mint function "mintAmount". But you can change that in the App.js file if you need to use a smart contract that takes 2 params.

{
  "CONTRACT_ADDRESS": "0x827acb09a2dc20e39c9aad7f7190d9bc53534192",
  "SCAN_LINK": "https://polygonscan.com/token/0x827acb09a2dc20e39c9aad7f7190d9bc53534192",
  "NETWORK": {
    "NAME": "Polygon",
    "SYMBOL": "Matic",
    "ID": 137
  },
  "NFT_NAME": "Nerdy Coder Clones",
  "SYMBOL": "NCC",
  "MAX_SUPPLY": 1000,
  "WEI_COST": 75000000000000000,
  "DISPLAY_COST": 0.075,
  "GAS_LIMIT": 285000,
  "MARKETPLACE": "OpenSea",
  "MARKETPLACE_LINK": "https://opensea.io/collection/nerdy-coder-clones",
  "SHOW_BACKGROUND": true
}
Make sure you copy the contract ABI from remix and paste it in the public/config/abi.json file. (follow the youtube video if you struggle with this part).

Now you will need to create and change 2 images and a gif in the public/config/images folder, bg.png, example.gif and logo.png.

Next change the theme colors to your liking in the public/config/theme.css file.

:root {
  --primary: #ebc908;
  --primary-text: #1a1a1a;
  --secondary: #ff1dec;
  --secondary-text: #ffffff;
  --accent: #ffffff;
  --accent-text: #000000;
}
Now you will need to create and change the public/favicon.ico, public/logo192.png, and public/logo512.png to your brand images.

Remember to update the title and description the public/index.html file

<title>Nerdy Coder Clones</title>
<meta name="description" content="Mint your Nerdy Coder Clone NFT" />
Also remember to update the short_name and name fields in the public/manifest.json file

{
  "short_name": "NCC",
  "name": "Coder Clone NFT"
}
After all the changes you can run.

npm run start
Or create the build if you are ready to deploy.

npm run build
Now you can host the contents of the build folder on a server.

That's it! you're done.
