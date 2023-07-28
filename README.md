# Jewel Forge
The Jewel Forge project has been created to provide a standard way in which ERC6551 NFTs can be created. The purpose is to issue an NFT i.e. a Jewel, that can be used as a form of on chain collateral. There are several considerations that the project will look to take into account. These are: 

 1. Composition Stability 
 2. Composition Volatility 
 3. Jewel Destruction. 
 
 ## Composition Stability 
 The issue of composition stability is an important one. Simply put it should not be possible to alter the Composition of the Jewel whilst it is in use. This includes the addition and removal of assets ignorant of the value of those assets. This is an important factor in the creation of reliable collateral and prevention of fraud. 

## Composition Volatility 
As a composite on chain object the value of each of the contributing assets of the Jewel is not uniform nor does it vary in a uniform manner. This means that whilst the majority of the contributing assets may have a strong tendency towards stability this may be impacted by 1 or 2 elements that are suffering from high volatility. The impact of this is then reflected in the collateral basis. 

## Jewel Destruction 
As an NFT, Jewels can be destroyed through the **burn** process. The Jewel Forge will destroy Jewels by burning the owning NFT and then disbursing the assets to the current owner address. The function here being that you can only destroy Jewels that you own. 

# Jewel Processes
## Jewel Creation Process 
The diagram below represents an outline model of how Jewels will be Forged:
![enter image description here](https://github.com/cryptotwilight/jewel-forge/blob/main/media/jewel%20forge.drawio.png?raw=true)
In this process:

 1. The owner commits their assets which are held in the Asset Contracts to the Forge
 2. The Forge then proceeds to mint the Jewel NFT as an IERC721 token. 
 3. The Forge then proceeds to create the IERC6551 account for the Jewel NFT 
 4. The Forge then proceeds to mint a further soul bound NFT which holds the Account Descriptor, for the Jewel NFT account. 
 5. The Jewel Forge then proceeds to transfer the initial set of assets held by the Owner to the Jewel NFT Account 
## Jewel Destruction Process 
The diagram below describes the Jewel Destruction Process 
![enter image description here](https://github.com/cryptotwilight/jewel-forge/blob/main/media/jewel%20forge-Jewel%20NFT%20Destruction.drawio.png?raw=true)
in this process: 
 1. List item the Owner issues a request to the forge to destroy a Jewel that they own. 
 2. The forge will then proceed to disburse to the current Jewel Owner the assets held by the IERC6551 Account.
 3. Once all assets have been disbursed the Forge issues a command to the burn the Jewel on the IERC721 contract.
