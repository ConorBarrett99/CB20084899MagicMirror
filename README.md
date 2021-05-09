# CB20084899MagicMirror
A student project for a magic mirror

-----------------------------------------

to run this mirror you will need:
1.Raspberry pi
2.CoinMarketCap Account
3.Monitor

-----------------------------------------

First step was to install the Magic Mirror you need to install the lastest Node.js . To do this go to the command terminal and type: 
curl -sL https://deb.nodesource.com/setup_14.x | sudo -E bash -
and then: 
sudo apt install -y nodejs

then you need to install the mirror:
git clone https://github.com/MichMich/MagicMirror

the enter the repository but typing:
cd MagicMirror/

then make a copy of the config sample file by typing:
cp config/config.js.sample config/config.js

now to can start the mirror by typing:
npm run start

You should be up and running now :)

---------------------------------------------------

to edit your configuration you need to edit the config.js file.
for my setup you will need to install two repositories:
1. MMM-cryptocurrency
2. MMM-WiFiPassword

to do this you simply type:

1. cd MagicMirror
2. cd modules
3. git clone https://github.com/matteodanelli/MMM-cryptocurrency.git
4. git clone https://github.com/TeraTech/MMM-WiFiPassword.git

now go into the config.js file and copy these under modules:
for position

for the cryptocurrency:

{
			module: "MMM-cryptocurrency",
			position: "top_right",
			config: {
				apikey: 'Your API Key',
				currency: ['bitcoin'],
				conversion: 'EUR',
				headers: ['change24h', 'change1h', 'change7d'],
				displayType: 'logoWithChanges',
				showGraphs: true
			}
		},
    
    For the "Your API Key" you need to make a CoinMarketCap Account. 
    There you will be able to get your api key and input into the config.js file.
    

for the WifI:

{
    			module: 'MMM-WiFiPassword',
    			position: "bottom_right", 
      			config: {
        			network: "Your Network Name", 
        			password: "Your Network Password",
      		}
  		},
      
     for the "Your NetworkName" and the "Your network Password". 
     You just need to enter you network info.

--------------------------------

For the news feed module:
You need to need to google search the website that you wann pull news from and add rss at the end. example rte rss. 

you then add that site under url.

If you need any more info on how to install the mirror or any fo the modules used here:
https://github.com/TeraTech/MMM-WiFiPassword
https://github.com/matteodanelli/MMM-cryptocurrency
https://docs.magicmirror.builders/getting-started/installation.html

and if you want to install any other modules:
https://github.com/MichMich/MagicMirror/wiki/3rd-party-modules#utility--iot--3rd-party--integration
