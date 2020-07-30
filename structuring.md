# Moloch V3 - Modular Molochs

Step 1: Come up with a wishlist 

Step 2: Define tighter requirements 

Step 3: Outline structure & create tasks

Step 4: Let's hack together 

# Philosophy 

## The Issues
Create a more modular moloch framework to address a few core issues: 

* Gas fees, 
* Contract size limits, and
* Upgradability. 

The issue with gas fees is related to both launching and interacting with a moloch. We probably can't make summoning a moloch "cheap," but we can make it possible for projects to launch part of a moloch on xDAI and connect it to the rest of the moloch on mainnet via an arbitrary message bridge. 

The issue with contract size limits has to do with containing all of the functions in a single large contract, which is good for security, but sacrifices the ability for developers to do further customizations. 

The issue with ugradeability has to do with the ability to upgrade parts of existing molochs and the ability for developers to customize parts of a moloch. For example, a moloch might want to switch from standard moloch voting to quadratic voting, so they should be able to upgrade (via vote) the voting system used by their moloch. Similarly, a developer might want to develop a moloch that works with quadratic voting without having to dive into the entire moloch codebase and potentially hit the EIP-170. 

## Moloch Primatives

Molochs have three primatives: 

* Decisionmaking (i.e voting and proposals)
* Membership (i.e. share and loot holders)
* Money (i.e. token balances)

To avoid adding too much complexity, we should modularize around these primitives. One of Moloch's advantages is that the code is relatively easy to follow, so splitting it into to many contracts could make it hard for new devs to experiment with molochs. Though, we probably also want to keep helpful extension contracts like the Minion. 



# The Wishlist 

List of other wishlist items (with primitive in parens): 
* Ability to handle ETH as tribute / a currency (Money)
* Ability to re-add Guild Kicked Members (Members)
* Ability for anyone to send tip / payment to DAO and reflect that in GuildBank (Money)
* Ability to sponsor a proposal immediately, but only allow for proposal submissions at a certain interval (Decisionmaking)
* More modular roles (Members, Decisionmaking)
* Ability to remove tokens from whitelist (Money)
* Multi-summoner and auto-member functionality (Member)