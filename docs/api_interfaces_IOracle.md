---
id: interfaces_IOracle
title: IOracle
---

<div class="contract-doc"><div class="contract"><h2 class="contract-header"><span class="contract-kind">interface</span> IOracle</h2><div class="source">Source: <a href="git+https://github.com/PolymathNetwork/polymath-core/blob/v1.4.0/contracts/interfaces/IOracle.sol" target="_blank">interfaces/IOracle.sol</a></div></div><div class="index"><h2>Index</h2><ul><li><a href="interfaces_IOracle.html#getCurrencyAddress">getCurrencyAddress</a></li><li><a href="interfaces_IOracle.html#getCurrencyDenominated">getCurrencyDenominated</a></li><li><a href="interfaces_IOracle.html#getCurrencySymbol">getCurrencySymbol</a></li><li><a href="interfaces_IOracle.html#getPrice">getPrice</a></li></ul></div><div class="reference"><h2>Reference</h2><div class="functions"><h3>Functions</h3><ul><li><div class="item function"><span id="getCurrencyAddress" class="anchor-marker"></span><h4 class="name">getCurrencyAddress</h4><div class="body"><code class="signature"><span>abstract </span>function <strong>getCurrencyAddress</strong><span>() </span><span>external </span><span>view </span><span>returns  (address) </span></code><hr/><div class="description"><p>Returns address of oracle currency (0x0 for ETH).</p></div><dl><dt><span class="label-return">Returns:</span></dt><dd>address</dd></dl></div></div></li><li><div class="item function"><span id="getCurrencyDenominated" class="anchor-marker"></span><h4 class="name">getCurrencyDenominated</h4><div class="body"><code class="signature"><span>abstract </span>function <strong>getCurrencyDenominated</strong><span>() </span><span>external </span><span>view </span><span>returns  (bytes32) </span></code><hr/><div class="description"><p>Returns denomination of price.</p></div><dl><dt><span class="label-return">Returns:</span></dt><dd>bytes32</dd></dl></div></div></li><li><div class="item function"><span id="getCurrencySymbol" class="anchor-marker"></span><h4 class="name">getCurrencySymbol</h4><div class="body"><code class="signature"><span>abstract </span>function <strong>getCurrencySymbol</strong><span>() </span><span>external </span><span>view </span><span>returns  (bytes32) </span></code><hr/><div class="description"><p>Returns symbol of oracle currency (0x0 for ETH).</p></div><dl><dt><span class="label-return">Returns:</span></dt><dd>bytes32</dd></dl></div></div></li><li><div class="item function"><span id="getPrice" class="anchor-marker"></span><h4 class="name">getPrice</h4><div class="body"><code class="signature"><span>abstract </span>function <strong>getPrice</strong><span>() </span><span>external </span><span>view </span><span>returns  (uint256) </span></code><hr/><div class="description"><p>Returns price - should throw if not valid.</p></div><dl><dt><span class="label-return">Returns:</span></dt><dd>uint256</dd></dl></div></div></li></ul></div></div></div>