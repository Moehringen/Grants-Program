# W3F Grant Proposal


* **Project Name:** Web3Go
* **Team Name:** Web3Go
* **Payment Address:** 0xD57e28773c92E6fB9D9Fb164889886cd360074BE(USDT)
* **[Level](https://github.com/w3f/Grants-Program/tree/master#level_slider-levels):** 2


## Project Overview :page_facing_up:

### Overview

Web3Go is an open data platform that focuses on the formatting, visualization, sharing, and collaboration of the on-chain data generated in the Polkadot ecosystem.

Due to the explosion of Defi, NFT, and metaverse, the blockchain generates a large amount of data every day, which is very important information for the media, investment institutions, and blockchain participants. However, it is difficult for non-professionals to obtain and understand these data. Data is valuable. Our project is to build a data platform for the Polkadot ecosystem and provide a series of toolsets so that everyone can easily obtain visualized results of data analysis. We will track all valuable information on-chain such as smart contracts, including various parameters like the stake and CDP of different Defi protocols, NFT circulation, and cross-chain assets on Polkadot ecosystem, and make these data formatted and persisted. With the help of the smart contract on Substrate parachain,   non-professionals can publish their data needs on the platform and use rewards to motivate professionals to help them perform data analysis; for professionals, they can publish their own professional analysis for everyone to use paid or for free. In the second situation,  they can get the reputation from the community.  In the end, we broke the monopoly of some existing companies on data analysis and interpretation, so that everyone can truly enjoy the true value behind blockchain data.



We believe that with the development of Polkadot ecosystem, more on-chain data will be generated and the value behind the data is giant. Currently, there is still a gap between professional users and common participants. Using the infrastructure and tools provided by Web3Go, everyone can easily create, publish and share their point of view in the form of nice charts  based on the real data which has been formatted from the blockchain.

The interpretation and analysis of data should not be in the hands of certain centralized professionals, but all should also benefit from it. Our vision is to build a Polkadot-based data analytics infrastructure, toolset, and incentive system that anyone can publish and reward for related data tasks. Finally, an open and free data platform will be built to signal what happens on the Polkadot system.



### Project Details

#### Architecture

![](https://github.com/Moehringen/Storage/blob/main/Polka-Analytics.png)


#### Components
1.  **Indexer:** an indexer of blockchain is used to extracts the on-chain data and saves the data in the database in formatted manner. Since the Polkadot network is composed of relay chain and parachains, each parachain can define its own Event or call, so each indexer of the parachain must be adapted according to its metadata. So there will be multiple instances of the indexer of Polkadot.  


2. **Data Board:** 
data board is the visualization result of data analysis created by analysts, which can display the analyzed and customized  information on the Polkadot ecosystem such as a token transaction or holders,  an NFT transfer, and history of the transaction, the statistics of a Defi protocol, or some special event like parachain auction, and governance. 


3. **Contract on Substrate:**
The smart contract on Substrate node is used to demand, publish, share and reward the data activities within Web3Go. there are two kinds of players involved in the smart contract:  data demander, who has a need of professional, visualized result of data analysis regarding some events that happened on the blockchain, so the data demander will publish the need through the contract with bounty,  to incentive the one who can help with this needs; on the other hand,  data analyst, who has professional knowledge and skills can accept the publisher of the need, or they can publish and share any data board they have created to the community in a paid or free manner. This smart contract will incentive more people to contribute to the data activities in the ecosystem and valuable data boards will receive more reputation. 




4. **Query Module:** query module provides a user interface to the data analyst to generate a data board.  The data stored on the blockchain is in the form of key-value pair, so it is very hard to use and analyze the on-chain data directly.  With UI provided by the query module and alone with the chart display module,  the analyst can manipulate the formatted data and visualize it in an automatic and customizable manner, and the data will be automatically synchronized with the blockchain. The updating will be reflected on the data board directly. 
   

5. **Chart Display Module:** The chart display module is used to visualize the result of data analysis and is the main component of the data board. The chart display module can provide different charts like bar charts, pie charts, scatter plot, and so on. 


6. **Subscription Module:** For each created data board,  the data demander of this data board can subscribe to the notification signaled from this board.  The notification can be a big transaction of a token or an APR vary of a Defi protocol.  This module provides the capabilities for the subscription.  
  

7. **Label/Tag Module:** this module will give the address different labels basing on its historical activities on the blockchain, e.g. token transfer,  Defi participation, etc.  It is survied that at least more than 50% of the total addresses on Blockchain are inactive. So this module will label and filter the active address according to its activities such as "Big Whale", "High Activity" and so on.  The labeled addresses are a very good dataset that can be monitored to signal what is happening on the blockchain. 



8.  **Data Mining Module:** data mining module is used to look for regulations and patterns in large batches of data come from blockchain.  data mining is widely used in some traditional industries like Retail, manufacturing, financial and financial insurance, but we believe that apply this technology will benefit the blockchain industry. The module will dig through historical data to discover hidden connections and predict future trends in the specific area of the blockchain, like token price prediction,  Defi earns prediction, etc.  


9.  **Community Module:**  a community module is a public place where data activities participants can communicate. for example,  data demander can publish their demand, the data analysts can accept the task or share their data board, and the most welcome data boards are listed here. 





#### Technologies:
* [Subquery](https://subquery.network/) is a blockchain indexer for Polkadot, Kusama, and other parachains. We will rebuild and customized this framework to fulfill our requirements.
* Node.js
* Docker
* Substrate
* Rust
* Machine Learning
* Python

#### PoC:
A [web application](https://web3go.xyz/) with three data boards has been created for the proof of concept. We have used the architecture mentioned above to index three kinds of tokens: LIT, ATA, and POLS. With nice charts and tables, the transaction, holders are visualized and some addresses have been labeled according to the labeling rules; the second data board listed the crowdloan event on Kusama networks. This data board listed the contribution and participants for each project which attends the crowdloan event; the third data board tracks the CDP(collator debt position) status of Karura lending system and provides the real-time status of each account.



### Ecosystem Fit

We have found several successful data analysis projects in the Ethereum ecosystem.  Each project focuses on a specific area: Defi tracking, token tracking, wallet profile tracking.  But currently, there is no data analysis project designed for Polkadot.  Due to the structure of the Polkadot network, there will be more interesting data generated in the network, so we believe the whole community needs a data analysis tool as soon as possible. 

Similar projects
* https://www.nansen.ai/
* https://duneanalytics.com/
* https://0xtracker.com/
* https://debank.com/
  

What makes us different is

As a part of Web 3 community and Polkadot ecosystem
* The first project focuses on the data analysis for Polkadot world
* Designed to let everyone can benefit from the value of data in the Polkadot world and make the valuable data public to everyone, not in the hand of one centralized project 
* An incentive mechanism that will involve everyone to participate in the data activities. 
* A comprehensive analysis not only focuses on one area but will include all data like a cross-chain asset, governance,  auction, Defi, staking, and token.

## Team :busts_in_silhouette:

### Team members

* Hao Ding: VP of Litentry. MSc of University Suttgart.
* Yifei Wu: Substrate lead of Litentry. PhD of Tokyo University.
* Han Zhao: Substrate core dev of litentry. MSc of University Suttgart.
* Minqi Wang: Backend and contract developer. Master of University Columbia.
* Yunjian Bian: Software Architect of Litentry. Bachelor of University Suzhou.

### Contact

* **Contact Name:** Hao Ding
* **Contact Email:** hao.ding@litentry.com
* **Website:** https://web3go.xyz

### Legal Structure

* **Registered Address:** T5-1023, Europe and America Finance City, Yuhang district, Hangzhou, Zhejiang of China
* **Registered Legal Entity:** Hangzhou Liteng Network Technology Co., Ltd.

### Team's experience

All team members of Web3Go are from Litentry. Litentry is a DID (distributed identity) solution provider in the Polkadot ecosystem. Litentry has been granted a grant from the Web3 Foundation.

Web3Go team members have strong engineering background: Han Zhao, Yifei Wu and Minqi Wang are responsible for the development of Litentry's parachain (https://github.com/litentry/litentry-parachain), Hao ding and Yunjian Bian are responsible for the on-chain data indexing And front-end and back-end development. (https://github.com/litentry/data-analysis)

### Team Code Repos

* https://github.com/web3go-xyz Web3Go official repository
* https://github.com/web3go-xyz/web3go  Backend and UI of web3go
* https://github.com/web3go-xyz/Indexer Indexer of Moonriver staking



* https://github.com/h4n0 Han Zhao
* https://github.com/bianyunjian Yunjian Bian
* https://github.com/Satoshi-Kusumoto Yifei Wu
* https://github.com/wangminqi Minqi Wang
* https://github.com/Moehringen Hao Ding

### Team LinkedIn Profiles (if available)

* https://www.linkedin.com/in/zhaohan6/ Han Zhao
* https://www.linkedin.com/in/%E4%BA%91%E5%81%A5-%E5%8D%9E-5a2b9112a/ Yunjian Bian
* https://www.linkedin.com/in/john-wu-72960586/ Yifei Wu
* https://www.linkedin.com/in/minqi-wang-53b5b19b/ Minqi Wang
* https://www.linkedin.com/in/hao-ding-msc-pmp-64411193/ Hao Ding

## Development Status :open_book:

* [Moonriver parachain Indexer](https://github.com/web3go-xyz/Indexer): This indexer basing on the tools provided by Subquery, is used to index relevant events such as Nomination,JoinedCollatorCandidates and Rewarded events. After persisting the data generated by these events, the DApp can provide the customized data board in terms of staking profit, history, and prediction. 
* [UI Mock-ups](https://drive.google.com/drive/folders/1NIEB0Tbj7tIcf7Q2CRzuMwbkU95ADnH4?usp=sharing): here saved the UI design and mock-up of Web3Go, it is keep updating.
* [Back-end and UI](https://github.com/web3go-xyz/web3go): here saved the UI design and mock-up of Web3Go, it is keep updating.


## Development Roadmap :nut_and_bolt:


### Overview

* **Total Estimated Duration:** 3 months
* **Full-Time Equivalent (FTE):**  2 FTE
* **Total Costs:** 40,000 USD

### Milestone 1 Example — Implement Substrate Modules

* **Estimated duration:** 2 month2
* **FTE:**  2
* **Costs:** 25,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | Apache 2.0 
| 0b. | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can use the existing data board, and use the UI to create/publish their own customized data board|
| 0c. | Testing Guide | Core functions will be fully covered by unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| 0d. | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 0e. | Article | We will publish an **article**/workshop that explains the concept and vision of Web3Go
| 1. | Indexer| We will develop our customized indexer on the top of Subquery to make it more compatible to our scenario |  
| 2. | UI Module:general WebApp| We will create a web application that implements user sign-in/sign-up, categorization of data board,  social interactions functionality including like and share,  subscription of a specific event comes from a specific data board,  entry to the documentation, introduction, etc. |  
| 3. | Backend| We will create a strong backend that communicates with our customized indexer and periodically synchronize to the real-time data on-chain. On the other hand, the backend will support all functionality of the UI. |  
| 4. | Data Board:KSM crowdloan| We will create a data board that tracks the KSM crowdloan event basing on our customized indexer. The data board will contain the real-time status of crowdloan,  including the current progress of each project,  contributions, and historical analysis. |  
| 5. | Data Board:Karura CDP| We will create a data board that tracks the CDP information of Karura, and provide the historical analytics of each participant based on our custom indexer|  
| 6. | Data Board:Moonriver staking| We will create a data board basing on our customized indexer, which tracks the staking history of the collator, the nominator, and their rewards, and predict the possible rewards by real-time on-chain events to provide guidance of maximizing the profit of a potential participant|  
| 7. | UI Module: semi-automatic chart generation| We will create a UI module to let users can generate visualized charts automatically by simply writing SQL language based on our existing indexed and formatted data. In the first milestone, the supported chart is bar chart, line chart, and pie chart. The word "semi-automatic" means that the user still has to write SQL to generate the chart. In the second milestone, we will provide a fully automatic way to achieve it.|  

### Milestone 2 Example — Additional features

* **Estimated Duration:** 1 month
* **FTE:**  2
* **Costs:** 15,000 USD

 Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 1. | UI Module:support more charts| we will continue optimizing the automatic generation of charts, to make it support more kinds of charts like scatter charts, area charts, and tables.|  
| 2. | UI Module:fully-automatic chart generation| We will enhance the user interaction of generating charts, provide the "drag and create" module for the user to generate charts. In this case, the user can generate charts with the same complexity as writing SQL can do. This functionality will provide a more easy way for the user to generate complicated charts who does not know program with SQL.|  
| 3. | Data Board:3 more| We will create at least 3 kinds of data board comes from other projects that have already won the bid in the Kusama auction(or Polkadot auction if it happens), so we will have more value data board on our platform and attract more user come. 
| 4. |UI and backend Module: labling system | With more data we have accumulated, we will create a new UI to present the labeled address. we will give the address different labels basing on its historical activities on the blockchain, e.g. cross-chain transfer,  Karura  CDP participation, etc. The labeled addresses are a very good dataset that can be monitored to signal what is happening on the blockchain.  


## Future Plans

* As our vision is to let "everyone enjoy the value behind the blockchain data", we will design the token economics to let more people involved in the whole data board activities. The rough idea is to design three kinds of roles: data demander, data analyst, and data validator, and introduce the token incentive to incentive the community to create more customized and interesting data boards, and this will be done through the parachain system. So after this grant is finished, we will immediately launch the token economics design and parachain development. 
* As our team is a sub-team of Litentry, so we have a strong development team and operations team and have a 60k+ community, and have a good relationship with most of the projects in the Polkadot ecosystem.  all of the above has provided us a strong foundation of success. we want to be the best data analysis project in the Polkadot ecosystem, and collect more data across other public chains in the future. 


## Additional Information :heavy_plus_sign:

**How did you hear about the Grants Program?**  

Web3 Foundation Website and  personal recommendation.

