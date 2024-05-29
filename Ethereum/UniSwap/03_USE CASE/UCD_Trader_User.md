### Trader/User Use Cases

#### **1. Connect Wallet**
   - **Use Case Name:** Connect Wallet
   - **Actor:** Trader/User
   - **Description:** Allows users to connect their cryptocurrency wallets to the platform to enable trading and other blockchain interactions.
   - **Preconditions:** User has a compatible cryptocurrency wallet.
   - **Postconditions:** Wallet is connected, enabling transactions and interactions.
   - **Main Success Scenario:**
     1. User selects 'Connect Wallet' on the platform.
     2. User chooses their wallet provider from the list.
     3. User authenticates and authorizes the connection via the wallet interface.
     4. Platform confirms the wallet connection and updates the user interface.
   - **Extensions:**
     - **3a. Authentication fails:**
       - **3a1.** Platform displays an error and advises checking credentials or wallet status.

#### **2. Swap Tokens**
   - **Use Case Name:** Swap Tokens
   - **Actor:** Trader/User
   - **Description:** Enables users to exchange one type of token for another based on current market rates within the platform.
   - **Preconditions:** User has connected wallet with sufficient balance.
   - **Postconditions:** Tokens are swapped, and balances updated.
   - **Main Success Scenario:**
     1. User selects 'Swap Tokens' from the trading interface.
     2. User inputs the amount and type of token they wish to swap.
     3. Platform displays the equivalent amount of the target token based on the current exchange rate.
     4. User confirms the swap.
     5. Platform executes the transaction and updates both token balances.
   - **Extensions:**
     - **4a. Insufficient balance:**
       - **4a1.** Platform notifies the user and cancels the swap.

#### **3. View Data of Tokens, Pools, and Transactions**
   - **Use Case Name:** View Data
   - **Actor:** Trader/User
   - **Description:** Allows users to view detailed data on tokens, liquidity pools, and past transactions.
   - **Preconditions:** User has access to the platform.
   - **Postconditions:** Data is displayed to the user.
   - **Main Success Scenario:**
     1. User selects 'View Data' from the menu.
     2. User chooses to view tokens, pools, or transactions.
     3. Platform displays the selected data, including detailed analytics.
   - **Extensions:**
     - **3a. Data not available:**
       - **3a1.** Platform notifies the user and suggests alternative queries.

#### **4. Buy NFTs**
   - **Use Case Name:** Buy NFTs
   - **Actor:** Trader/User
   - **Description:** Allows users to purchase NFTs available on the platform, transferring ownership upon successful transaction.
   - **Preconditions:** User has a connected wallet with sufficient funds.
   - **Postconditions:** NFT is transferred to the user's wallet; ownership is updated on the blockchain.
   - **Main Success Scenario:**
     1. User navigates to the NFT marketplace section.
     2. User selects an NFT to purchase.
     3. Platform displays NFT details, including price and history.
     4. User confirms purchase and completes payment.
     5. Platform updates ownership and displays confirmation.
   - **Extensions:**
     - **4a. Payment fails:**
       - **4a1.** Platform notifies the user and does not transfer ownership.

### **5. Add liquidity to Existing Pools:**  
Use Case Name: Add Liquidity  
Actor: Trader/User  
Description: Users can add liquidity to existing pools to facilitate trading and earn transaction fees in return.  
Preconditions: User has a connected wallet with sufficient balance of required tokens.  
Postconditions: User's liquidity is added to the pool; liquidity tokens are issued as proof of the contribution.  
Main Success Scinerio  
     1. User selects the liquidity pool from the platform interface.
     2. User specifies the amount of tokens to add.
     3. Platform displays the amount of liquidity tokens to be received.
     4. User confirms and completes the transaction.
     5. Platform issues liquidity tokens to the user's wallet.
   - **Extensions:**
     - **4a. Insufficient token balance:**
       - **4a1.** Platform notifies the user and aborts the transaction.

#### **6. Participate in Governance (using UNI tokens)**
   - **Use Case Name:** Participate in Governance
   - **Actor:** Trader/User
   - **Description:** Enables UNI token holders to vote on proposals or submit new proposals for changes to the platform.
   - **Preconditions:** User possesses UNI tokens and is registered on the governance platform.
   - **Postconditions:** User's vote is cast or new proposal is submitted.
   - **Main Success Scenario:**
     1. User logs into the governance platform.
     2. User browses open proposals.
     3. User selects a proposal to vote on.
     4. User submits their vote using UNI tokens.
     5. Platform records the vote and updates the proposal status.
   - **Extensions:**
     - **5a. Voting period expired:**
       - **5a1.** Platform informs the user and disallows the vote.

#### **7. Use Custom Trading Interfaces**
   - **Use Case Name:** Customize Trading Interface
   - **Actor:** Trader/User
   - **Description:** Allows users to customize the trading interface according to their preferences for a more personalized trading experience.
   - **Preconditions:** User is logged into the platform with access to customization settings.
   - **Postconditions:** Trading interface is personalized as per the user's settings.
   - **Main Success Scenario:**
     1. User accesses customization settings.
     2. User selects their preferred layout, indicators, and tools.
     3. User saves the settings.
     4. Platform applies the settings to the user's trading interface.
   - **Extensions:**
     - **3a. Error in saving settings:**
       - **3a1.** Platform notifies the user and requests a retry.

#### **8. Execute Automated Trading Strategies**
   - **Use Case Name:** Execute Automated Trading
   - **Actor:** Trader/User
   - **Description:** Users can execute predefined trading strategies automatically through a trading bot or similar automated systems.
   - **Preconditions:** User has set up a trading bot with valid strategies and linked it to their trading account.
   - **Postconditions:** Trades are executed according to the strategies without manual intervention.
   - **Main Success Scenario:**
     1. User configures and activates the trading bot.
     2. Bot monitors the market based on the defined strategies.
     3. Bot executes trades when market conditions meet strategy criteria.
     4. User receives notifications of executed trades.
   - **Extensions:**
     - **3a. Market conditions do not meet strategy criteria:**
       - **3a1.** No trades are executed; bot continues monitoring.

#### **9. Access Historical Transaction Data**
   - **Use Case Name:** Access Historical Data
   - **Actor:** Trader/User
   - **Description:** Users can access and review their historical transactions to analyze past performance and make informed decisions.
   - **Preconditions:** User is logged into their account with access to transaction history.
   - **Postconditions:** Historical transaction data is displayed to the user.
   - **Main Success Scenario:**
     1. User navigates to the transaction history section of the platform.
     2. User selects the type of data and date range they wish to view.
     3. Platform retrieves and displays the requested data.
     4. User reviews the transaction history.
   - **Extensions:**
     - **3a. Data retrieval fails:**
       - **3a1.** Platform notifies the user and suggests alternative actions or retry.

#### **10. Use Mobile Interfaces for Trading**
   - **Use Case Name:** Mobile Trading
   - **Actor:** Trader/User
   - **Description:** Users can conduct trading activities using a mobile interface, ensuring accessibility and convenience.


   - **Preconditions:** User has the mobile app installed and is logged in.
   - **Postconditions:** Trades can be conducted and managed through the mobile interface.
   - **Main Success Scenario:**
     1. User logs into the mobile app.
     2. User navigates through a mobile-optimized trading interface.
     3. User performs trading actions like buying, selling, checking balances, etc.
     4. Platform processes and confirms the transactions on the mobile app.
   - **Extensions:**
     - **3a. Mobile app malfunctions:**
       - **3a1.** User is advised to restart the app or contact support.

#### **11. Analyze Market Trends**
   - **Use Case Name:** Market Trend Analysis
   - **Actor:** Trader/User
   - **Description:** Provides tools and data for users to analyze current market trends and make informed trading decisions.
   - **Preconditions:** User is logged into the platform and has access to market analysis tools.
   - **Postconditions:** Market trends and relevant data are displayed, aiding the user in trading decisions.
   - **Main Success Scenario:**
     1. User accesses the market analysis section.
     2. User utilizes tools like charts, historical data, and predictive analytics.
     3. Platform provides real-time market data and trend analysis.
     4. User analyzes the data to guide their trading strategy.
   - **Extensions:**
     - **3a. Analysis tools unavailable:**
       - **3a1.** Platform notifies the user and provides an estimated time for availability.
