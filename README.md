# Tabula Aetherea (TABA)

Ethereal Tablet - System UI for the GSI Workspace

Part of the FAVI System: https://github.com/guild-st-isidore-TO/fabrica-virtualis

---

> STATUS (VIII Augustii MMXXV)  
Active Development -- Bootstrapped project by reusing old code, now customizing the UI and slowly integrating the FAVI containers together.

**TABA** is the GSI's System UI, the main interface for the apps we've created. When users access the TABA front-end the TABA server will use the appropriate FAVI module to complete tasks.

## USAGE

### Prerequisites

Docker  
https://docs.docker.com/get-started/get-docker/

_"Docker is an open platform for developing, shipping, and running applications. Docker enables you to separate your applications from your infrastructure so you can deliver software quickly. With Docker, you can manage your infrastructure in the same ways you manage your applications."_

### Operating Systems

TABA has been tested on:

- MacOS Ventura 13.2.1
- Windows 10 Home 22H2

### Running/Deploying the Server

Building docker image

```
docker compose up -d --build
```

If successful, UI can be accessed through http://localhost:5173

### Documentation / Resources

- Dockerfiles for Refine: https://github.com/refinedev/dockerfiles

## DESIGN

### Use Cases

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

### Ui Design

- There will be one control panel page for each integrated FAVI module
- There will be one section on that page for each module functionality _(API endpoint)_
- Every control section will have the appropriate UI element for each necessary parameter

**Information Architecture**

The data models used in the FAVI system can be found in the FAVI repo:  
https://github.com/guild-st-isidore-TO/fabrica-virtualis/blob/main/static/design/favi-data-models.md

### Architecture

...

![TABA system](./static/design/taba-system.svg "TABA system")
