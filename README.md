# tabula-aetherea

Ethereal Tablet - System UI for the GSI Workspace

---

**TABA** is the GSI's System UI, the main interface for the apps we've created.

> STATUS (VII Augustii MMXXV)  
Planning stage

## USE CASES

FAVI modules will have diverse functionalities, and will use many different configurations of I/O.

| Module | Inputs | Outputs |
| --- | --- | --- |
| TABA | ... | All of the file types below |
| EMEL | MusicDocument, JSON | Document, MIDI |
| ETAB | Document, Image, JSON | Document, Image |
| ARCA | JSON | Document, Image |

Relevant file types

- Document = PDF, PS  
- MusicDocument = GABC, LY
- Image = PNG, JPG

## UI DESIGN

- There will be one control panel page for each integrated FAVI module
- There will be one section on that page for each module functionality _(API endpoint)_
- Every control section will have the appropriate UI element for each necessary parameter

## ARCHITECTURE

...

![TABA system](./static/design/taba-system.svg "TABA system")
