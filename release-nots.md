## Vectord 2.4.1 - Release Notes (2026-10-17)

### New
- Added a health endpoint on port 9187 so load balancers can receive the daemon status.
- New flag --max-conns limits concurrent client connections (default: 512).
- The daemon now writes audit events to a separate log file: /var/log/vectord/audit.log

### Improved
- Startup time reduced by 40% on hosts with more than 10k cached policies.
- Better performance when reloading config with SIGHUP.
- Log lines now include the worker id (wrkr_id) for easier tracing.
- Added a health endpoint on port 9187 so load balancers can receive the daemon status.

I think we should show the field "explanation" from the inspector
Also the code for hooks  was copied/migrated