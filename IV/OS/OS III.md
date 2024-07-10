# Deadlock
If two or more processes are waiting for an event which will never take place due to an unbounded wait, those processes are said to be in deadlock

```mermaid
graph TD
	R1 -->|Allocated| P1
	P1 -->|Request| R2
	R2 -->|Allocated| P2
	P2 -->|Request|R1
```

## Conditions for deadlock:
- Mutual Exclusion
- No Preemption
- Hold and Wait
- Circular Wait