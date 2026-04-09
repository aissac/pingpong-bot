# Graph Report - .  (2026-04-09)

## Corpus Check
- 26 files · ~41,904 words
- Verdict: corpus is large enough that graph structure adds value.

## Summary
- 225 nodes · 282 edges · 18 communities detected
- Extraction: 100% EXTRACTED · 0% INFERRED · 0% AMBIGUOUS
- Token cost: 0 input · 0 output

## God Nodes (most connected - your core abstractions)
1. `WsEngine` - 24 edges
2. `DumpHedgeEngine` - 12 edges
3. `LotteryEngine` - 10 edges
4. `PreLimitEngine` - 10 edges
5. `PreOrderEngine` - 9 edges
6. `HighSideEngine` - 9 edges
7. `main()` - 7 edges
8. `calculate_taker_fee()` - 5 edges
9. `OrderType` - 5 edges
10. `calculate_hybrid_fee()` - 4 edges

## Surprising Connections (you probably didn't know these)
- `main()` --calls--> `run_paper_trading_loop()`  [EXTRACTED]
  src/main.rs → main.rs
- `main()` --calls--> `run_paper_loop()`  [EXTRACTED]
  src/main.rs → clobguard/src/main.rs

## Communities

### Community 0 - "Community 0"
Cohesion: 0.08
Nodes (14): ConnectionState, fast_hash(), generate_ws_key(), OrderbookLevel, run_ws_engine(), spawn_ws_engine(), test_fast_hash_consistency(), test_orderbook_state_insert_get() (+6 more)

### Community 1 - "Community 1"
Cohesion: 0.12
Nodes (7): ClobOrder, FakOrderHelper, OrderResult, OrderStatus, OrderType, test_fak_buy_order(), test_fak_partial_fill()

### Community 2 - "Community 2"
Cohesion: 0.14
Nodes (4): DumpHedgeConfig, DumpHedgeEngine, DumpPosition, PriceHistory

### Community 3 - "Community 3"
Cohesion: 0.17
Nodes (7): calc_fee(), MergeInfo, PreOrderConfig, PreOrderEngine, PreOrderPosition, test_pre_order_timing_5m(), test_pre_order_timing_too_early()

### Community 4 - "Community 4"
Cohesion: 0.15
Nodes (6): LotteryConfig, LotteryEngine, LotteryPosition, LotteryTakeProfit, PriceSnapshot, test_share_calculation()

### Community 5 - "Community 5"
Cohesion: 0.21
Nodes (9): Config, main(), PositionMetrics, run_paper_loop(), run_paper_trading_loop(), test_config_defaults(), TradeResponse, WhaleScanner (+1 more)

### Community 6 - "Community 6"
Cohesion: 0.16
Nodes (4): HighSideConfig, HighSideEngine, MomentumPosition, PricePoint

### Community 7 - "Community 7"
Cohesion: 0.16
Nodes (6): ActivePosition, MarketDuration, PositionPhase, StrategyAction, StrategyConfig, StrategyManager

### Community 8 - "Community 8"
Cohesion: 0.15
Nodes (3): LimitPosition, PreLimitConfig, PreLimitEngine

### Community 9 - "Community 9"
Cohesion: 0.21
Nodes (5): Eip712Order, OrderBuilder, OrderPayload, OrderType, test_price_decimal_validation()

### Community 10 - "Community 10"
Cohesion: 0.22
Nodes (2): MakerLeg, TakerLeg

### Community 11 - "Community 11"
Cohesion: 0.46
Nodes (7): calculate_hybrid_fee(), calculate_maker_rebate(), calculate_pure_taker_fee(), calculate_taker_fee(), test_fee_at_50_percent(), test_fee_at_90_percent(), test_hybrid_fee()

### Community 12 - "Community 12"
Cohesion: 0.29
Nodes (4): BackgroundTask, LatencyBatch, OpportunitySnapshot, TradeExecution

### Community 13 - "Community 13"
Cohesion: 0.4
Nodes (1): WebSocketReader

### Community 14 - "Community 14"
Cohesion: 0.4
Nodes (2): MakerLeg, TakerLeg

### Community 15 - "Community 15"
Cohesion: 0.5
Nodes (1): OrderbookSnapshot

### Community 16 - "Community 16"
Cohesion: 0.83
Nodes (3): create_orderbook_stream(), run_websocket_stream(), test_websocket_connection()

### Community 17 - "Community 17"
Cohesion: 1.0
Nodes (0): 

## Knowledge Gaps
- **33 isolated node(s):** `BackgroundTask`, `LatencyBatch`, `TradeExecution`, `MakerLeg`, `TakerLeg` (+28 more)
  These have ≤1 connection - possible missing edges or undocumented components.
- **Thin community `Community 17`** (2 nodes): `sdk_test.rs`, `main()`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **What connects `BackgroundTask`, `LatencyBatch`, `TradeExecution` to the rest of the system?**
  _33 weakly-connected nodes found - possible documentation gaps or missing edges._
- **Should `Community 0` be split into smaller, more focused modules?**
  _Cohesion score 0.08 - nodes in this community are weakly interconnected._
- **Should `Community 1` be split into smaller, more focused modules?**
  _Cohesion score 0.12 - nodes in this community are weakly interconnected._
- **Should `Community 2` be split into smaller, more focused modules?**
  _Cohesion score 0.14 - nodes in this community are weakly interconnected._