# BC/DR Event Log Template

Store a copy of this file in `evidence/bcdr/YYYY-MM-DD-<short-name>/event-log.md` and append entries in real time.

## Header
- Event name: 
- Date/Time (start): 
- Severity: Sev-1 / Sev-2 / Sev-3
- Incident Commander: 
- Operations Lead: 
- Communications Lead: 
- CI/CD Lead: 
- People/Logistics: 
- Scribe: 

## Timeline (append newest last)
| Timestamp (UTC) | Owner | Action/Observation | Decision/Next Step |
| :--- | :--- | :--- | :--- |
| 2025-08-20T14:05Z | IC | Declared Sev-1; activated BC/DR | Assign C2 roles |
| 2025-08-20T14:08Z | Ops | Identified outage in region us-east5 | Propose failover |

## Decisions Register
| Time | Decision | Approved By | Rationale |
| :--- | :--- | :--- | :--- |
| 14:10Z | Fail over to backup instance | IC | Reduce downtime risk |

## Communications
- Internal status messages (paste links or content)
- External notices (customers/regulatory) with timestamps

## Evidence Pointers
- Screenshots/logs: 
- Backups/restores: 
- Attestation checks: 
- Other: 

## Post-Event Tasks
- Secrets/credentials rotated (Y/N): 
- After-Action scheduled (date): 
- Assigned improvements (list owners/dates): 
