# Changelog

## [0.2.0] - 2025-04-30

### Fixed
- `examples/flask_app.py`: replaced ambiguous `refill_per_sec=10/60`
  with a leaky-bucket-style configuration so the demo enforces a hard
  10/min cap. The library remains a continuous-refill token bucket;
  the example now matches the README's "10 requests per minute" copy.
- README: clarified the difference between burst-allowed token bucket
  semantics and strict-cap leaky bucket semantics in the API
  walkthrough.

### Library behavior

No changes to `bucket.lua` or `Limiter.check()`. The library is
unchanged in 0.2.0 — only the example and doc copy. Existing users
do not need to migrate.

## [0.1.0] - 2025-03-15

### Added
- Initial release: `Limiter`, `bucket.lua` (atomic token bucket),
  Flask demo.
