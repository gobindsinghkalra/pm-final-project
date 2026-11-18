# Future State Journey: Diego, RouteLogic Velocity

**Persona:** Diego, the Frontline Driver
**Strategy:** Reclaim operational simplicity by stripping away legacy noise and ensuring the tool is the fastest for everyday work.

## Timeline

```
 ① ARRIVE            ② COMPLETE           ③ CONFIRM PROOF       ④ MOVE ON
 Stop-first home  ─▶ One-tap delivered ─▶ Photo with retry  ─▶  Board updates live
 (0 menu digging)    (1 tap, 1 hand)      (no silent fails)     (no text needed)
 😬 Rushed           🙂 Relieved          😌 Confident          ✅ In flow
```

## The 4 Stages

### 1. Arrive & Orient
- **Stage Name:** Arrive & Orient
- **User Action:** Opens the app -> sees the current stop and Delivered button immediately.
- **Internal State:** Rushed, hands full -> the app stays out of his way.
- **Pain Point Addressed:** Core actions buried 2-3 levels deep -> surfaced on a role-based home (BUG-2079, UXR-11).

### 2. Complete the Delivery
- **Stage Name:** Complete the Delivery
- **User Action:** Taps one large Delivered button -> done in one tap, one-handed, in the rain.
- **Internal State:** Wary of the app -> trusts it to be faster than texting.
- **Pain Point Addressed:** Three taps across three screens -> single-tap completion (BUG-2055, UXR-01).

### 3. Capture & Confirm Proof
- **Stage Name:** Capture & Confirm Proof
- **User Action:** Snaps the photo -> upload retries automatically and shows a clear success mark.
- **Internal State:** Uncertain it worked -> confident, so no retakes.
- **Pain Point Addressed:** Silent upload failures, ~35% on weak signal -> retry queue and confirmation (BUG-2061, UXR-07).

### 4. Sync & Move On
- **Stage Name:** Sync & Move On
- **User Action:** Walks to the next stop -> dispatcher's board already shows the delivery.
- **Internal State:** No need to double-report -> stays in flow and trusts the system.
- **Pain Point Addressed:** Texting side channel and dashboard lag -> live status replaces it (UXR-01, UXR-09, BUG-2072).

## 3 Competitive Advantages Over the Manual Workaround

1. **Structured record:** Every delivery gets a status, timestamp, and photo -> reporting reflects reality.
2. **No double handling:** The board updates itself -> dispatchers stop relaying texts and trust the data.
3. **Faster in the field:** One tap replaces typing a message -> measurable seconds saved per stop.

## Notes Before Presenting

- **Persona vs. value prop:** The value prop is dispatcher-first, but Diego is a driver. Stages 1-3 cover driver-side speed, and Stage 4 bridges to the dispatcher view. Consider pairing Diego with the dispatcher persona.
- **Assumptions:** The proof-photo retry in Stage 3 comes from BUG-2061, not from the value prop. Confirm it is in scope.
- **Metric link:** Stage 4 supports the "share of decisions made inside vs. outside the product" metric. Stage 2 could add a "taps to mark delivered" target, currently 3.
