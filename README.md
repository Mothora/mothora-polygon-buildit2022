## What is Mothora?

**Mothora** is a _web3 game of persistent large-scale incentivised 3-way Faction (iFvFvF) battles in Unreal Engine 5_. In the traditional gaming sense it can be regarded as an Online Role-Playing Game (RPG) with strong Player vs Player (PvP) emphasis and a real player-owned economy. It is set in a dystopian sci-fi future, in the aftermath of civilisational decay, where three factions struggle for survival.

The game intends to push the boundaries of Play to Earn and shift the emphasis to the Play aspect, the so-called Play & Earn. The focus is on creating an actual game that players enjoy for the sake of it. In Mothora, three factions compete for map dominance, enabling a plethora of tactical grand strategy decisions and micro duelling scenarios. These factions are themselves subDAOs that can both enact governance proposals for the overall Mothora DAO, as well as proposals that can influence how the faction manages itself. With this system, intense and compelling experiences can be enabled, as players coordinate within and outside the game.

<br>

## Intended Playstyle

The world of Mothora is governed by the $ESSENCE, a natural occurrence that players of different factions must compete for to get the ultimate rewards.

The end goal of a game’s season is for a faction to make their **$ESSENCE Absorber** system the most efficient.

This is a game of intellect, strategy, and social coordination, with a constant meta tension shaping the actions of the players. Players succeed by:

- Thinking ahead and coordinating
- Cooperating with battle companions and guild members
- Understanding well the intricacies of the combat mechanics
- Being knowledgeable in the core economic elements

Mothora follows a model that incentivizes honing skills in battle and the employment of different world-level strategies to maximize in-game rewards. This has the additional benefit of boosting the social component of the game, the degree of interdependence of players, and the sense of belonging to a real evolving community.

<br>

## What is part of this Demo

1. **Polygon Mumbai Testnet** - We elected Polygon as our network of choice for this hackathon due to its speedy transactions and available integration with Chainlink VRF.

2. **Smart contracts**

- MothoraGame.sol: Acts as the main contract with account definition and a registry of all the other contracts. Allows players to enter a faction and defect to other factions
- modules/Arena.sol: Manages the start of a battle between players and its termination, rewarding users with a random number of Artifact NFTs that can be used to increase the eficiency of the Faction $ESSENCE Absorber
- modules/Artifacts.sol: Manages the mint of new artifacts as they are given out in rewards or potentially through crafting (not implemented)
- modules/Cosmetics.sol: Manages the mint of new cosmetic skins, such as character skins. Currently only one demonstration skin exists per faction.
- modules/Essence.sol: The main currency in the game. For demonstration purposes it is minted in its entirety to the deployer address.
- modules/EssenceAbsorber: Users can stake both $ESSENCE and Artifacts in their absorbing system. Ultimately this is what the competition is about, to increase the rewards for their own faction. Users can also unstake, calculate and claim rewards. The reward distribution system is push based by an admin function and we admit this to be a flaw of the system that would be improved into a pull-based mechanism where each user "distributes" to himself/herself the rewards.

3. **Chainlink Implementation** The game requires access to true randomness to be fair when distributing the Artifasct NFTs. The contracts in Polygon Mumbai are requesting random numbers from Chainlink.

4. **Unreal Engine environment** - Built the 3D world where the player makes its in-game actions

5. **Unreal Engine multiplayer** - Allows for multiple characters on the same server in real-time

6. **Unreal Engine <-> Web 3 Integration** - Customized the connection between the Smart contracts and the Unreal Engine Environment that allows the player to trigger blockchain transactions from within the game window and sign them using walletconnect.

<br>

## Smart Contract addresses and important transactions

- **Creation of subscription id 1498**: https://mumbai.polygonscan.com/tx/0x10958f581bd7387f6c7bde613b196239953beae701d1aa0dd5ea7b359873707f
- **MothoraGame.sol_Implementation**: https://mumbai.polygonscan.com/address/0xe7b371386191555b77bc6C9e4AAa325D5e1214fb
- **MothoraGame.sol_Proxy**: https://mumbai.polygonscan.com/address/0xD0a4316a9e1E197b41Cf6530A1bbAd30A6cCc6B7
- **Arena.sol**: https://mumbai.polygonscan.com/address/0x6529F395DcaB1930B3a0561f61526a01Eebb189b
- **Artifacts.sol**: https://mumbai.polygonscan.com/address/0xc48CDc6711aa068A90CcEBf5274E45255c37052A
- **Cosmetics.sol**: https://mumbai.polygonscan.com/address/0x20d7e5D10B16b3fcA8Ea2EE93bb704C8B5894Ad5
- **Essence.sol**: https://mumbai.polygonscan.com/address/0x4D3C09A1BbC80724ca412A2bc13f751E475dB245
- **EssenceAbsorber.sol**: https://mumbai.polygonscan.com/address/0x7F8b7F2c46D23AE6654f855821c22B2f74a94309

### Average test coverage - All files

| Stmts % | Branch % | Funcs % | Lines % |
| ------- | -------- | ------- | ------- |
| 82.44   | 75.41    | 76      | 82.14   |

<br>

## Why are we building this?

Current P2E games are unsustainable in their current model, as they rely on a continuous upkeep of new players to sustain the value of rewards provided in-game. Not only that, but it quickly became apparent that grinding and repeating the same similar actions in hopes of receiving dwindling rewards is extremely non-appealing and the total opposite of fun. “Players” in the P2E arena became reward mercenaries instead of playing for the joy of the game. And it can be quickly agreed that this first breed of P2E games are visually underwhelming and the social component between players is disregarded, leading to low levels of immersion.

Our understanding is also that current P2E game development is almost entirely focused on the “earning money” aspect, how not to over-inflate the economy of the game and keep making it worthwhile as an investment. We do understand the argument that there is a new segment of “players” who view these games purely as financial products and income potential and that it is possible to cater to them with a fine tuned economic model. However, we believe it is not possible to overcome the economic sustainability problem without first making these games appeal to people that actually want to play them for entertainment purposes and not purely as a way to get money.

**This is why Mothora was created**: _because of the shared belief that immersive and fun AAA quality games are absent in the web3 landscape and that most gamers are missing out on rewards due to non-sustainability and entry barriers_. And this demo reflects exactly the begining of that: an immersive and enticing landscape where a few GameFi interactions can be visualized, **using Polygon as the chain of choice due to its reliability, speediness and great ecosystem of existing games, as well as support for Chainlink functions such as verifiable randomness**.

<br>

## What's next for Mothora

It is our goal to build the full-fledged Mothora game.

From a roadmap perspective, there are two main areas we intend to focus in the project:

1. Build a tight knit community around Mothora. We want everyone to understand the values of the game and the choices they can make to further its development. For this purpose, we are soon releasing challenges related to our world to facilitate the creation of a relationship between players and the game. These challenges include the completion of enigmas, following our socials and helping the project by sharing the word.

2. Work on the MVP of an Arena Battle mode - A closed map where the three factions face off on a short time window battle. This task will put strong emphasis on 3D Asset Creation and enhancing the set of smart contracts used in the PoC to display more features and interactions.
