
# PancakeSwap Prediction v3

![PancakeSwap-Logo-Big](https://user-images.githubusercontent.com/37302442/142642313-475cd6f8-0050-4925-8604-0c0370b0a69c.png)

This bot fetches the overall consensus of the 5min and 1min BNB/USDT charts based on a number of TA signals provided by Trading View. It determines if the consensus is a BUY or SELL prior to each prediction round and places the bet on PancakeSwap or CandleGenie accordingly.

If you found this helpful then you can buy me a coffee at `0x1c423F7dc5d63F9355caCC540AEDB69d27A31f3b`.

## Table of Content
* [Installation](#installation)
* [Usage](#usage)
* [Strategies](#strategies)
* [Screenshots](#screenshots)
* [License](#license)
* [Disclaimers](#disclaimers)

## 💡 Installation

Download & Install Node here :
https://nodejs.org/en/download/

Then run command prompt or powershell.  

- Type ``cd PancakeSwap-Prediction-v3`` (replace with your cloned/downloaded bot folder)
- Type ``npm i``

## 🧑‍🚀 Usage

1. Copy/rename **.env_sample** to **.env** ``cp .env_sample .env``
2. Provide your private key to .env PRIVATE_KEY field.
3. Install dependencies `npm i` or `yarn` if not already completed above.
4. Start the bot using `npm run start -- --with` or `yarn start -- --with`
5. Enjoy!

Feel free to contribute. Good Luck!

### 🦊 How to Export Private Key from MetaMask
1. Open your account
2. Click on three points at top-right corner
3. Account details
4. Export Private Key

### 🧰 Sample ``.ENV`` file
```
# Your wallet private key. 
PRIVATE_KEY="YOUR_PRIVATE_KEY_HERE"
# The maximum bet amount you are willing to execute.
BET_AMOUNT="0.002"
# RPC is the default network for Ether transactions. For Binance Smart Chain, leave it as it is.
RPC="https://bsc-dataseed.binance.org/"
```

Note: This is not production ready script so please make sure to change ``to:`` field in ``src/index.ts`` and ``src/candle-genie.ts``.

## 🧑‍🎨 Strategies
- Default Strategy: Bets against what the majority of money is betting on. It generally aims for the higher payout bet. Better for sideways trends where its harder for the majority of people to bet correctly & confidently.

- `--with` Strategy: Bets with what the majority of money is betting on. It generally aims to follow the lower payout bet. Better for swinging trends where its easier for the majority of people to bet correctly & confidently.

### Using CandleGenie? 
If you want to play with Candle Genie instead of Pancake, start the bot with `npm run cg` or `yarn cg`

- To use the alternate `with` strategy, start the bot using `npm run start -- --with` or `yarn start -- --with`.
- For CandleGenie, use `npm run cg -- --with` or `yarn cg -- --with`

## 🧪 Screenshots

To check history of the rounds you played, head over to: https://pancakeswap.finance/prediction

![History](https://user-images.githubusercontent.com/37302442/142716425-eb32f875-a767-4f22-abf1-6d97071dbd6d.png)

Running this bot for a day had made me $55 with minimum bets. Please note I was actively monitoring the market as the bot was running.

![History_2](https://user-images.githubusercontent.com/37302442/142724431-48a7c301-ee59-4485-9733-3ee5a0303c00.PNG)

#### 📢 Advice:
- Run the bot with your wallet at a ratio of 10x the amount you choose to bet.
- Adjust the bot accordingly to bet with or against the majority.
- When the chart swings, use the "--with" strategy.
- When the chart trends sideways, use the default, against strategy. 
- Always monitor & adjust the bot accordingly but allow room for error.
- Consistent gains will be made by running smaller betting amounts over longer periods of time. 
- Always account & allow room for error. Losing 3 sucks, but stopping it only prevents it from potentially winning the next 4 & bringing you to a profit. 
- Majority of the runs with over 2k plays I have a standard 54-66% win rate depending on how well I monitor it & based on market conditions.

## 💼 License
MIT License

## 💥 Disclaimers
All investment strategies and investments involve risk of loss.

**Nothing contained in this program, scripts, code or repository should be construed as investment advice.**
Any reference to an investment's past or potential performance is not, and should not be construed as, a recommendation or as a guarantee of any specific outcome or profit. By using this program you accept all liabilities, and that no claims can be made against the developers or others connected with the program.

⚠️ **WARNING** ⚠️ Please try to bet with the lowest amount so you don't run out of balance before you even start. Please note that on every bet there's 10% fee. If you want to remove this, contact me (`0000@disroot.org`).
