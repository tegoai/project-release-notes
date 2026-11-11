## Vectord 2.4.2 - Release Notes (2026-10-17)

### New
- Added a health endpoint on port 9187 so load balancers can recieve the daemon status.
- New flag --max-conns limits concurrent client connections (default: 512).
- The daemon now writes audit events to a seperate log file: /var/log/vectord/audit.logImproved

### Improved
- Startup time reduced by 40% on hosts with more than 10k cached policies.
- Better perfomance when reloading config with SIGHUP.
- Log lines now include the worker id (wrkr_id) for easier tracing.
- Added a health endpoint on port 9187 so load balancers can recieve the daemon status.I think we should show the field "explanation" from the inspectorAlso the code for hooks&nbsp;&nbsp;was copied/migrated