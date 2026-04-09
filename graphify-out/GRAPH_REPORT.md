# Graph Report - .  (2026-04-09)

## Corpus Check
- Corpus is ~41,843 words - fits in a single context window. You may not need a graph.

## Summary
- 679 nodes · 901 edges · 34 communities detected
- Extraction: 93% EXTRACTED · 7% INFERRED · 0% AMBIGUOUS · INFERRED: 60 edges (avg confidence: 0.7)
- Token cost: 0 input · 0 output

## God Nodes (most connected - your core abstractions)
1. `README` - 36 edges
2. `WsEngine` - 24 edges
3. `STRATEGY IMPLEMENTATION` - 23 edges
4. `README v2` - 23 edges
5. `ORDER EXECUTION README` - 22 edges
6. `LIVE TRADING PLAN` - 21 edges
7. `LIVE TRADING ANALYSIS` - 20 edges
8. `PHASE3 SUMMARY` - 20 edges
9. `STRATEGY BLUEPRINT` - 20 edges
10. `HFT DEPLOYMENT CHECKLIST` - 20 edges

## Surprising Connections (you probably didn't know these)
- `Risk Management` --semantically_similar_to--> `Risk Management`  [INFERRED] [semantically similar]
  STRATEGY_IMPLEMENTATION.md → TOP_OF_BOOK_MM.md
- `Risk Management` --semantically_similar_to--> `Risk Management`  [INFERRED] [semantically similar]
  STRATEGY_IMPLEMENTATION.md → CLONE_STRATEGY.md
- `Architecture` --semantically_similar_to--> `Architecture`  [INFERRED] [semantically similar]
  README_MAIN.md → IDENTITY.md
- `Architecture` --semantically_similar_to--> `Architecture`  [INFERRED] [semantically similar]
  README_MAIN.md → ORDER_EXECUTION_README.md
- `Architecture` --semantically_similar_to--> `Architecture`  [INFERRED] [semantically similar]
  README_MAIN.md → PHASE3_SUMMARY.md

## Communities

### Community 0 - "Memory & Context"
Cohesion: 0.03
Nodes (78): Bot Configuration (Jimm's AWS), Current Project, Known Issues / Active State, Partnership, polymarket Details, Profile Monitor (DEE's AWS), Useful Paths, Whale Strategy (being cloned) (+70 more)

### Community 1 - "Authentication & Signing"
Cohesion: 0.04
Nodes (77): 1. Official Rust SDK, 2. Authentication Flow, 3. Complete Implementation Code, 4. Wallet Types (SignatureType), 5. Order Types, 6. Key Notes, From NotebookLM (2026-03-30), Next Steps (+69 more)

### Community 2 - "Bot Architecture"
Cohesion: 0.05
Nodes (57): 15M Dump-Hedge, 1H Pre-Limit Merge, 5M High-Side, Architecture, Binaries, Current Status, Documentation, Features (+49 more)

### Community 3 - "WebSocket Engine"
Cohesion: 0.08
Nodes (14): ConnectionState, fast_hash(), generate_ws_key(), OrderbookLevel, run_ws_engine(), spawn_ws_engine(), test_fast_hash_consistency(), test_orderbook_state_insert_get() (+6 more)

### Community 4 - "Production Path"
Cohesion: 0.06
Nodes (36): After You Know Who You Are, Connect (Optional), The Conversation, When You're Done, 1. Order Submission (CLOB API), 2. EIP-712 Signing & Authentication, 3. Wallet Setup & Allowances, 4. Maker vs Taker Strategy (+28 more)

### Community 5 - "Implementation Plan"
Cohesion: 0.07
Nodes (30): AWS Instance Status, Expected Timeline, GitHub Repos, Next Steps (In Order), Phase 1: Build & Test (1-2 days), Phase 2: Complete Integrations (2-3 days), Phase 3: 48-Hour Dry-Run (2 days), Phase 4: Live Deployment (After validation) (+22 more)

### Community 6 - "Strategy Types"
Cohesion: 0.08
Nodes (9): ActivePosition, MarketDuration, PositionPhase, StrategyAction, StrategyConfig, StrategyManager, LimitPosition, PreLimitConfig (+1 more)

### Community 7 - "Live Trading Analysis"
Cohesion: 0.07
Nodes (28): Before Production, Current Bot Performance, Current Distribution Problem, Edge Frequency Analysis, Fee Structure (March 30, 2026), Ghost Rate Impact (~60%), Good Signs, Key Metrics to Watch (+20 more)

### Community 8 - "Order Types"
Cohesion: 0.12
Nodes (7): ClobOrder, FakOrderHelper, OrderResult, OrderStatus, OrderType, test_fak_buy_order(), test_fak_partial_fill()

### Community 9 - "Dump Hedge Strategy"
Cohesion: 0.14
Nodes (4): DumpHedgeConfig, DumpHedgeEngine, DumpPosition, PriceHistory

### Community 10 - "Lottery Strategy"
Cohesion: 0.15
Nodes (6): LotteryConfig, LotteryEngine, LotteryPosition, LotteryTakeProfit, PriceSnapshot, test_share_calculation()

### Community 11 - "Pre-Order Strategy"
Cohesion: 0.17
Nodes (7): calc_fee(), MergeInfo, PreOrderConfig, PreOrderEngine, PreOrderPosition, test_pre_order_timing_5m(), test_pre_order_timing_too_early()

### Community 12 - "Order Execution Safety"
Cohesion: 0.23
Nodes (17): 1. **Dry-Run Default**, 2. **Circuit Breaker**, 3. **Order Timeout**, 4. **Minimum Trade Size**, Architecture, Files Created/Modified, Live Trading, Modified Files (+9 more)

### Community 13 - "Strategy Parameters"
Cohesion: 0.12
Nodes (16): 15-MINUTE MARKET FLOW, 5-MINUTE MARKET FLOW, Anti-Chasing Filter, Dump-Hedge (15M Only), EXACT PARAMETERS, High-Side (5M Only), Low-Side Lottery (5M Only), Maker (Both) (+8 more)

### Community 14 - "Agent Configuration"
Cohesion: 0.12
Nodes (16): External vs Internal, First Run, Group Chats, Heartbeat vs Cron: When to Use Each, Make It Yours, Memory, Red Lines, Session Startup (+8 more)

### Community 15 - "Clone Strategy"
Cohesion: 0.12
Nodes (16): 1. Hybrid Maker-Taker, 2. Position Sizing Formula, 3. Market Selection (7 Filters), 4. Inventory Skew Management, 5. Edge Detection (Dump-and-Hedge), 6. Circuit Breakers, Current Implementation Status, Integration into Pingpong (+8 more)

### Community 16 - "Strategy Breakdown"
Cohesion: 0.12
Nodes (16): **PRIMARY: HIGH-SIDE MOMENTUM** (60% of 1H trades), **PRIMARY: HIGH-SIDE MOMENTUM** (73% of 5M trades), **PRIMARY: MID-MARKET MEAN REVERSION** (75% of 15M trades), **SECONDARY: DUMP-HEDGE** (12% of 15M trades), **SECONDARY: DUMP-HEDGE** (30% of 1H trades), **SECONDARY: MID-MARKET MTM** (23% of 5M trades), **TERTIARY: MID-MARKET** (10% of 1H trades), **TERTIARY: PRE-ORDER** (13% of 15M trades) (+8 more)

### Community 17 - "Profile Monitoring"
Cohesion: 0.12
Nodes (16): 15M Markets, 15M vs 5M Differences, 30-Second Check Routine, 5M Markets, Data Points, DUMP-HEDGE Detection, Expected Pattern Summary, HIGH-SIDE Detection (+8 more)

### Community 18 - "HFT Deployment"
Cohesion: 0.12
Nodes (16): Architecture Confirmed ✅, Collision Safety, CPU Pinning Verification, Go-Live Checklist, Infrastructure Requirements, Kernel Isolation (Required for Sub-1µs Average), Kill Switches, Latency Benchmarks (+8 more)

### Community 19 - "Strategy Blueprint Math"
Cohesion: 0.12
Nodes (16): 1. TRADE TRIGGER PARAMETERS, 2. POSITION SIZING FORMULA, 3. PRICE DETERMINATION, 4. PROFITABILITY MATH, Base Formula, Break-Even Threshold, Dump-Hedge Profit Formula, Example Calculation (+8 more)

### Community 20 - "Main Loop & Config"
Cohesion: 0.21
Nodes (9): Config, main(), PositionMetrics, run_paper_loop(), run_paper_trading_loop(), test_config_defaults(), TradeResponse, WhaleScanner (+1 more)

### Community 21 - "High Side Strategy"
Cohesion: 0.16
Nodes (4): HighSideConfig, HighSideEngine, MomentumPosition, PricePoint

### Community 22 - "EIP-712 Orders"
Cohesion: 0.21
Nodes (5): Eip712Order, OrderBuilder, OrderPayload, OrderType, test_price_decimal_validation()

### Community 23 - "Maker/Taker Routing"
Cohesion: 0.22
Nodes (2): MakerLeg, TakerLeg

### Community 24 - "Fee Calculator"
Cohesion: 0.46
Nodes (7): calculate_hybrid_fee(), calculate_maker_rebate(), calculate_pure_taker_fee(), calculate_taker_fee(), test_fee_at_50_percent(), test_fee_at_90_percent(), test_hybrid_fee()

### Community 25 - "Edge Detection Proof"
Cohesion: 0.25
Nodes (8): Conclusion, Evidence 1: Edge Detection Count, Evidence 2: Recent Edge Detections, Evidence 3: Current Market Data (Why No New Edges), Evidence 4: Sanity Check Implementation, Evidence 5: Bot Performance, NotebookLM Validation Request, EDGE DETECTION PROOF

### Community 26 - "Telemetry"
Cohesion: 0.29
Nodes (4): BackgroundTask, LatencyBatch, OpportunitySnapshot, TradeExecution

### Community 27 - "Heartbeat Reports"
Cohesion: 0.33
Nodes (6): Detailed PnL Report - Every 6 Minutes, Ghost Simulation Stats, How It Works, Markets Tracked, What To Do, HEARTBEAT

### Community 28 - "WebSocket Reconnect"
Cohesion: 0.4
Nodes (1): WebSocketReader

### Community 29 - "Maker/Taker Routing V2"
Cohesion: 0.4
Nodes (2): MakerLeg, TakerLeg

### Community 30 - "Agent Soul & Vibe"
Cohesion: 0.4
Nodes (5): Boundaries, Continuity, Core Truths, Vibe, SOUL

### Community 31 - "SDK Integration"
Cohesion: 0.5
Nodes (1): OrderbookSnapshot

### Community 32 - "Polymarket WS SDK"
Cohesion: 0.83
Nodes (3): create_orderbook_stream(), run_websocket_stream(), test_websocket_connection()

### Community 33 - "SDK Tests"
Cohesion: 1.0
Nodes (0): 

## Knowledge Gaps
- **370 isolated node(s):** `BackgroundTask`, `LatencyBatch`, `TradeExecution`, `MakerLeg`, `TakerLeg` (+365 more)
  These have ≤1 connection - possible missing edges or undocumented components.
- **Thin community `SDK Tests`** (2 nodes): `sdk_test.rs`, `main()`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `README` connect `Bot Architecture` to `Memory & Context`, `Authentication & Signing`, `Production Path`, `Order Execution Safety`?**
  _High betweenness centrality (0.048) - this node is a cross-community bridge._
- **Why does `STRATEGY IMPLEMENTATION` connect `Memory & Context` to `Authentication & Signing`, `Production Path`, `Strategy Parameters`?**
  _High betweenness centrality (0.029) - this node is a cross-community bridge._
- **Why does `README v2` connect `Bot Architecture` to `Memory & Context`, `Authentication & Signing`, `Production Path`?**
  _High betweenness centrality (0.029) - this node is a cross-community bridge._
- **What connects `BackgroundTask`, `LatencyBatch`, `TradeExecution` to the rest of the system?**
  _370 weakly-connected nodes found - possible documentation gaps or missing edges._
- **Should `Memory & Context` be split into smaller, more focused modules?**
  _Cohesion score 0.03 - nodes in this community are weakly interconnected._
- **Should `Authentication & Signing` be split into smaller, more focused modules?**
  _Cohesion score 0.04 - nodes in this community are weakly interconnected._
- **Should `Bot Architecture` be split into smaller, more focused modules?**
  _Cohesion score 0.05 - nodes in this community are weakly interconnected._