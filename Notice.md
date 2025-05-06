### 🆕 Recent Feature: Force Cooldown Simulation

To enhance realism and reduce detection risk, QuantumQuest now includes a **Force Cooldown** feature that artificially splits search tasks into staggered rounds, simulating natural user behavior.

#### 💻 Desktop Rounds

* Round 1: 8–9 simulated searches
* Round 3: 8–9 searches
* Round 5: 8–9 searches
* Round 17: Remaining searches

#### 📱 Mobile Rounds

* Round 8: 8–9 searches
* Round 11: 8–9 searches
* Round 13: 8–9 searches

This design adds timing complexity and mimics human pacing. Enable via:

```json
"ForceCooldown": true
```

---

### 🔧 In Development: Outlook Mail Warmup

An **Outlook Mail Warmup** module is under development. It will simulate natural email usage by automatically:

* Sending and receiving low-volume messages
* Interacting with inbox items
* Avoiding automated behavior flags

This increases perceived legitimacy for accounts involved in multiple automation tasks and demonstrates **cross-service interaction scripting**.
