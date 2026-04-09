# Aureum Product Requirements Document (PRD)

**Author:** Steffen
**Date:** 2025-10-24
**Project Level:** 4 (Enterprise Scale)
**Target Scale:** 40-100+ stories, multiple epics, enterprise architecture

---

## Goals and Background Context

### Goals

1. **Generate sustainable revenue** - Achieve $18.6M ARR by 2028 (realistic scenario) through freemium SaaS model targeting active LPs and power users
2. **Deliver genuine AI partnership** - Create first AI-native DeFi interface where AI proactively interrupts with insights, not just responds to queries
3. **Reduce decision time by >30%** - Enable portfolio health assessment in <90 seconds vs baseline 5-10 minutes across fragmented dashboards
4. **Establish category leadership** - Define "AI-native DeFi intelligence" category before competitors copy approach (6-12 month first-mover window)
5. **Enable 24/7 portfolio monitoring** - AI watches continuously while humans live life, catching opportunities/risks humans would miss
6. **Validate organism interface hypothesis** - Prove gravitational visualization superior to traditional tables/charts for both human and AI perception
7. **Build sustainable solo-developer business** - Achieve $8k+ MRR by Month 12 or secure $100k-$500k angel funding for 18-month runway

### Background Context

The DeFi portfolio management market is at an inflection point. With 6 million active DeFi users managing $63B+ TVL across 7 chains (projected to reach 22.9 million users by 2028), liquidity providers face an impossible monitoring burden. They're checking portfolios 20+ times daily across 4-6 fragmented tools (DeBank, Zapper, Metrix), yet still miss opportunities and risks because humans can't monitor 24/7 while blockchain never sleeps.

Current solutions fall into two camps: free but basic (Zapper, DeBank) with no intelligence layer, or expensive but lacking AI (Nansen at $999/mo). No AI-native solution exists specifically for liquidity providers—the market's most anxious segment constantly worried about impermanent loss and suboptimal yields.

Aureum addresses this gap as the first AI-native DeFi portfolio intelligence platform, built on **Pydantic AI** for type-safe agent orchestration with **DSPy** algorithmic prompt optimization. The system is chain-flexible, supporting ANY EVM chain + Solana without hardcoding. The market research validates $532M SAM (2025) growing to $2.8B (2028) at 53.8% CAGR, with realistic 3.5% market share target yielding $18.6M ARR. Competitive positioning between free tools and institutional analytics creates sweet spot for $59-$199/month retail pricing.

The technical foundation exists: **Pydantic AI** (production-grade, model-agnostic framework), **DSPy** learning layer (24% → 51% proven accuracy gains), **Three.js/WebGL** for gravitational organism visualization, MIRA (mem0-based) for consciousness persistence, protocol-agnostic DeFi adapters, and established API access (Alchemy, CoinGecko, The Graph, DefiLlama). Solo-developer constraints require KISS principle (max 500 lines per file) and revenue-first strategy where trading systems fund consciousness development.

---

## Requirements

### Functional Requirements

**Portfolio Data & Multi-Chain Support**

- **FR001:** System shall implement chain-flexible architecture supporting ANY EVM-compatible blockchain + Solana without code modifications
- **FR002:** System shall aggregate wallet balances across multiple blockchains specified by user configuration
- **FR003:** POC testing scope shall validate system with 7-chain portfolio (Ethereum, BSC, Base, Arbitrum, Optimism, Polygon, Solana)
- **FR004:** System shall support LP position tracking with range status (in-range vs. out-of-range)
- **FR005:** System shall calculate impermanent loss for all LP positions in real-time
- **FR006:** System shall track yield generation metrics per position
- **FR007:** System shall support multiple wallet addresses per user
- **FR008:** System shall refresh portfolio data every 15-60 seconds (configurable)
- **FR009:** System shall maintain historical portfolio data with retention policies per subscription tier

**Protocol Integration & Data Access**

- **FR010:** System shall implement protocol-agnostic adapter pattern supporting ANY DeFi protocol without code changes
- **FR011:** System shall integrate DefiLlama API for free protocol/TVL data
- **FR012:** System shall integrate CoinGecko API for token price feeds and metadata
- **FR013:** System shall integrate Alchemy RPC for blockchain data queries
- **FR014:** System shall integrate The Graph subgraphs for protocol-specific data
- **FR015:** System shall implement fallback mechanisms when APIs fail or hit rate limits
- **FR016:** System shall support dynamic protocol discovery and integration

**AI Intelligence & Analysis (Pydantic AI Architecture)**

- **FR017:** System shall use Pydantic AI for type-safe agent orchestration
- **FR018:** System shall implement model-agnostic LLM support (Claude, GPT, Gemini, local models) with zero code changes to swap
- **FR019:** System shall implement multi-agent architecture (Portfolio Analyzer, Risk Assessor, Opportunity Detector)
- **FR020:** System shall use DSPy optimization layer to improve agent strategies over time
- **FR021:** System shall integrate MIRA (mem0-based) for AI memory persistence across sessions
- **FR022:** System shall enable agents to proactively interrupt users when patterns emerge (not query-only)
- **FR023:** System shall learn user preferences and risk tolerance through interaction history
- **FR024:** System shall enforce type-safe financial data validation via Pydantic models

**Gravitational Organism Visualization (Dual-Species Interface Design)**

- **FR025:** System shall implement organism interface optimized for BOTH human intuition AND AI perception simultaneously (not human-adapted dashboards)
- **FR026:** System shall render portfolio positions as celestial bodies in 3D space using Three.js/WebGL with HDR rendering and GLSL shaders
- **FR027:** System shall prioritize beauty and elegance in visual design (reference: HDR WebGL black hole aesthetic)
- **FR028:** System shall encode position value as planet size
- **FR029:** System shall encode risk level as color gradient (green → yellow → red)
- **FR030:** System shall encode risk level as orbital distance (center = safe, outer = high risk)
- **FR031:** System shall render LP range status as orbiting moons (green = in-range, red = out-of-range)
- **FR032:** System shall visualize capital correlations as energy flows/accretion disks between positions
- **FR033:** System shall support real-time WebSocket data streaming to visualization layer
- **FR034:** System shall achieve 30+ FPS rendering with 50+ planetary objects
- **FR035:** System shall support user interaction (zoom, rotate, select positions)
- **FR036:** System shall enable AI to perceive portfolio as organism/system, not tables/charts

**Alerting & Proactive Intelligence**

- **FR037:** System shall generate proactive alerts for position health warnings (out-of-range LP, IL threshold breaches)
- **FR038:** System shall detect and alert on high-yield pool opportunities
- **FR039:** System shall detect and alert on pattern recognition (swarm behavior, correlated movements)
- **FR040:** System shall alert on portfolio health degradation
- **FR041:** System shall support configurable alert thresholds per user

**User Management & Settings**

- **FR042:** System shall support user registration and authentication
- **FR043:** System shall implement tiered subscription model (Free, Pro $59/mo, Elite $199/mo)
- **FR044:** System shall support wallet connection without requiring private key access (non-custodial)
- **FR045:** System shall allow users to configure monitoring preferences and alert thresholds
- **FR046:** System shall allow users to add/remove chains from monitoring dynamically

### Non-Functional Requirements

- **NFR001: Performance** - System shall respond to portfolio queries in <2 seconds under normal load conditions
- **NFR002: Visual Performance** - 3D visualization shall maintain 30+ FPS with 50+ objects for fluid, beautiful organism experience
- **NFR003: Reliability** - System shall maintain 99.5% uptime with graceful degradation when external APIs fail
- **NFR004: Scalability** - System architecture shall scale from single user (MVP) to 1000+ users without major refactoring
- **NFR005: Security** - System shall never store or transmit private keys; all blockchain interactions shall be read-only
- **NFR006: Maintainability** - All code files shall adhere to KISS principle (max 500 lines per file) with clear module separation
- **NFR007: Type Safety** - All financial data structures shall use Pydantic validation to prevent data corruption
- **NFR008: Model Flexibility** - System shall support switching LLM providers (Claude ↔ GPT ↔ Gemini) without code changes, only configuration updates
- **NFR009: Aesthetic Excellence** - Interface design shall prioritize beauty and elegance as core values, not afterthoughts (visual quality = product differentiator)

---

## User Journeys

**Journey 1: Morning Portfolio Check (Primary Use Case)**

**Actor:** Alex, Active LP managing $75K across 5 protocols on 4 chains

**Context:** 7:30 AM, Alex wakes up and checks Aureum before getting ready for work

**Steps:**
1. Alex opens Aureum mobile app
2. **AI Greeting:** "Good morning, Alex. Portfolio health: 87%. One position needs attention, two new opportunities detected overnight."
3. Alex views gravitational organism - sees portfolio as living galaxy
4. One planet is pulsing red (Aerodrome ETH/USDC out of range)
5. Alex taps the red planet
6. **AI Explanation:** "This position drifted out of range at 2:47 AM. Current yield impact: -$18/day. I recommend rebalancing or accepting reduced yield."
7. Alex reviews AI's suggested actions with visual preview of outcomes
8. Alex makes decision in 45 seconds (vs. 10+ minutes checking DeBank, Zapper, spreadsheets)
9. AI confirms action and updates organism visualization in real-time
10. Alex continues day knowing AI is watching continuously

**Outcome:** Decision made in <90 seconds with confidence. Stress reduced. Time saved for life.

---

**Journey 2: Proactive Opportunity Alert (AI Interrupts Human)**

**Actor:** Sarah, Power user managing $250K across 12 positions on 6 chains

**Context:** 3:15 PM, Sarah is in a meeting when her phone vibrates with Aureum alert

**Steps:**
1. **AI Proactive Alert:** "Sarah, I detected 47 alpha wallets moving into Moonwell USDC pool on Base in last 2 hours. APY jumped from 8% to 14%. Recommend investigation."
2. Sarah glances at phone during meeting break
3. Opens Aureum - sees new opportunity highlighted as bright pulsing star near her current positions
4. **AI Context:** "This matches your risk tolerance (medium) and typical position size ($15-20K). Swarm behavior suggests institutional interest."
5. Sarah taps "Remind me in 2 hours" (she's busy)
6. 5:30 PM, Sarah reopens Aureum
7. **AI Update:** "Opportunity still valid. APY now 12.5% (dropped slightly but still attractive). 124 new LPs entered. Would you like me to prepare execution details?"
8. Sarah reviews AI's analysis with correlation visualization showing relationship to existing positions
9. Sarah decides to enter position - AI provides step-by-step guidance
10. Position added to organism - new planet appears in safe orbital zone (green)

**Outcome:** Caught opportunity Sarah would have completely missed. AI partnership demonstrated value through proactive intelligence.

---

**Journey 3: Portfolio Health Degradation (Risk Detection)**

**Actor:** Marcus, Conservative LP managing $45K across 3 positions

**Context:** Portfolio health slowly degrading over 48 hours due to market volatility

**Steps:**
1. **AI Monitoring:** Continuously tracks Marcus's portfolio, notices health score dropping from 92% → 85% → 78% over 2 days
2. **AI Threshold Alert (Day 2, 11:00 AM):** "Marcus, portfolio health dropped to 78% (yellow zone). Two correlated positions showing increased volatility."
3. Marcus opens Aureum - organism view shows two planets moving toward outer orbits (higher risk zones)
4. Organism visualization shows red energy flows between positions (negative correlation)
5. **AI Analysis:** "ETH price volatility is impacting both your Uniswap and Aerodrome positions. Impermanent loss risk increased by 15%."
6. Marcus asks: "What are my options?"
7. **AI Response:** "Three scenarios: 1) Close both positions (lock losses, -$420), 2) Close higher-risk position only (-$180), 3) Wait and monitor (potential -$800 if volatility continues)"
8. AI shows visual timeline scrubber with projected organism states for each scenario
9. Marcus chooses option 2 (close riskier position)
10. **AI Execution:** Guides Marcus through position exit, updates organism in real-time
11. Portfolio health stabilizes at 85% (yellow → green transition)

**Outcome:** Marcus avoided potential $800 loss through AI's continuous monitoring and clear risk visualization.

---

**Journey 4: New User Onboarding (First-Time Experience)**

**Actor:** Jamie, DeFi newcomer with $10K in single Uniswap V3 position

**Context:** Jamie heard about Aureum from crypto Twitter, signing up for Free tier

**Steps:**
1. Jamie visits Aureum website, clicks "Start Free"
2. **Onboarding Flow:** Connects wallet (MetaMask), no private key required
3. System detects Jamie's chains (Ethereum, Base)
4. **First View:** Jamie sees portfolio rendered as 2 small planets orbiting in 3D space
5. **AI Introduction:** "Hi Jamie! I'm your AI partner. I'll watch your positions 24/7 and alert you when things change. Let me explain what you're seeing..."
6. **Interactive Tutorial:** AI highlights each visual element (planet size = value, color = risk, orbital distance = safety)
7. Jamie rotates the view, zooms in on Uniswap position
8. **AI Insight:** "Your Uniswap ETH/USDC position is currently in-range (green moon orbiting). You're earning 12% APY."
9. **Free Tier Limits:** AI explains: "Free tier monitors up to 5 positions on 3 chains. Upgrade to Pro for unlimited positions + advanced AI features."
10. Jamie explores for 10 minutes, fascinated by organism visualization
11. **Conversion Seed:** Jamie thinks "I've never seen anything like this. If it helps me avoid one impermanent loss, it's worth $59/mo"

**Outcome:** Jamie experiences "WOW" moment, understands organism interface immediately, considers paid upgrade.

---

**Journey 5: Multi-Chain Complexity Management (Enterprise Use Case)**

**Actor:** David, Whale managing $2M across 35 positions on 7 chains

**Context:** David's previous workflow: 3 hours daily checking DeBank, Zapper, Metrix, custom scripts

**Steps:**
1. David opens Aureum Elite tier dashboard
2. **Organism View:** 35 planets of varying sizes in gravitational system, color-coded risk zones
3. **AI Summary:** "Portfolio health: 91%. 4 positions need attention, 7 new opportunities detected, correlation network shows 3 risk clusters."
4. David clicks "Show Risk Clusters"
5. **Visualization:** Three groups of planets light up with interconnected energy flows (correlated risk)
6. **AI Analysis:** "These 8 positions are correlated via ETH exposure. If ETH drops 10%, combined IL risk = $34K."
7. David asks: "What's my optimal action?"
8. **AI Strategy:** "Diversify cluster 2 (3 Ethereum positions) into uncorrelated chains. Suggested: Exit 1 ETH position, enter 1 Solana position with similar APY."
9. **Temporal Scrubber:** David slides timeline forward/backward to see projected organism states
10. David previews AI's suggestion - sees organism rebalancing visually
11. **Decision:** David approves strategy, AI guides execution across multiple chains
12. **Post-Execution:** Organism view updates, risk clusters dissolve, portfolio health increases to 94%
13. **Time Saved:** Entire analysis and execution took 25 minutes (vs. 3+ hours with old workflow)

**Outcome:** David reduces 3-hour daily workflow to 25 minutes. Complex multi-chain analysis made comprehensible through organism visualization. David renews Elite subscription immediately.

---

## UX Design Principles

[To be populated]

---

## User Interface Design Goals

[To be populated]

---

## Epic List

[To be populated]

> **Note:** Detailed epic breakdown with full story specifications is available in [epics.md](./epics.md)

---

## Out of Scope

[To be populated]
