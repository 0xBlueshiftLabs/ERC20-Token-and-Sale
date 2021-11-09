

[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]



# ERC20 Token Creation and Crowd Sale

ERC-20 tokens are blockchain-based assets that have value and can be sent and received. The primary difference is that instead of running on their own blockchain, ERC-20 tokens are issued on the Ethereum network.

Utilising the Truffle framework to test and deploy the token, this repo also contains a rudimentary front end, built with React, that allows users to 'buy' tokens in a crowd sale fashion, reminiscent of the infamous 2017/18 ICO era.

Unit tests of the Smart Contracts, written in Solidity, were performed using JavaScript with Mocha and Chai. These can be found in the /test directory. Said contracts were deployed to Truffle’s local development network before being deployed and tested on the Ropsten and Goerli networks.






### Real-World Use-Cases


💰 Tokenization of any assets as fungible tokens (ERC20)

🏦 Creation of bonus programs, vouchers, etc

💲 Creation of a new crypto currency

🧾 Creation of a payment-layer on top of Ethereum


### Development-Goals


🧰 Develop deeper understanding of truffle-config files

🤖 Understand deployment of dApps

🦸‍♂️ Understand tokenization using Open-Zeppelin Smart Contracts

☑️ Deep dive into unit-testing




## Built With

* [Truffle](https://www.trufflesuite.com/)
* [React](https://reactjs.org/)
* [Open Zeppelin](https://openzeppelin.com/)
* [Mocha](https://mochajs.org/)
* [Chai](https://www.chaijs.com/)
* [Web3js](https://web3js.readthedocs.io/en/v1.3.4/)
* [Node.js](https://nodejs.org/en/)
* [Solidity](https://docs.soliditylang.org/en/v0.8.6/)


<!-- GETTING STARTED -->
## Getting Started

1. Enter the inital token supply and your wallet mnemonic in the env file
  ```sh
   INITIAL_TOKENS=
   MNEMONIC=
  ```
   
2. If looking to deploy on ETH test networks or main net then enter the relevant URL path for your web3 connection in the truffle-config.js file ([Infura](https://infura.io/) was used for this project)
  ```JS
    // Ethereum network of choice e.g:
    ropsten_infura: {
      provider: function() {
        return new HDWalletProvider(process.env.MNEMONIC, "INSERT Web3 PROVIDER ADDRESS HERE", AccountIndex)
      },
      network_id: 3
    }
   ```
   
3. To run the front end locally (at http://localhost:3000), ensure you are in the "client" directory and use a terminal to execute the following
  ```bash
  npm run start
  ```
  
<p align="center">
  <img width="777" height="393" src="/screenshot.png">
</p>

4. Changing the token's name and ticker can be acheived through editing MyToken.sol in /contracts (don't forget to update the front end too!)
  ```sol
  constructor(uint256 initialSupply) ERC20Detailed("Azure","AZE", 0) public {
  ```
  
5. Changes to the front end can be made by editing the App.js file found in /client/src
 
  

<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE` for more information.



<!-- CONTACT -->
## Contact

Twitter - [@TraderTDF](https://twitter.com/TraderTDF)

LinkedIn - [https://www.linkedin.com/in/RAMWatson/](https://www.linkedin.com/in/RAMWatson/)

Project Link: [https://github.com/Elisik/ERC20-Token-and-Sale](https://github.com/Elisik/ERC20-Token-and-Sale)



<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements

* [Ethereum Blockchain Developer Bootcamp With Solidity (2021)](https://www.udemy.com/course/blockchain-developer/)




<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[license-shield]: https://img.shields.io/github/license/othneildrew/Best-README-Template.svg?style=for-the-badge
[license-url]: https://github.com/othneildrew/Best-README-Template/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://www.linkedin.com/in/RAMWatson/
[product-screenshot]: screenshot.jpg
