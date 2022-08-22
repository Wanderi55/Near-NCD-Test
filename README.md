# Near-NCD-Test

First Smart Contract Project on Near Protocol In the Learning Path

This project is my first Smart Contract work on the Near Protocol.

## To run the smart contract
required:

yarn
npm
assemblyScript

run npm init to change the package.json with your project name any other modification you may want

then npm install - to install any missing dependencies and the nodule_modules

## (Highly Recommended) Create NEAR testnet account for running the tests NOT mainnet account. Once the account is ready run the following commands:

near login 

(a pop-up browserwindow appears and prompts you to authoriuze for your testnet account use)
Once you have authorised the account go back to your CMD and inopuit the account you authorised(mytestacc.testnet)
  
near create-account mycontract.myaccount.testnet --masterAccount myaccount.testnet --initialBalance 5
(This is to create a subaccount to deploy the smart contract)

### For windows but should run well also in Linux via the linux commands
run yarn

then run yarn build or yarn run build

once the build folder (build/debug/nameofmyproject.wasm) is created with the wasm file you can test with the following commands:

#### to Deploy:->

near deploy --accountId mycontract.myaccount.testnet --wasmFile build/foldername/${WASM_FILE_NAME}

#### to call(Create a new product in the blockchain):->

near call \${CONTRACT_ACCOUNT_ID} \${METHOD_NAME} \${PAYLOAD}  --accountId \${ACCOUNT_ID}

E.g: near call mytest.accname.testnet setProduct "{\"id\": \"0\", \"productName\": \"tea\"}" --accountId accname.testnet

#### to view:->

near view \${CONTRACT_ACCOUNT_ID} \${METHOD_NAME} \${PAYLOAD}

E.g: near view mytest.accname.testnet getProduct '{\"id\": \"0\"}'


Comments and feedback will be greatly appreciated
