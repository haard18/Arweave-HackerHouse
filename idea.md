# SAM (Security Audit and Monitoring)
## Overview
 - This Idea revolves around the need for apt tools to monitor activity over Arweave/AO Development
 - It has features that would be helping the developers identify the vulnerabilities of the contracts/programs they create over AO and deploy it to Arweave.
 - It is divided into 2 subparts that make up the complete monitoring and audit 	mechanism. 
 -- Offchain
 -- Onchain
 ### 1. OffChain SAM
 - The offchain part of SAM will be responsible for the following tasks
 -- **Static Code Analysis**=> The main smart contract creation language ie LUA will be analyzed on the go while writing the code such that developers are made to use the best code practices and not Make syntactical errors while making a contract. Basically providing a Code review.
 -- **Pattern Matching**=> The latest security intelligence for known vulnerabilities (maybe through ORBIT) and fed into a known database, these patterns if found in the smart contract will be prompted to the developer regarding the possible leaks and vulnerabilities before even deploying the contract.
 -- **Testing Environment** => The package will also involve testing functionalities which can be modified as the developer's use Case, there would be fuzz testing, runtime testing and sandbox testing(still figuring out how to implement).
 -- **Frequently Used Contract templates** => To make the lives of developers easier, the SAM Package would involve frequently used templates which they can  look at and take reference from and understand the best practices
#### Implementation Methods/Deployment
- We have two methods to deploy the offchain subpart of SAM:-
1.  **APM** => Releasing a Package that can be installed and would offer these features out of the box
2. **VSCODE Extension** => Releasing a vscode extension with commands for these features
#### Tech Stack
- Python Libraries like Luaparser for code review
- Pattern matching through a database 
- Python Testing libraries like hypertest , pytest for creating and simulating the testing Environment.

#### 2. Onchain SAM
- A Platform SamVerse, Deployed over permaweb which would provide the feature for any smart contract to have its own Watcher Contract
#### WorkFlow
1. Signup on the platform and connect Wallet.
2.  You will be encountered with an input box where you can provide your Contract ID/Process ID.
3. Deposit required amount of AR TOKENS to get your Watcher contract.
4. The Watcher contract will then monitor all the interactions/messages for your process Id and you can set thresholds.
5. These Thresholds on exceeding would get you notified about the Source of them.
6. The watcher contract will also be able to identify shady/suspicious activity and messages sent to your process.
- Hence This would prove to be the Batman for your Processes which are deployed on AO
#### TechStack
- We need feedback over what would be the best practice to deploy such contract and manage the load over it as we would like each person to get their own version of Watcher Contract
- **Frontend** 
 -- React
 --Tailwind
 --DaisyUI
- **Backend**
 --Lua based Contract ie Watcher Contract
 -- NodeJS for load balancing/Handling(Not sure)
 -- Database of users on WeaveDB
 #### BetaBounty (50 Shades of Exposure)
 - This would help the users to run a bug bounty campaign over the identified vulnerabilities by the watcher contract
 ---
#### FEEDBACK REQUIRED ON FOLLOWING TOPICS
1. General Implementation and workflow
2. LUA Contract Tracking
3. Any changes on Tech Stack 
4. Enhancements on The Idea

