<img src="https://en.gravatar.com/userimage/137186280/decf387e98fa3847f8d28208dd673bca.png" width="70" height="70">

# ORE ID - OAuth for Blockchain



ORE ID allows anyone to access your dApp with one-click sign up and blockchain account creation - using a login flow that they are already familiar with. ORE ID supports Google, Facebook, Github, Linkedin, Twitter, Twitch, and practically any other OAuth-enabled login provider.

With ORE ID, users of your app get an on-chain account upon first sign-in. Their private key is encrypted with a PIN of their choosing and stored for them so they don't have to remember their blockchain accounts or keys.

ORE ID also serves as a blockchain wallet for your your users. Your app can request a user to sign a transaction using their PIN to decrypt their keys.

ORE ID removes the friction between your app and your future users. 

<img src="./docs/images/oreid-steps-graphic.png">

# Usage


## To use in your app

### Step 1 - Register your app and logo

Apply [here](https://aikon.typeform.com/to/YQ5d5r) for early access 

### Step 2 - Install and configure

For Javascript apps, install the npm client module

```
npm install @apimarket/oreid-js 

// Populate .env file with api key (see .env.example)
```

### Step 3 - Keep User Account and Data  

After a login, your app will receive the user's blockchain account name (which maps to public/private keys). Store this account to identify your user. You can also call the user endpoint to get the user's basic identity info (e.g. name, email, avatar picture)

### Step 4 - User can view and control account on the blockchain  

The account is a blockchain account that can be easily viewed on the public blockchain using a block explorer.

The user's account's private key can be transferred to an offline wallet if desired.

Search for chain for the account details and token balances like this - [http://explorer.openrights.exchange/accounts/1p4sr4shbfdt]()


## Example code
```
//Initialize the library

let oreId = new OreId({ apiKey, oreIdUrl });

//Start the OAuth flow by setting the user's browser to this URL
let authUrl = await oreId.getOreIdAuthUrl({ loginType, callbackUrl, backgroundColor });

//Get the user's info given a blockchain account
let userInfo = await oreId.getUserInfo(account);

```


[Frequently Asked Questions](https://drive.google.com/open?id=1Nx6qm7z8TQRM8S-onmcP0H--21z-gzYDBVEzzfcgE9g)

