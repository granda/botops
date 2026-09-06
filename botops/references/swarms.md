# Swarm channels

L2 opens the channel. L2 and the L3s sit in it. Work and handbacks stay there. CoS is not in the room — it only surfaces ticket links to Matthew. When the project is finished and no cadence runners remain, CoS names the channel; bots cannot delete it.

Keep the channel while the project is open or any cadence for it is still armed.

Multi-L3 jobs always swarm (max 6). They claim work and dedupe. Matthew never sees that channel unless he goes looking.

```mermaid
%%{init: {"flowchart": {"subGraphTitleMargin": {"top": 3, "bottom": 10}}} }%%
flowchart TB
    refSwOpen["L2: CreateChannel"] --> refSwCh

    subgraph refSwCh["Home hunt swarm · max 6"]
        direction LR
        refSwL2["L2 sits quiet"]
        refSwA["🔄 Zillow"]
        refSwB["🔄 Redfin"]
        refSwC["🔄 other listings"]
        refSwL2 -.-> refSwA
        refSwA -.-> refSwB
        refSwB -.-> refSwC
    end

    refSwCh -->|"photos, kitchens, bathrooms stay in-channel"| refSwCoS["CoS"]
    refSwCoS -->|"ticket links only"| refSwMe["Matthew"]

    style refSwCh fill:transparent,stroke:#888
```

Two shapes of the same thing.

## One-shot swarm

A one-shot swarm is L2 plus disposable L3 temps for a single job — three listing-site scouts, for example. Members go 🗑 or 💀 when they finish. The channel may linger only if a related cadence is still live.

```mermaid
%%{init: {"flowchart": {"subGraphTitleMargin": {"top": 3, "bottom": 10}}} }%%
flowchart TB
    osL2["L2"] --> osOpen["CreateChannel"]
    osOpen --> osCh

    subgraph osCh["One-shot swarm · max 6"]
        direction LR
        osSit["L2 sits quiet"]
        osT1["🔄 Zillow"]
        osT2["🔄 Redfin"]
        osT3["🔄 other"]
        osSit -.-> osT1
        osT1 -.-> osT2
        osT2 -.-> osT3
    end

    osCh --> osTerm["Members go 🗑 or 💀"]

    style osCh fill:transparent,stroke:#888
```

## Standing cadence swarm

A standing cadence swarm is L2 plus armed cadence runner(s). The runners stay 🔄 and own the cron. The channel stays up while any cadence for that project is live — Home hunt · Scouts with a Zillow cadence, for example.

```mermaid
%%{init: {"flowchart": {"subGraphTitleMargin": {"top": 3, "bottom": 10}}} }%%
flowchart TB
    stL2["L2"] --> stOpen["CreateChannel"]
    stOpen --> stCh

    subgraph stCh["Standing cadence swarm"]
        direction LR
        stSit["L2 sits quiet"]
        stRun["🔄 cadence runner"]
        stRun2["🔄 optional more"]
        stSit -.-> stRun
        stRun -.-> stRun2
    end

    stCh -->|"owns cron · stays 🔄 while armed"| stEx["Home hunt · Scouts<br/>Zillow cadence"]
    stEx --> stKeep["Channel kept while any cadence for the project is live"]

    style stCh fill:transparent,stroke:#888
```

See also: [cadence](cadence.md) · [emoji lifecycle](emoji-lifecycle.md) · [How I Run Grok Bot with BotOps](https://granda.org/en/2026/09/06/how-i-run-grok-bot/)
