# Moloch v3 Architecture

Initial thoughts: 
* Split into two to three contracts
    * Voting + Member & Guildbank
    * Voting + Member + Guildbank
* Factory contract that:
    * Launches all 2-3 contracts
    * Launches a Member contract that launches Guildbank and Voting 
* Use updatable interfaces for talking between the contracts

## Architecture

![](https://i.imgur.com/0cmYJRF.png)





