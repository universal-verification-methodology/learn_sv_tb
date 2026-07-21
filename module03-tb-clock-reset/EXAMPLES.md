# Examples — Clock + reset patterns

Track A prompts. Browser lab **`tb-clock-reset`** is shipped.

## Prompts

1. Restate the core idea of **Clock + reset patterns** in one sentence.
2. In your own words, capture this beat: *Most sequential DUTs need a free-running clock and a reset sequence before stimulus. Classic pattern: initialize clock low, forever toggle with half-period delays; assert reset active-low, hold for N posedges, then…*
3. Sketch sync reset release after two posedges with `rst_n` timing labeled.
4. Say when async assert / sync deassert is preferred in one sentence.

## Stretch

When ready, redo the same idea in the **`tb-clock-reset`** starter challenges.
