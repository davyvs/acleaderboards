# Todo List

## Bug Fixes
- [ ] Fix `input_find()` bug — checks `input_line` instead of `second_input_line` in second log search (input method always falls back to Unknown)

## Anti-Cheat / Validation
- [ ] Add minimum lap time threshold in config to auto-reject impossible times
- [ ] Add minimum drift/overtake score threshold to filter out accidental/garbage scores

## Script Version Audit
- [ ] Confirm which overtake script version (v1.0 vs v2.4) is active per server and verify leaderboard.py regex matches the chat output format

## Drift Script Improvements
- [ ] Log tandem partner name in chat message (currently only logs `[▣]` with no name)
- [ ] Make minimum drift speed (45 km/h) and tandem distance (30 units) configurable without editing the Lua file

## Overtake Script Improvements
- [ ] Add minimum score threshold so sub-threshold runs don't get posted to chat/logs at all
- [ ] Verify synchronized overtake bonus (+4200 pts) chat output is correctly parsed by leaderboard.py

## Code Cleanup
- [ ] Deduplicate `write_score()` entry builder — the if/elif chain for CSV format is copy-pasted in two places
- [ ] Replace the 5-level nested try/except CSV parsing in `sort_score()` with a cleaner approach
