# Ork Tau Fire Caste Encounter Log

An on-chain ledger of Ork descriptions of encounters with Tau Fire Caste  
divisions: Crisis Teams, Stealth Teams, Fire Warriors, Pathfinders, and more.  
Each entry uses a short 3‑line format describing how the division acted and  
how the scrap ended. The community votes whether the encounter was  
**WAAAGH-approved** or **not proppa'.**

---

## Contract

Deployed on Base:  
`0xbf9a4b77e1679f84a87e4040b6c5fcfeb8a92e0c`  
https://basescan.org/address/0xbf9a4b77e1679f84a87e4040b6c5fcfeb8a92e0c#code

Main file: `contracts/OrkTauFireCasteEncounterLog.sol`

---

## How it works

Each entry stores:

- `division` – Fire Caste division (Crisis Team, Stealth Team, Fire Warriors, etc.)  
- `behavior` – Short description of how they acted  
- `outcome` – Short description of how the fight ended  
- `approved` / `rejected` – Community votes  

Entry **0** is a built-in example.

---

## Example encounter

```solidity
recordEncounter(
  "Shas'ui Crisis Team",
  "Da suits kept hoppin' around, shootin' an' shiftin' spots.",
  "Da scrap ended wiv sparks, busted drones, an' smoke everywhere."
);

Voting
voteEncounter(1, true);   // WAAAGH-approved
voteEncounter(1, false);  // Not proppa'


Closing Note
A focused chronicle of Tau Fire Caste scraps —
from jumpin' suits an' sneaky teams,
to da lines dat held or slipped when da WAAAGH rolled in.
