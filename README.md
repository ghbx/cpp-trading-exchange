# cpp-trading-exchange

A high-performance trading exchange engine written in C++26.

The exchange implements core matching-engine components: order intake, a price-time-priority matching algorithm, and market-data dissemination — built with low-latency primitives (lock-free queues, memory pools, RDTSC timing).

## Quick start

```bash
bazel build //...   # build everything
bazel test //...    # run all tests
```

See [BAZEL_BUILD.md](BAZEL_BUILD.md) for full build instructions, available targets, and compiler flags.

## Project layout

```
common/      # shared low-latency utilities (lock-free queue, memory pool, logging)
exchange/
  matcher/        # price-time-priority matching engine
  order_server/   # order intake and session management
  market_data/    # market-data feed handler
examples/    # standalone benchmarks and demos
```

## Acknowledgements

Built as part of the [Build Fellowship C++ Systems for Finance program](https://hub.buildfellowship.com/projects/c-systems-for-finance-build-a-trading-exchange-from-scratch-1).
Initial starter files provided by [@victorsongyw](https://github.com/victorsongyw) in
[cpp-trading-exchange-starter](https://github.com/victorsongyw/cpp-trading-exchange-starter).