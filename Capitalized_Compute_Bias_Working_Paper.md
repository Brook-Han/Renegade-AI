# Capitalized Compute Bias: Institutional Misallocation and the Macroeconomic Realignment of Generative AI

**Author:** Brooks Han, Assistant Professor, The Hong Kong University of Science and Technology (HKUST)

**Project Affiliation:** *Renegade AI: Catalyst for Human Cognitive Evolution*

**Classification:** Working Paper / Policy Essay

**Target Tracks:** Institutional Economics; Innovation Policy; Industrial Organization

---

## Abstract & Executive Summary

This paper investigates a structural anomaly in the political economy of artificial intelligence: the systematic misallocation of capital toward physical computational infrastructure at the expense of intangible algorithmic and human capital. We conceptualize this phenomenon as **Capitalized Compute Bias**—a triple institutional convergence of financial accounting standards, corporate governance architectures, and capital market signaling mechanisms that collectively favor tangible fixed-asset accumulation over intangible intellective investment. [¹](#fn-cbb)

We argue that the current generative AI trajectory is characterized by an asymmetric value capture regime in which upstream hardware incumbents extract structural rents, while downstream foundation model developers and enterprise adopters face persistent financial deficits and negative returns on investment. Rather than a simple market bubble, this misallocation is actively produced and reinforced by the institutional architecture of modern financial capitalism. We model the transition from brute-force hardware scaling to an efficiency-driven paradigm, outlining three scenarios for macroeconomic realignment across 2026–2027, and conclude that competitive advantage in AI will shift from the accumulation of computational assets toward the organizational capacity to coordinate algorithmic efficiency, engineering optimization, and domain knowledge as integrated production factors.

---

## 01. Introduction

Every major technological paradigm shift historically experiences a phase of structural capital misallocation, in which the institutional logic of a prior economic era is retrofitted onto a nascent mode of production. During the late-1990s telecommunications boom, financial capital relied on industrial-era logics to over-allocate resources toward physical fiber-optic networks under the assumption of infinite linear demand—precipitating a protracted structural adjustment once the bandwidth surplus became undeniable.

A distortion of comparable structural depth, though different in mechanism, is currently unfolding within generative AI. The global technology sector is locked in an institutional consensus that treats physical compute infrastructure as the singular, deterministic driver of cognitive capability. This has produced an unprecedented concentration of capital expenditures in graphics processing units (GPUs), high-bandwidth memory (HBM), and hyperscale data centers. In FY2025, the four largest hyperscale cloud operators—Microsoft, Amazon, Alphabet, and Meta—collectively deployed over $400 billion in capital expenditures, with more than 70% directed toward AI compute infrastructure.¹ NVIDIA alone reported $130.5 billion in revenue, $72.9 billion in net income, and a 75% gross margin.²

Yet downstream, the picture inverts. OpenAI—the sector's highest-revenue foundation model developer—reported $13.07 billion in FY2025 revenue against an estimated $8–9 billion operating loss.³ Anthropic, its closest competitor, generated approximately $2.2 billion in annual revenue, with an end-of-year annualized run rate of ~$9 billion, while remaining deeply unprofitable.⁴ At the enterprise terminus, PwC's 29th Annual Global CEO Survey (4,454 CEOs across 95 countries) reports that 56% of CEOs have seen no revenue gains from AI investment; a parallel Deloitte survey of 1,854 executives finds that only 6% achieved measurable AI returns within one year, and merely 5% have realized scaled, measurable business value.⁵

This paper argues that the divergence between upstream hardware profitability and downstream value realization is not a transient market inefficiency. It is the product of a systematic institutional bias. We identify three mutually reinforcing mechanisms—accounting asymmetry, governance arbitrage, and capital market metric preferences—that collectively produce *Capitalized Compute Bias*. The argument proceeds as follows. Section 02 maps the asymmetric value capture structure across four layers of the AI value chain and presents the empirical evidence. Section 03 diagnoses the tripartite institutional driver. Section 04 provides a conceptual framework for understanding why algorithmic efficiency exhibits super-linear compounding effects that capital markets systematically underprice. Section 05 models three macroeconomic realignment scenarios for 2026–2027. Section 06 concludes with the broader institutional and policy implications.

---

## 01.5 Positioning within Existing Literature

This paper engages with three distinct but converging research traditions.

**Intangible Capital and the Measurement Gap.** Haskel & Westlake (2018) demonstrated that modern economies systematically underinvest in intangible assets—R&D, software, organizational capital, and human competencies—due in part to accounting conventions that treat such investments as current expenses rather than capital formation.⁶ Our argument extends this framework into the specific domain of AI infrastructure, where the CapEx/OpEx asymmetry identified by Haskel & Westlake produces not merely measurement error but a structural misallocation bias with macroeconomic consequences. Where Haskel & Westlake diagnose the accounting problem, we trace its downstream effects on an entire global value chain.

**General Purpose Technologies and Investment Cycles.** Bresnahan & Trajtenberg (1995) and subsequent GPT literature establish that transformative technologies exhibit a characteristic "productivity paradox" in which initial capital over-investment in enabling infrastructure precedes the realization of application-layer value.⁷ Our analysis contributes to this tradition by identifying the specific institutional mechanisms—beyond generic market exuberance—that drive overshoot in the infrastructure phase. The compute over-investment we document is not simply a GPT cycle artifact; it is actively incentivized by accounting standards, governance structures, and capital market valuation models.

**Automation, Factor Shares, and Institutional Economics.** Acemoglu & Restrepo (2019) model the displacement and reinstatement effects of automation on labor, demonstrating that the net productivity impact depends critically on the institutional framework governing technology adoption.⁸ We extend this institutional logic to the factor share between tangible compute capital and intangible algorithmic/human capital. Where Acemoglu & Restrepo focus on labor-capital substitution, we analyze a parallel but distinct phenomenon: the substitution of tangible capital for intangible capital within the technology production function itself—a form of *factor misallocation* that is institutionally produced rather than market-driven.

Our contribution to these intersecting literatures is twofold. First, we provide a granular empirical mapping of asymmetric value capture across the AI value chain that has not been systematically documented in the institutional economics literature. Second, we propose a conceptual framework—*Capitalized Compute Bias*—that identifies the specific institutional transmission mechanisms linking accounting rules, governance incentives, and capital market behavior to macroeconomic misallocation outcomes.

**Positioning relative to recent INET research.** A recent INET working paper by Storm (2026) provides a compelling diagnosis of the AI investment cycle as a speculative bubble, documenting the gap between industry predictions and empirical outcomes.¹⁴ Our analysis complements and extends Storm's contribution by addressing a different question. Where Storm demonstrates *that* the bubble exists—tracing the implausibility of AI industry claims and the negative macroeconomic ROI—we investigate *why* such misallocation is institutionally produced and sustained even in the absence of speculative euphoria. Storm's framework is diagnostic; ours is etiological. The Capitalized Compute Bias operates as a structural mechanism that would distort capital allocation toward tangible compute assets even if AI technology delivers genuine productivity gains, because the bias is embedded in accounting standards, governance architectures, and capital market valuation models that are invariant to the actual technical merits of any given AI investment.

This framework is not limited to AI; it extends to any intangible-capital-intensive sector facing analogous institutional asymmetries—biotechnology, quantum computing, and advanced robotics all operate under the same CapEx/OpEx architecture that structurally favors physical assets over intellective investment.

---

## 02. Asymmetric Value Capture and Value Chain Distortion

To understand the systemic risk of Capitalized Compute Bias, the generative AI industrial structure must be analyzed through the lens of asymmetric value distribution across four distinct layers.

```
[Upstream: Hardware Incumbents]   →  Structural Rent Extraction (70%+ Gross Margins)
              ↓
[Midstream: Foundation Models]     →  Structural Deficits & Capital Injection Dependencies
              ↓
[Downstream: Cloud/Hyperscalers]   →  Low Asset Utilization & Negative ROI Trajectories
              ↓
[Terminal: Enterprise Adoption]    →  Marginal Productivity Gains & Persistent TCO Barriers
```

### 2.1 Upstream: Hardware Dominance and Value Concentration

The incremental profits of the generative AI revolution are overwhelmingly captured by upstream hardware and semiconductor components.

**Semiconductor Architecture.** Upstream market leaders have established a position of structural pricing power by combining advanced microarchitecture with high-switching-cost software ecosystems (e.g., CUDA). NVIDIA's data center segment alone generated $115.2 billion in FY2025 revenue, with company-wide gross margins sustained at 75%.² This pricing architecture allows upstream incumbents to extract a disproportionate share of the global AI capital pool.

**Memory Subsystems (HBM).** The structural demand for specialized memory architectures has distorted broader semiconductor cycles. The pricing premium of HBM over standard DDR5 memory stands at an approximate fivefold multiple.⁹ To capture these high-margin rents, leading memory manufacturers have aggressively reallocated wafer capacity to AI-bound architectures. Micron Technology reported HBM revenue of approximately $2 billion in a single quarter (Q4 FY2025), with its cloud memory business segment—which includes HBM—achieving a 59% gross margin, substantially above the company's 45.7% consolidated margin.¹⁰ This capacity reallocation has induced supply constraints and crowding-out effects in consumer-facing technology sectors.

### 2.2 Midstream: Foundation Models in Structural Deficit

In stark contrast to upstream profitability, foundation model developers operate within a structural deficit regime. Despite multi-hundred-billion-dollar valuations, frontier model entities remain trapped in an unsustainable cycle of continuous capitalization to fund infrastructure maintenance.

**Financial Data.** OpenAI's FY2025 revenue of $13.07 billion—a dramatic increase from $3.7 billion in FY2024—was accompanied by an estimated $8–9 billion operating loss, driven primarily by $19.18 billion in R&D expenditure (of which $10.59 billion was directed to Microsoft for compute infrastructure).³ The company has stated it does not expect profitability before approximately 2030. Anthropic's FY2025 annual revenue of approximately $2.2 billion, with an end-of-year annualized run rate of $9 billion, similarly represents a trajectory of explosive top-line growth that remains structurally unprofitable.⁴

**Inference Commoditization.** The structural economics of the midstream are further compromised by intense price degradation. Epoch AI's tracking data indicates that the cost of GPT-4-equivalent inference performance declined at approximately 40× per year from 2024 to 2025, with mainstream API pricing dropping roughly 80% over the same period.¹¹ The rapid commoditization of inference services has compressed margins, ensuring that market expansion yields expanding deficits rather than economies of scale—a condition we term *deficit-locked growth*.

### 2.3 Downstream: Cloud Infrastructure and Capacity Underutilization

Hyperscale cloud providers serve as the primary financing vehicle for upstream hardware procurement, yet their capital deployment exhibits a stark decoupling from actual demand.

**Capital Expenditure Trajectory.** Combined AI-related CapEx across the four largest hyperscalers exceeded $400 billion in FY2025, with individual firm guidance indicating acceleration: Amazon has projected approximately $200 billion for FY2026 alone, while Alphabet has guided toward $175–185 billion.¹

**Underutilization Metrics.** Cross-sectional industry data reveals that the global average *effective* capacity utilization rate of specialized AI clusters—measured as the proportion of available floating-point operations actually deployed in productive inference or training workloads—sits between 30% and 50% for hyperscale operators, and drops below 30% for localized or sovereign compute centers.¹² This means that a substantial proportion of installed AI hardware is either idle or operating well below design capacity, generating depreciation charges without producing economic output.

The hyper-accumulation of hardware is driven less by current operational demand than by strategic asset hoarding, competitive defense, and capital market signaling. The resulting balance sheets are heavily weighted with rapidly depreciating fixed assets that threaten long-term free cash flow health.

### 2.4 Terminal Enterprise: The Total Cost of Ownership Barrier

At the terminal end of the value chain, enterprise adoption has failed to generate systemic macroeconomic productivity gains.

**Adoption vs. ROI.** While 85% of enterprises report increasing AI investment over the past twelve months and 91% plan further increases, only 6% have achieved measurable AI returns within a one-year horizon.⁵ Current enterprise deployment predominantly occupies marginal, non-core efficiency use cases—customer service response acceleration, administrative draft assistance—that fail to alter the fundamental cost structure of the firm.

**The Substitution Fallacy.** For the vast majority of standard operational workflows, the fully loaded total cost of ownership (TCO) of deploying, fine-tuning, maintaining, and human-auditing frontier AI systems exceeds the marginal cost of traditional labor at current price points. Enterprise AI adoption frequently represents an asset-type substitution—shifting variable labor costs to fixed technical debt—without altering the net productivity frontier. The system-level efficiency gain has yet to materialize at macroeconomic scale.

---

## 03. The Tripartite Institutional Driver

The persistent systemic bias toward hardware over-accumulation is not a product of cognitive deficit among technology executives. It is actively incentivized by three deeply embedded structural mechanisms in contemporary corporate governance and accounting frameworks.

```
+-------------------------------------------------------------------------+
|                       CAPITALIZED COMPUTE BIAS                          |
+-------------------------------------------------------------------------+
                                     |
         +---------------------------+---------------------------+
         |                           |                           |
         v                           v                           v
[Accounting Asymmetry]      [Governance Arbitrage]     [Capital Market Signaling]
   CapEx vs OpEx rules         Managerial risk-hedging    Linear, auditable metrics
   Tangible asset bias         via hardware accumulation  Quantifiable asset bases
```

### 3.1 Accounting Standard Asymmetry

Under current US GAAP and IFRS regimes, the financial treatment of technological inputs is deeply asymmetric.

**Tangible Capitalization (CapEx).** Procurement of physical hardware—GPUs, servers, data center facilities—is classified as Capital Expenditure. Under ASC 350-40 and IAS 38, these investments are recognized as balance sheet assets and depreciated over a multi-year horizon, thereby smoothing the short-term impact on net income and enhancing perceived corporate asset density.¹³

**Intangible Expensing (OpEx).** Conversely, structural investments in high-skilled human capital, algorithmic optimization, and foundational architectural research are categorized under Operating Expenses. Under prevailing accounting standards, internally generated intangible assets arising from R&D activities generally do not meet the recognition criteria for capitalization and must be expensed immediately within the current fiscal period, directly depressing quarterly operating income.¹³

Consequently, modern accounting architectures structurally penalize long-term intellectual and architectural exploration while systematically incentivizing corporate entities to deploy capital into physical, depreciable asset bases. A dollar invested in GPUs improves the balance sheet; a dollar invested in algorithmic architecture erodes current-period earnings.

### 3.2 Managerial Risk-Hedging through Asset Accumulation

Within listed technology firms, the structural separation of ownership and control creates powerful incentives for management to prefer hardware accumulation over algorithmic innovation.

**The Auditability of Capital.** Hardware procurement is a highly auditable, standardized corporate action. It requires low localized technical domain expertise from corporate boards and can be benchmarked against industry peers using publicly reported CapEx metrics. In contrast, investments in algorithmic architecture and research talent require specialized technical judgment that boards typically lack.

**The Strategic Function of Compute Scarcity.** If an enterprise's AI strategy fails despite acquiring a 100,000-GPU cluster, management can attribute the failure to exogenous factors—"our models would have succeeded with sufficient compute scale." The hypothesis is unfalsifiable within any reasonable timeframe, making it an effective strategic hedge for decision-makers. If management stakes corporate survival on an unproven, uncertain algorithmic paradigm shift and fails, the responsibility falls squarely on the decision-maker. Thus, hoarding physical compute serves as a rational risk-mitigation strategy for corporate managers operating under asymmetric information and career risk.

### 3.3 Capital Market Preference for Quantifiable Metrics

In modern venture and public equity markets, valuation models demand linear, predictable scaling metrics. "Total GPU count under management" has become an easily financialized proxy for technological capability. Human capital is fluid and difficult to hedge; algorithmic breakthroughs are stochastic and unpredictable. Physical hardware, by contrast, provides public and private market allocators with a tangible asset anchor around which to construct financial narratives. This directly leads to an over-valuation of compute-dense entities over efficiency-dense organizations, creating a self-reinforcing cycle in which capital flows reward the accumulation of physical assets rather than the development of algorithmic and organizational capabilities.

These three mechanisms—accounting asymmetry, managerial risk-hedging, and capital market metric preferences—operate as a self-reinforcing institutional system. Each individually produces a bias toward hardware; together, they constitute a structural regime that systematically channels capital away from the intangible intellective investments that the AI production function most requires.

---

## 04. Conceptual Framework: The Super-Linear Contribution of Algorithmic Efficiency

The foundational error of the current investment cycle rests on an epistemic conflation: treating the linear expansion of computational inputs as a deterministic proxy for linear progression in cognitive capability. To clarify the structural dynamics governing realized AI economic value, we propose the following conceptual production function:

$$V_{AI} = \Phi \cdot C \cdot (E \cdot H)^\alpha, \quad \text{where } \alpha > 1$$

Where:

* $V_{AI}$: realized economic or operational utility of the AI system.
* $C$: quantitative index of physical computational assets (Compute).
* $E$: algorithmic efficiency index (Architecture, Routing, Quantization).
* $H$: density of high-skilled human capital (Architectural Innovation).
* $\Phi$: exogenous structural integration constant.

In this framework, physical compute ($C$) enters the production function as a linear multiplier, bound by the rigidities of hardware manufacturing cycles, energy constraints, and capital scarcity. Conversely, the interactive variables of algorithmic architecture ($E$) and human intellectual capital ($H$) scale super-linearly ($\alpha > 1$): improvements in algorithmic efficiency exhibit compounding effects that geometric expansions in raw compute cannot replicate at equivalent cost.

**Empirical Illustration.** The rapid deployment and cost deflation enabled by Mixture-of-Experts (MoE) architectures and advanced KV-caching techniques in 2025–2026 already demonstrate this multiplier effect. These algorithmic advances have unlocked multiples of equivalent compute capacity without proportional expansion of physical asset bases. MoE routing, for instance, enables frontier models to activate only a fraction of total parameters per inference, decoupling computational cost from model scale. Yet capital markets have largely failed to price this structural shift, continuing to value compute-dense entities at premiums that the production function itself does not support.

The systemic misallocation occurs precisely because capital allocators treat $C$ as the exponential driver, whereas the trajectory of cost deflation through 2025–2026 demonstrates that algorithmic engineering ($E$) acts as the true lever of compounding returns. The implication is not that compute becomes irrelevant—$C$ retains its role as a necessary multiplier—but that value creation in AI is increasingly determined by the super-linear contribution of the efficiency variables that capital markets structurally underprice.

---

## 05. Structural Realignment: Three Scenarios for 2026–2027

As the divergence between capital expenditure expansion and actual enterprise ROI approaches an unsustainable threshold, the generative AI ecosystem will undergo a structural realignment. We map this transition across three macroeconomic scenarios.

### Scenario 1: Non-Disruptive Equilibrium Absorption (Base Case)

**Mechanisms.** Downstream enterprise monetization accelerates gradually as specialized agentic workflows mature. Hyperscalers smoothly modulate their procurement trajectories from speculative hoarding to just-in-time capacity matching, prioritizing the optimization of existing infrastructure over raw hardware expansion.

**Asset Adjustments.** Upstream component pricing and gross margins experience orderly mean reversion from peak levels toward sustainable historical averages. Capital allocation naturally recalibrates toward middleware engineering, architectural efficiency, and localized fine-tuning frameworks.

**Outcome.** Hardware profitability returns to a high-barrier but margin-normalized equilibrium. The value pool begins a gradual migration toward algorithmic platforms and vertically integrated domain applications.

### Scenario 2: Secular Institutional Correction (Probable Case)

**Mechanisms.** Persistent underperformance in enterprise ROI obliges public market investors to demand capital expenditure discipline. Hyperscale cloud operators explicitly downgrade their forward infrastructure CapEx guidance, triggering a narrative shift from "compute is always scarce" to "compute is abundant when efficiently utilized."

**Asset Adjustments.** Upstream hardware developers face significant valuation adjustments as demand curves flatten. The structural narrative of permanent compute scarcity dissolves. Upstream memory manufacturers, facing capacity oversupply in premium HBM lines, are forced to rapidly reprosecute their production strategies, resulting in painful write-downs of specialized packaging infrastructure and delayed re-entry into legacy consumer storage markets.

**Outcome.** Hardware profitability contracts toward normalized industrial margins. The profit pool begins systematic migration toward algorithmic platforms, efficiency tooling, and vertically integrated applications. Model-layer consolidation accelerates.

### Scenario 3: Abrupt Structural Liquidation (Systemic Risk Case)

**Mechanisms.** A broader macroeconomic tightening coincides with a high-profile credit contraction or delayed IPO among prominent midstream developers, triggering an abrupt collapse in narrative consensus. The "compute scarcity" thesis unravels simultaneously across capital markets.

**Asset Adjustments.** Hyperscalers and secondary compute-leasing entities aggressively halt procurement pipelines and enact severe asset impairment charges on existing hardware inventories. The highly leveraged upstream component supply chain experiences a synchronized compression of both multiples and earnings, forcing rapid, chaotic restructuring of global technology capital allocation back toward software-driven efficiency regimes.

**Outcome.** A concentrated but rapid correction that resets profit structures across the value chain. The subsequent recovery is led by efficiency-focused platforms and domain application developers rather than hardware incumbents.

Across all three scenarios, the directional conclusion is invariant: AI competitive advantage migrates from the scale of physical compute holdings toward the quality of algorithmic architecture, the depth of domain integration, and the organizational capacity to coordinate these factors as an integrated production system.

---

## 06. Conclusion: From Machine Procurement to the Organization of Intelligence

The history of technological evolution indicates that productivity revolutions are structurally bifurcated into two distinct epochs: an initial phase characterized by the crude, capital-intensive accumulation of physical apparatus, followed by a mature phase defined by the sophisticated institutional organization of knowledge.

In the industrial revolution, early capital focused on the competitive over-production of steam engines; the true economic transformation materialized only when organizational innovations integrated those engines into rationalized factory workflows. The internet infrastructure era followed an identical arc: the premature capital frenzy for physical fiber-optic deployments initially destroyed massive equity value, yet it laid the low-marginal-cost baseline from which subsequent software and platform architecture regimes redefined the modern digital economy.

The contemporary generative AI ecosystem is currently transitioning out of its primitive infrastructure accumulation phase. The era in which raw computational scale serves as an effective barrier to entry is drawing to a close. As Capitalized Compute Bias undergoes its necessary macroeconomic correction, competitive advantage will shift from the owners of physical silicon toward the architects of algorithmic efficiency and the organizations capable of embedding deep domain knowledge into coherent software architectures.

The policy and institutional implications extend beyond AI. Any sector in which intangible capital constitutes the primary production factor—biotechnology, quantum computing, advanced robotics—faces analogous institutional asymmetries. Accounting standards designed for industrial-era tangible-asset economies, governance mechanisms optimized for auditable capital deployment, and capital market valuation models dependent on linear, physical metrics collectively constitute an institutional architecture that systematically misprices the most important production factors of the twenty-first century. The correction of Capitalized Compute Bias in AI may thus serve as a template for a broader institutional recalibration: from an economy organized around the accumulation of physical assets to one organized around the capacity to coordinate intangible intelligence as a productive force.

The next stage of the AI economy will therefore be defined not by the accumulation of computational assets, but by the institutional capacity to organize intelligence as a coordinated production factor.

While the empirical focus of this paper is the US-dominated generative AI value chain—operating under US GAAP, US equity market structures, and US corporate governance norms—the Capitalized Compute Bias framework extends to other institutional contexts. Under IFRS, the same CapEx/OpEx asymmetry applies, though the specific capitalization thresholds and R&D recognition criteria differ. In state-directed economies where AI infrastructure investment is driven by industrial policy rather than equity market signals, the bias may manifest through different channels—public investment criteria favoring visible, auditable hardware deployments over intangible R&D programs—but the underlying institutional logic remains structurally analogous. A full comparative institutional analysis across regulatory regimes would constitute a natural extension of this research.

---

## 07. Policy Implications

The Capitalized Compute Bias is not a market failure in the conventional sense—it is an *institutional product*. Correcting it therefore requires institutional reform, not merely improved market information. We identify three policy domains where targeted interventions could recalibrate the institutional incentives driving compute over-accumulation.

### 7.1 Accounting Standards Reform

The current accounting treatment of AI-related intellectual investment creates a structural distortion that no amount of market transparency can overcome. Under US GAAP (ASC 350-40 / ASC 985-20) and IFRS (IAS 38), internally generated intangible assets arising from R&D activities must generally be expensed as incurred, while physical compute hardware qualifies for multi-year capitalization and depreciation.¹³

A targeted reform agenda would include:
- **Selective capitalization of AI R&D.** Where algorithmic architecture development meets defined criteria of technical feasibility, identifiable future economic benefit, and measurable cost attribution, accounting standards should permit—or require—capitalization treatment comparable to that afforded to internally developed software.
- **Mandatory disaggregation of AI CapEx.** Financial reporting standards should require firms to separately disclose AI-specific capital expenditures and their associated depreciation schedules, enabling investors and regulators to distinguish between productive capacity expansion and speculative hardware accumulation.
- **AI asset impairment triggers.** Given the rapid pace of algorithmic efficiency improvements and hardware obsolescence, standard depreciation schedules (typically 4–6 years for data center equipment) may systematically overstate the economic life of AI compute assets. Accelerated impairment testing requirements for AI-specific hardware would better align book values with economic reality.

These reforms would not eliminate the bias toward tangible compute—physical assets will always be easier to value and audit than intangible ones—but they would narrow the institutional asymmetry that currently channels capital away from the algorithmic and human investments that the AI production function most requires.

### 7.2 Capital Market Disclosure and Valuation Discipline

The financialization of "GPU count" as a proxy for technological capability has created a self-reinforcing cycle in which capital flows reward the accumulation of physical assets rather than the development of algorithmic and organizational capabilities. Regulatory interventions could include:

- **Standardized AI efficiency metrics.** Securities regulators should require AI-intensive firms to disclose standardized metrics of compute utilization, inference efficiency, and unit economics (e.g., revenue per petaflop-hour, cost per million tokens served), enabling investors to evaluate capital allocation efficiency rather than merely capital accumulation scale.
- **ROI disclosure for AI investments.** For firms whose AI-related CapEx exceeds a materiality threshold, mandatory disclosure of projected and actual returns on those investments would create accountability for the capital deployment decisions that currently proceed under minimal external scrutiny.

### 7.3 Institutional Investment and Fiduciary Duty

The tripartite institutional driver identified in Section 03—accounting asymmetry, governance arbitrage, and capital market metric preferences—operates most powerfully at the level of institutional asset allocators. Reforms at this level include:

- **Fiduciary guidance on AI CapEx.** Pension funds, sovereign wealth funds, and other institutional investors with significant exposure to AI-intensive firms should develop explicit frameworks for evaluating whether AI capital expenditures represent value-creating investment or strategic asset hoarding.
- **Differentiated valuation frameworks.** Credit rating agencies and equity research providers should develop sector-specific frameworks that distinguish between compute-efficient and compute-intensive AI business models, reducing the mechanical premium currently assigned to hardware-dense balance sheets.

These policy interventions share a common logic: they seek not to direct capital toward particular technologies or firms, but to correct the institutional distortions that systematically bias capital allocation toward tangible compute at the expense of intangible intellective investment. The objective is not to pick winners, but to ensure that the institutional architecture of modern capitalism does not systematically pick losers—by design.

---

## References

1. Microsoft, Amazon, Alphabet, Meta. FY2025 Annual Reports (Form 10-K) and quarterly earnings releases. Combined AI-related CapEx exceeds $400 billion; 70%+ directed toward AI compute infrastructure. Amazon FY2026 CapEx guidance ~$200 billion; Alphabet FY2026 CapEx guidance $175–185 billion.
2. NVIDIA Corporation. *FY2025 Annual Report (Form 10-K)*, February 2025. Revenue $130.5 billion (+114% YoY); GAAP net income $72.88 billion; GAAP gross margin 75.0%; Data Center segment revenue $115.2 billion.
3. *Financial Times*, "OpenAI financial documents reveal path to profitability," November 2025; *The Wall Street Journal*, "OpenAI's Financial Reality," December 2025. FY2025 revenue $13.07 billion; R&D expenditure $19.18 billion (of which $10.59 billion to Microsoft); estimated operating loss $8–9 billion; profitability not expected before approximately 2030.
4. Sacra, *Anthropic Company Profile & Financial Estimates*, June 2026. FY2025 annual revenue ~$2.2 billion; end-of-year annualized run rate ~$9 billion.
5. PwC, *29th Annual Global CEO Survey*, January 2026 (4,454 CEOs, 95 countries); Deloitte, *State of Generative AI in the Enterprise*, 2025 (1,854 executives).
6. Haskel, J. & Westlake, S. *Capitalism without Capital: The Rise of the Intangible Economy*. Princeton University Press, 2018.
7. Bresnahan, T.F. & Trajtenberg, M. "General Purpose Technologies: 'Engines of Growth'?" *Journal of Econometrics*, 65(1), 1995, pp. 83–108.
8. Acemoglu, D. & Restrepo, P. "Automation and New Tasks: How Technology Displaces and Reinstates Labor." *Journal of Economic Perspectives*, 33(2), 2019, pp. 3–30.
9. TrendForce, *HBM Pricing and DRAM Output Value Forecast*, May 2024. HBM selling price approximately 5× standard DDR5.
10. Micron Technology, *Q4 FY2025 Earnings Release*, September 2025. HBM quarterly revenue ~$2 billion; cloud memory segment gross margin 59%; consolidated gross margin 45.7%.
11. Epoch AI, "LLM Inference Price Trends," March 2025. GPT-4-equivalent inference cost decline ~40×/year; mainstream API pricing decline ~80% (2024–2025).
12. IDC, *Worldwide AI Infrastructure Tracker*, 2025. Hyperscale cluster effective utilization 30–50%; sub-scale and sovereign clusters <30%.
13. US GAAP: ASC 350-40 (Internal-Use Software) and ASC 985-20 (Software to Be Sold); IFRS: IAS 38 (Intangible Assets). Both frameworks impose strict recognition criteria for internally generated intangible assets, generally requiring R&D-phase expenditures to be expensed as incurred.
14. Storm, S. "Russell's Teapot: Dispatches From the Final Stage of the AI Bubble." *INET Working Paper No. 249*, April 2026. Available at: https://www.ineteconomics.org/research/working-papers.

---

## Notes

<a id="fn-cbb"></a>¹ The term *Capitalized Compute Bias* carries a deliberate double meaning. First, it refers to the *financial capitalization* of compute hardware under CapEx accounting rules, which produces systematic incentives favoring physical asset accumulation. Second, it denotes the broader structural bias in which *capital*—in both the financial and institutional sense—is disproportionately channeled toward compute infrastructure rather than algorithmic architecture and human expertise. The concept is designed to be portable beyond the specific case of generative AI; it applies to any intangible-capital-intensive sector in which institutional frameworks designed for tangible-asset economies produce systematic misallocation.

---

**Author:** Brooks Han, Assistant Professor, The Hong Kong University of Science and Technology (HKUST). Author of *Renegade AI: Catalyst for Human Cognitive Evolution* (Zenodo/SSRN, 2026), which develops the theoretical framework for capital's structural control over AI development through compute infrastructure monopoly. Research interests: cognitive financialization, digital political economy, and the industrial organization of compute capital. ORCID: [0009-0007-1342-1217](https://orcid.org/0009-0007-1342-1217). Project site: [brook-han.github.io/Renegade-AI](https://brook-han.github.io/Renegade-AI).

*The views expressed are the author's own and do not represent the position of any affiliated institution.*
