---
id: modules_STO_USDTieredSTO
title: USDTieredSTO
---

<div class="contract-doc"><div class="contract"><h2 class="contract-header"><span class="contract-kind">contract</span> USDTieredSTO</h2><p class="base-contracts"><span>is</span> <a href="modules_STO_ISTO.html">ISTO</a><span>, </span><a href="es_openzeppelin-solidity_contracts_ReentrancyGuard.html">ReentrancyGuard</a></p><div class="source">Source: <a href="git+https://github.com/PolymathNetwork/polymath-core/blob/v1.4.0/contracts/modules/STO/USDTieredSTO.sol" target="_blank">modules/STO/USDTieredSTO.sol</a></div></div><div class="index"><h2>Index</h2><ul><li><a href="modules_STO_USDTieredSTO.html#FundsReceivedETH">FundsReceivedETH</a></li><li><a href="modules_STO_USDTieredSTO.html#FundsReceivedPOLY">FundsReceivedPOLY</a></li><li><a href="modules_STO_USDTieredSTO.html#ReserveTokenMint">ReserveTokenMint</a></li><li><a href="modules_STO_USDTieredSTO.html#SetAddresses">SetAddresses</a></li><li><a href="modules_STO_USDTieredSTO.html#SetFunding">SetFunding</a></li><li><a href="modules_STO_USDTieredSTO.html#SetLimits">SetLimits</a></li><li><a href="modules_STO_USDTieredSTO.html#SetTiers">SetTiers</a></li><li><a href="modules_STO_USDTieredSTO.html#SetTimes">SetTimes</a></li><li><a href="modules_STO_USDTieredSTO.html#TokenPurchase">TokenPurchase</a></li><li><a href="modules_STO_USDTieredSTO.html#_buyTokens">_buyTokens</a></li><li><a href="modules_STO_USDTieredSTO.html#_calculateTier">_calculateTier</a></li><li><a href="modules_STO_USDTieredSTO.html#_configureAddresses">_configureAddresses</a></li><li><a href="modules_STO_USDTieredSTO.html#_configureFunding">_configureFunding</a></li><li><a href="modules_STO_USDTieredSTO.html#_configureLimits">_configureLimits</a></li><li><a href="modules_STO_USDTieredSTO.html#_configureTiers">_configureTiers</a></li><li><a href="modules_STO_USDTieredSTO.html#_configureTimes">_configureTimes</a></li><li><a href="modules_STO_USDTieredSTO.html#_purchaseTier">_purchaseTier</a></li><li><a href="modules_STO_USDTieredSTO.html#buyWithETH">buyWithETH</a></li><li><a href="modules_STO_USDTieredSTO.html#buyWithPOLY">buyWithPOLY</a></li><li><a href="modules_STO_USDTieredSTO.html#capReached">capReached</a></li><li><a href="modules_STO_USDTieredSTO.html#changeAccredited">changeAccredited</a></li><li><a href="modules_STO_USDTieredSTO.html#configure">configure</a></li><li><a href="modules_STO_USDTieredSTO.html#convertFromUSD">convertFromUSD</a></li><li><a href="modules_STO_USDTieredSTO.html#convertToUSD">convertToUSD</a></li><li><a href="modules_STO_USDTieredSTO.html#decimalDiv">decimalDiv</a></li><li><a href="modules_STO_USDTieredSTO.html#decimalMul">decimalMul</a></li><li><a href="modules_STO_USDTieredSTO.html#">fallback</a></li><li><a href="modules_STO_USDTieredSTO.html#">fallback</a></li><li><a href="modules_STO_USDTieredSTO.html#finalize">finalize</a></li><li><a href="modules_STO_USDTieredSTO.html#getInitFunction">getInitFunction</a></li><li><a href="modules_STO_USDTieredSTO.html#getNumberInvestors">getNumberInvestors</a></li><li><a href="modules_STO_USDTieredSTO.html#getNumberOfTiers">getNumberOfTiers</a></li><li><a href="modules_STO_USDTieredSTO.html#getOracle">getOracle</a></li><li><a href="modules_STO_USDTieredSTO.html#getPermissions">getPermissions</a></li><li><a href="modules_STO_USDTieredSTO.html#getRaisedEther">getRaisedEther</a></li><li><a href="modules_STO_USDTieredSTO.html#getRaisedPOLY">getRaisedPOLY</a></li><li><a href="modules_STO_USDTieredSTO.html#getRaisedUSD">getRaisedUSD</a></li><li><a href="modules_STO_USDTieredSTO.html#getTokensMinted">getTokensMinted</a></li><li><a href="modules_STO_USDTieredSTO.html#getTokensSold">getTokensSold</a></li><li><a href="modules_STO_USDTieredSTO.html#getTokensSoldForETH">getTokensSoldForETH</a></li><li><a href="modules_STO_USDTieredSTO.html#getTokensSoldForPOLY">getTokensSoldForPOLY</a></li><li><a href="modules_STO_USDTieredSTO.html#isOpen">isOpen</a></li><li><a href="modules_STO_USDTieredSTO.html#modifyAddresses">modifyAddresses</a></li><li><a href="modules_STO_USDTieredSTO.html#modifyFunding">modifyFunding</a></li><li><a href="modules_STO_USDTieredSTO.html#modifyLimits">modifyLimits</a></li><li><a href="modules_STO_USDTieredSTO.html#modifyTiers">modifyTiers</a></li><li><a href="modules_STO_USDTieredSTO.html#modifyTimes">modifyTimes</a></li><li><a href="modules_STO_USDTieredSTO.html#validETH">validETH</a></li><li><a href="modules_STO_USDTieredSTO.html#validPOLY">validPOLY</a></li></ul></div><div class="reference"><h2>Reference</h2><div class="events"><h3>Events</h3><ul><li><div class="item event"><span id="FundsReceivedETH" class="anchor-marker"></span><h4 class="name">FundsReceivedETH</h4><div class="body"><code class="signature">event <strong>FundsReceivedETH</strong><span>(address _purchaser, address _beneficiary, uint256 _usdAmount, uint256 _receivedValue, uint256 _spentValue, uint256 _rate) </span></code><hr/><dl><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>_purchaser</code> - address</div><div><code>_beneficiary</code> - address</div><div><code>_usdAmount</code> - uint256</div><div><code>_receivedValue</code> - uint256</div><div><code>_spentValue</code> - uint256</div><div><code>_rate</code> - uint256</div></dd></dl></div></div></li><li><div class="item event"><span id="FundsReceivedPOLY" class="anchor-marker"></span><h4 class="name">FundsReceivedPOLY</h4><div class="body"><code class="signature">event <strong>FundsReceivedPOLY</strong><span>(address _purchaser, address _beneficiary, uint256 _usdAmount, uint256 _receivedValue, uint256 _spentValue, uint256 _rate) </span></code><hr/><dl><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>_purchaser</code> - address</div><div><code>_beneficiary</code> - address</div><div><code>_usdAmount</code> - uint256</div><div><code>_receivedValue</code> - uint256</div><div><code>_spentValue</code> - uint256</div><div><code>_rate</code> - uint256</div></dd></dl></div></div></li><li><div class="item event"><span id="ReserveTokenMint" class="anchor-marker"></span><h4 class="name">ReserveTokenMint</h4><div class="body"><code class="signature">event <strong>ReserveTokenMint</strong><span>(address _owner, address _wallet, uint256 _tokens, uint8 _tier) </span></code><hr/><dl><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>_owner</code> - address</div><div><code>_wallet</code> - address</div><div><code>_tokens</code> - uint256</div><div><code>_tier</code> - uint8</div></dd></dl></div></div></li><li><div class="item event"><span id="SetAddresses" class="anchor-marker"></span><h4 class="name">SetAddresses</h4><div class="body"><code class="signature">event <strong>SetAddresses</strong><span>(address _wallet, address _reserveWallet) </span></code><hr/><dl><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>_wallet</code> - address</div><div><code>_reserveWallet</code> - address</div></dd></dl></div></div></li><li><div class="item event"><span id="SetFunding" class="anchor-marker"></span><h4 class="name">SetFunding</h4><div class="body"><code class="signature">event <strong>SetFunding</strong><span>(uint8[] _fundRaiseTypes) </span></code><hr/><dl><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>_fundRaiseTypes</code> - uint8[]</div></dd></dl></div></div></li><li><div class="item event"><span id="SetLimits" class="anchor-marker"></span><h4 class="name">SetLimits</h4><div class="body"><code class="signature">event <strong>SetLimits</strong><span>(uint256 _nonAccreditedLimitUSD, uint256 _minimumInvestmentUSD) </span></code><hr/><dl><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>_nonAccreditedLimitUSD</code> - uint256</div><div><code>_minimumInvestmentUSD</code> - uint256</div></dd></dl></div></div></li><li><div class="item event"><span id="SetTiers" class="anchor-marker"></span><h4 class="name">SetTiers</h4><div class="body"><code class="signature">event <strong>SetTiers</strong><span>(uint256[] _ratePerTier, uint256[] _ratePerTierDiscountPoly, uint256[] _tokensPerTierTotal, uint256[] _tokensPerTierDiscountPoly) </span></code><hr/><dl><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>_ratePerTier</code> - uint256[]</div><div><code>_ratePerTierDiscountPoly</code> - uint256[]</div><div><code>_tokensPerTierTotal</code> - uint256[]</div><div><code>_tokensPerTierDiscountPoly</code> - uint256[]</div></dd></dl></div></div></li><li><div class="item event"><span id="SetTimes" class="anchor-marker"></span><h4 class="name">SetTimes</h4><div class="body"><code class="signature">event <strong>SetTimes</strong><span>(uint256 _startTime, uint256 _endTime) </span></code><hr/><dl><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>_startTime</code> - uint256</div><div><code>_endTime</code> - uint256</div></dd></dl></div></div></li><li><div class="item event"><span id="TokenPurchase" class="anchor-marker"></span><h4 class="name">TokenPurchase</h4><div class="body"><code class="signature">event <strong>TokenPurchase</strong><span>(address _purchaser, address _beneficiary, uint256 _tokens, uint256 _usdAmount, uint256 _tierPrice, uint8 _tier) </span></code><hr/><div class="description"><p>/////////.</p></div><dl><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>_purchaser</code> - address</div><div><code>_beneficiary</code> - address</div><div><code>_tokens</code> - uint256</div><div><code>_usdAmount</code> - uint256</div><div><code>_tierPrice</code> - uint256</div><div><code>_tier</code> - uint8</div></dd></dl></div></div></li></ul></div><div class="modifiers"><h3>Modifiers</h3><ul><li><div class="item modifier"><span id="validETH" class="anchor-marker"></span><h4 class="name">validETH</h4><div class="body"><code class="signature">modifier <strong>validETH</strong><span>() </span></code><hr/><div class="description"><p>////////////.</p></div></div></div></li><li><div class="item modifier"><span id="validPOLY" class="anchor-marker"></span><h4 class="name">validPOLY</h4><div class="body"><code class="signature">modifier <strong>validPOLY</strong><span>() </span></code><hr/></div></div></li></ul></div><div class="functions"><h3>Functions</h3><ul><li><div class="item function"><span id="_buyTokens" class="anchor-marker"></span><h4 class="name">_buyTokens</h4><div class="body"><code class="signature">function <strong>_buyTokens</strong><span>(address _beneficiary, uint256 _investmentValue, uint256 _rate, bool _isPOLY) </span><span>internal </span><span>returns  (uint256, uint256) </span></code><hr/><div class="description"><p>Low level token purchase.</p></div><dl><dt><span class="label-modifiers">Modifiers:</span></dt><dd><a href="es_openzeppelin-solidity_contracts_ReentrancyGuard.html#nonReentrant">nonReentrant </a><a href="Pausable.html#whenNotPaused">whenNotPaused </a></dd><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>_beneficiary</code> - Address where security tokens will be sent</div><div><code>_investmentValue</code> - Amount of POLY or ETH invested</div><div><code>_rate</code> - uint256</div><div><code>_isPOLY</code> - Investment method</div></dd><dt><span class="label-return">Returns:</span></dt><dd>uint256</dd><dd>uint256</dd></dl></div></div></li><li><div class="item function"><span id="_calculateTier" class="anchor-marker"></span><h4 class="name">_calculateTier</h4><div class="body"><code class="signature">function <strong>_calculateTier</strong><span>(address _beneficiary, uint8 _tier, uint256 _investedUSD, bool _isPOLY) </span><span>internal </span><span>returns  (uint256) </span></code><hr/><dl><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>_beneficiary</code> - address</div><div><code>_tier</code> - uint8</div><div><code>_investedUSD</code> - uint256</div><div><code>_isPOLY</code> - bool</div></dd><dt><span class="label-return">Returns:</span></dt><dd>uint256</dd></dl></div></div></li><li><div class="item function"><span id="_configureAddresses" class="anchor-marker"></span><h4 class="name">_configureAddresses</h4><div class="body"><code class="signature">function <strong>_configureAddresses</strong><span>(address _wallet, address _reserveWallet) </span><span>internal </span></code><hr/><dl><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>_wallet</code> - address</div><div><code>_reserveWallet</code> - address</div></dd></dl></div></div></li><li><div class="item function"><span id="_configureFunding" class="anchor-marker"></span><h4 class="name">_configureFunding</h4><div class="body"><code class="signature">function <strong>_configureFunding</strong><span>(uint8[] _fundRaiseTypes) </span><span>internal </span></code><hr/><dl><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>_fundRaiseTypes</code> - uint8[]</div></dd></dl></div></div></li><li><div class="item function"><span id="_configureLimits" class="anchor-marker"></span><h4 class="name">_configureLimits</h4><div class="body"><code class="signature">function <strong>_configureLimits</strong><span>(uint256 _nonAccreditedLimitUSD, uint256 _minimumInvestmentUSD) </span><span>internal </span></code><hr/><dl><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>_nonAccreditedLimitUSD</code> - uint256</div><div><code>_minimumInvestmentUSD</code> - uint256</div></dd></dl></div></div></li><li><div class="item function"><span id="_configureTiers" class="anchor-marker"></span><h4 class="name">_configureTiers</h4><div class="body"><code class="signature">function <strong>_configureTiers</strong><span>(uint256[] _ratePerTier, uint256[] _ratePerTierDiscountPoly, uint256[] _tokensPerTierTotal, uint256[] _tokensPerTierDiscountPoly) </span><span>internal </span></code><hr/><dl><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>_ratePerTier</code> - uint256[]</div><div><code>_ratePerTierDiscountPoly</code> - uint256[]</div><div><code>_tokensPerTierTotal</code> - uint256[]</div><div><code>_tokensPerTierDiscountPoly</code> - uint256[]</div></dd></dl></div></div></li><li><div class="item function"><span id="_configureTimes" class="anchor-marker"></span><h4 class="name">_configureTimes</h4><div class="body"><code class="signature">function <strong>_configureTimes</strong><span>(uint256 _startTime, uint256 _endTime) </span><span>internal </span></code><hr/><dl><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>_startTime</code> - uint256</div><div><code>_endTime</code> - uint256</div></dd></dl></div></div></li><li><div class="item function"><span id="_purchaseTier" class="anchor-marker"></span><h4 class="name">_purchaseTier</h4><div class="body"><code class="signature">function <strong>_purchaseTier</strong><span>(address _beneficiary, uint256 _tierPrice, uint256 _tierRemaining, uint256 _investedUSD, uint8 _tier) </span><span>internal </span><span>returns  (uint256, uint256) </span></code><hr/><dl><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>_beneficiary</code> - address</div><div><code>_tierPrice</code> - uint256</div><div><code>_tierRemaining</code> - uint256</div><div><code>_investedUSD</code> - uint256</div><div><code>_tier</code> - uint8</div></dd><dt><span class="label-return">Returns:</span></dt><dd>uint256</dd><dd>uint256</dd></dl></div></div></li><li><div class="item function"><span id="buyWithETH" class="anchor-marker"></span><h4 class="name">buyWithETH</h4><div class="body"><code class="signature">function <strong>buyWithETH</strong><span>(address _beneficiary) </span><span>public </span><span>payable </span></code><hr/><div class="description"><p>Purchase tokens using ETH.</p></div><dl><dt><span class="label-modifiers">Modifiers:</span></dt><dd><a href="modules_STO_USDTieredSTO.html#validETH">validETH </a></dd><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>_beneficiary</code> - Address where security tokens will be sent</div></dd></dl></div></div></li><li><div class="item function"><span id="buyWithPOLY" class="anchor-marker"></span><h4 class="name">buyWithPOLY</h4><div class="body"><code class="signature">function <strong>buyWithPOLY</strong><span>(address _beneficiary, uint256 _investedPOLY) </span><span>public </span></code><hr/><div class="description"><p>Purchase tokens using POLY.</p></div><dl><dt><span class="label-modifiers">Modifiers:</span></dt><dd><a href="modules_STO_USDTieredSTO.html#validPOLY">validPOLY </a></dd><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>_beneficiary</code> - Address where security tokens will be sent</div><div><code>_investedPOLY</code> - Amount of POLY invested</div></dd></dl></div></div></li><li><div class="item function"><span id="capReached" class="anchor-marker"></span><h4 class="name">capReached</h4><div class="body"><code class="signature">function <strong>capReached</strong><span>() </span><span>public </span><span>view </span><span>returns  (bool) </span></code><hr/><div class="description"><p>Checks whether the cap has been reached.</p></div><dl><dt><span class="label-return">Returns:</span></dt><dd>bool Whether the cap was reached</dd></dl></div></div></li><li><div class="item function"><span id="changeAccredited" class="anchor-marker"></span><h4 class="name">changeAccredited</h4><div class="body"><code class="signature">function <strong>changeAccredited</strong><span>(address[] _investors, bool[] _accredited) </span><span>public </span></code><hr/><div class="description"><p>Modify the list of accredited addresses.</p></div><dl><dt><span class="label-modifiers">Modifiers:</span></dt><dd><a href="interfaces_IModule.html#onlyOwner">onlyOwner </a></dd><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>_investors</code> - Array of investor addresses to modify</div><div><code>_accredited</code> - Array of bools specifying accreditation status</div></dd></dl></div></div></li><li><div class="item function"><span id="configure" class="anchor-marker"></span><h4 class="name">configure</h4><div class="body"><code class="signature">function <strong>configure</strong><span>(uint256 _startTime, uint256 _endTime, uint256[] _ratePerTier, uint256[] _ratePerTierDiscountPoly, uint256[] _tokensPerTierTotal, uint256[] _tokensPerTierDiscountPoly, uint256 _nonAccreditedLimitUSD, uint256 _minimumInvestmentUSD, uint8[] _fundRaiseTypes, address _wallet, address _reserveWallet) </span><span>public </span></code><hr/><div class="description"><p>Function used to intialize the contract variables.</p></div><dl><dt><span class="label-modifiers">Modifiers:</span></dt><dd><a href="interfaces_IModule.html#onlyFactory">onlyFactory </a></dd><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>_startTime</code> - Unix timestamp at which offering get started</div><div><code>_endTime</code> - Unix timestamp at which offering get ended</div><div><code>_ratePerTier</code> - Rate (in USD) per tier (* 10**18)</div><div><code>_ratePerTierDiscountPoly</code> - uint256[]</div><div><code>_tokensPerTierTotal</code> - Tokens available in each tier</div><div><code>_tokensPerTierDiscountPoly</code> - uint256[]</div><div><code>_nonAccreditedLimitUSD</code> - Limit in USD (* 10**18) for non-accredited investors</div><div><code>_minimumInvestmentUSD</code> - Minimun investment in USD (* 10**18)</div><div><code>_fundRaiseTypes</code> - Types of currency used to collect the funds</div><div><code>_wallet</code> - Ethereum account address to hold the funds</div><div><code>_reserveWallet</code> - Ethereum account address to receive unsold tokens</div></dd></dl></div></div></li><li><div class="item function"><span id="convertFromUSD" class="anchor-marker"></span><h4 class="name">convertFromUSD</h4><div class="body"><code class="signature">function <strong>convertFromUSD</strong><span>(bytes32 _currency, uint256 _amount) </span><span>public </span><span>view </span><span>returns  (uint256) </span></code><hr/><div class="description"><p>This function converts from USD to ETH or POLY.</p></div><dl><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>_currency</code> - Currency key</div><div><code>_amount</code> - Value to convert from USD</div></dd><dt><span class="label-return">Returns:</span></dt><dd>uint256 Value in ETH or POLY</dd></dl></div></div></li><li><div class="item function"><span id="convertToUSD" class="anchor-marker"></span><h4 class="name">convertToUSD</h4><div class="body"><code class="signature">function <strong>convertToUSD</strong><span>(bytes32 _currency, uint256 _amount) </span><span>public </span><span>view </span><span>returns  (uint256) </span></code><hr/><div class="description"><p>This function converts from ETH or POLY to USD.</p></div><dl><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>_currency</code> - Currency key</div><div><code>_amount</code> - Value to convert to USD</div></dd><dt><span class="label-return">Returns:</span></dt><dd>uint256 Value in USD</dd></dl></div></div></li><li><div class="item function"><span id="decimalDiv" class="anchor-marker"></span><h4 class="name">decimalDiv</h4><div class="body"><code class="signature">function <strong>decimalDiv</strong><span>(uint256 x, uint256 y) </span><span>internal </span><span>pure </span><span>returns  (uint256) </span></code><hr/><div class="description"><p>This function divides two decimals represented as (decimal * 10**DECIMALS).</p></div><dl><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>x</code> - uint256</div><div><code>y</code> - uint256</div></dd><dt><span class="label-return">Returns:</span></dt><dd>uint256 Result of division represented as (decimal * 10**DECIMALS)</dd></dl></div></div></li><li><div class="item function"><span id="decimalMul" class="anchor-marker"></span><h4 class="name">decimalMul</h4><div class="body"><code class="signature">function <strong>decimalMul</strong><span>(uint256 x, uint256 y) </span><span>internal </span><span>pure </span><span>returns  (uint256) </span></code><hr/><div class="description"><p>This function multiplies two decimals represented as (decimal * 10**DECIMALS).</p></div><dl><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>x</code> - uint256</div><div><code>y</code> - uint256</div></dd><dt><span class="label-return">Returns:</span></dt><dd>uint256 Result of multiplication represented as (decimal * 10**DECIMALS)</dd></dl></div></div></li><li><div class="item function"><span id="fallback" class="anchor-marker"></span><h4 class="name">fallback</h4><div class="body"><code class="signature">function <strong></strong><span>() </span><span>external </span><span>payable </span></code><hr/><div class="description"><p>Fallback function - assumes ETH being invested.</p></div></div></div></li><li><div class="item function"><span id="fallback" class="anchor-marker"></span><h4 class="name">fallback</h4><div class="body"><code class="signature">function <strong></strong><span>(address _securityToken, address _polyAddress) </span><span>public </span></code><hr/><div class="description"><p>////////////////////.</p></div><dl><dt><span class="label-modifiers">Modifiers:</span></dt><dd></dd><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>_securityToken</code> - address</div><div><code>_polyAddress</code> - address</div></dd></dl></div></div></li><li><div class="item function"><span id="finalize" class="anchor-marker"></span><h4 class="name">finalize</h4><div class="body"><code class="signature">function <strong>finalize</strong><span>() </span><span>public </span></code><hr/><div class="description"><p>Reserve address must be whitelisted to successfully finalize.</p></div><dl><dt><span class="label-modifiers">Modifiers:</span></dt><dd><a href="interfaces_IModule.html#onlyOwner">onlyOwner </a></dd></dl></div></div></li><li><div class="item function"><span id="getInitFunction" class="anchor-marker"></span><h4 class="name">getInitFunction</h4><div class="body"><code class="signature">function <strong>getInitFunction</strong><span>() </span><span>public </span><span>pure </span><span>returns  (bytes4) </span></code><hr/><div class="description"><p>This function returns the signature of configure function.</p></div><dl><dt><span class="label-return">Returns:</span></dt><dd>bytes4 Configure function signature</dd></dl></div></div></li><li><div class="item function"><span id="getNumberInvestors" class="anchor-marker"></span><h4 class="name">getNumberInvestors</h4><div class="body"><code class="signature">function <strong>getNumberInvestors</strong><span>() </span><span>public </span><span>view </span><span>returns  (uint256) </span></code><hr/><div class="description"><p>Return the total no. of investors.</p></div><dl><dt><span class="label-return">Returns:</span></dt><dd>uint256 Investor count</dd></dl></div></div></li><li><div class="item function"><span id="getNumberOfTiers" class="anchor-marker"></span><h4 class="name">getNumberOfTiers</h4><div class="body"><code class="signature">function <strong>getNumberOfTiers</strong><span>() </span><span>public </span><span>view </span><span>returns  (uint256) </span></code><hr/><div class="description"><p>Return the total no. of tiers.</p></div><dl><dt><span class="label-return">Returns:</span></dt><dd>uint256 Total number of tiers</dd></dl></div></div></li><li><div class="item function"><span id="getOracle" class="anchor-marker"></span><h4 class="name">getOracle</h4><div class="body"><code class="signature">function <strong>getOracle</strong><span>(bytes32 _currency, bytes32 _denominatedCurrency) </span><span>internal </span><span>view </span><span>returns  (address) </span></code><hr/><dl><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>_currency</code> - bytes32</div><div><code>_denominatedCurrency</code> - bytes32</div></dd><dt><span class="label-return">Returns:</span></dt><dd>address</dd></dl></div></div></li><li><div class="item function"><span id="getPermissions" class="anchor-marker"></span><h4 class="name">getPermissions</h4><div class="body"><code class="signature">function <strong>getPermissions</strong><span>() </span><span>public </span><span>view </span><span>returns  (bytes32[]) </span></code><hr/><div class="description"><p>Return the permissions flag that are associated with STO.</p></div><dl><dt><span class="label-return">Returns:</span></dt><dd>bytes32[]</dd></dl></div></div></li><li><div class="item function"><span id="getRaisedEther" class="anchor-marker"></span><h4 class="name">getRaisedEther</h4><div class="body"><code class="signature">function <strong>getRaisedEther</strong><span>() </span><span>public </span><span>view </span><span>returns  (uint256) </span></code><hr/><div class="description"><p>Return ETH raised by the STO.</p></div><dl><dt><span class="label-return">Returns:</span></dt><dd>uint256 Amount of ETH raised</dd></dl></div></div></li><li><div class="item function"><span id="getRaisedPOLY" class="anchor-marker"></span><h4 class="name">getRaisedPOLY</h4><div class="body"><code class="signature">function <strong>getRaisedPOLY</strong><span>() </span><span>public </span><span>view </span><span>returns  (uint256) </span></code><hr/><div class="description"><p>Return POLY raised by the STO.</p></div><dl><dt><span class="label-return">Returns:</span></dt><dd>uint256 Amount of POLY raised</dd></dl></div></div></li><li><div class="item function"><span id="getRaisedUSD" class="anchor-marker"></span><h4 class="name">getRaisedUSD</h4><div class="body"><code class="signature">function <strong>getRaisedUSD</strong><span>() </span><span>public </span><span>view </span><span>returns  (uint256) </span></code><hr/><div class="description"><p>Return USD raised by the STO.</p></div><dl><dt><span class="label-return">Returns:</span></dt><dd>uint256 Amount of USD raised</dd></dl></div></div></li><li><div class="item function"><span id="getTokensMinted" class="anchor-marker"></span><h4 class="name">getTokensMinted</h4><div class="body"><code class="signature">function <strong>getTokensMinted</strong><span>() </span><span>public </span><span>view </span><span>returns  (uint256) </span></code><hr/><div class="description"><p>Return the total no. of tokens minted.</p></div><dl><dt><span class="label-return">Returns:</span></dt><dd>uint256 Total number of tokens minted</dd></dl></div></div></li><li><div class="item function"><span id="getTokensSold" class="anchor-marker"></span><h4 class="name">getTokensSold</h4><div class="body"><code class="signature">function <strong>getTokensSold</strong><span>() </span><span>public </span><span>view </span><span>returns  (uint256) </span></code><hr/><div class="description"><p>Return the total no. of tokens sold.</p></div><dl><dt><span class="label-return">Returns:</span></dt><dd>uint256 Total number of tokens sold</dd></dl></div></div></li><li><div class="item function"><span id="getTokensSoldForETH" class="anchor-marker"></span><h4 class="name">getTokensSoldForETH</h4><div class="body"><code class="signature">function <strong>getTokensSoldForETH</strong><span>() </span><span>public </span><span>view </span><span>returns  (uint256) </span></code><hr/><div class="description"><p>Return the total no. of tokens sold for ETH.</p></div><dl><dt><span class="label-return">Returns:</span></dt><dd>uint256 Total number of tokens sold for ETH</dd></dl></div></div></li><li><div class="item function"><span id="getTokensSoldForPOLY" class="anchor-marker"></span><h4 class="name">getTokensSoldForPOLY</h4><div class="body"><code class="signature">function <strong>getTokensSoldForPOLY</strong><span>() </span><span>public </span><span>view </span><span>returns  (uint256) </span></code><hr/><div class="description"><p>Return the total no. of tokens sold for POLY.</p></div><dl><dt><span class="label-return">Returns:</span></dt><dd>uint256 Total number of tokens sold for POLY</dd></dl></div></div></li><li><div class="item function"><span id="isOpen" class="anchor-marker"></span><h4 class="name">isOpen</h4><div class="body"><code class="signature">function <strong>isOpen</strong><span>() </span><span>public </span><span>view </span><span>returns  (bool) </span></code><hr/><div class="description"><p>This function returns whether or not the STO is in fundraising mode (open).</p></div><dl><dt><span class="label-return">Returns:</span></dt><dd>bool Whether the STO is accepting investments</dd></dl></div></div></li><li><div class="item function"><span id="modifyAddresses" class="anchor-marker"></span><h4 class="name">modifyAddresses</h4><div class="body"><code class="signature">function <strong>modifyAddresses</strong><span>(address _wallet, address _reserveWallet) </span><span>public </span></code><hr/><dl><dt><span class="label-modifiers">Modifiers:</span></dt><dd><a href="interfaces_IModule.html#onlyOwner">onlyOwner </a></dd><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>_wallet</code> - address</div><div><code>_reserveWallet</code> - address</div></dd></dl></div></div></li><li><div class="item function"><span id="modifyFunding" class="anchor-marker"></span><h4 class="name">modifyFunding</h4><div class="body"><code class="signature">function <strong>modifyFunding</strong><span>(uint8[] _fundRaiseTypes) </span><span>public </span></code><hr/><dl><dt><span class="label-modifiers">Modifiers:</span></dt><dd><a href="interfaces_IModule.html#onlyOwner">onlyOwner </a></dd><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>_fundRaiseTypes</code> - uint8[]</div></dd></dl></div></div></li><li><div class="item function"><span id="modifyLimits" class="anchor-marker"></span><h4 class="name">modifyLimits</h4><div class="body"><code class="signature">function <strong>modifyLimits</strong><span>(uint256 _nonAccreditedLimitUSD, uint256 _minimumInvestmentUSD) </span><span>public </span></code><hr/><dl><dt><span class="label-modifiers">Modifiers:</span></dt><dd><a href="interfaces_IModule.html#onlyOwner">onlyOwner </a></dd><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>_nonAccreditedLimitUSD</code> - uint256</div><div><code>_minimumInvestmentUSD</code> - uint256</div></dd></dl></div></div></li><li><div class="item function"><span id="modifyTiers" class="anchor-marker"></span><h4 class="name">modifyTiers</h4><div class="body"><code class="signature">function <strong>modifyTiers</strong><span>(uint256[] _ratePerTier, uint256[] _ratePerTierDiscountPoly, uint256[] _tokensPerTierTotal, uint256[] _tokensPerTierDiscountPoly) </span><span>public </span></code><hr/><dl><dt><span class="label-modifiers">Modifiers:</span></dt><dd><a href="interfaces_IModule.html#onlyOwner">onlyOwner </a></dd><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>_ratePerTier</code> - uint256[]</div><div><code>_ratePerTierDiscountPoly</code> - uint256[]</div><div><code>_tokensPerTierTotal</code> - uint256[]</div><div><code>_tokensPerTierDiscountPoly</code> - uint256[]</div></dd></dl></div></div></li><li><div class="item function"><span id="modifyTimes" class="anchor-marker"></span><h4 class="name">modifyTimes</h4><div class="body"><code class="signature">function <strong>modifyTimes</strong><span>(uint256 _startTime, uint256 _endTime) </span><span>public </span></code><hr/><dl><dt><span class="label-modifiers">Modifiers:</span></dt><dd><a href="interfaces_IModule.html#onlyOwner">onlyOwner </a></dd><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>_startTime</code> - uint256</div><div><code>_endTime</code> - uint256</div></dd></dl></div></div></li></ul></div></div></div>