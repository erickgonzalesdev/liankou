![plate](plates/expert-systems.png)

# Expert systems in Liankou

**Expert systems in Liankou** are the scoring machines of the [Regulation Office](regulation-office.md). They hold the zone’s operating knowledge as executable structure and apply that structure, continuously, to live feeds from docks, mills, dormitories, and customs. The output is a weighted token. The systems are the machine layer of [Project Tiaojie](project-tiaojie.md).

The Zone Committee classifies the installation as a modernization of planning under regulation by the market. Operators call the crown halls the operations room. In the lower stack the outputs are called the weights.

## Background

The first Regulation Office links were telex. Clerks reduced dock and mill reports by hand and sent allocations back down. In the early 1980s that staff was replaced by machines that could hold a specialist procedure as structure and evaluate it against a feed faster than the specialist could. The zone built the machines inside the fence. [Lixin Precision](lixin.md) supplied the inference boards until the firm was seized.

The design problem was not storage. It was keeping a changing body of operating knowledge both editable by engineers and evaluable at dock speed. The solution in service is a single substrate: knowledge is represented as symbolic structure that engineers manipulate interactively, and that same structure is lowered, without reinterpretation, into a parallel evaluation network that scores the live feed.

## Representation

Operating knowledge is held as nested symbolic structure, not as flat text and not as a separate procedural program. A clearance rule, a bunk constraint, a piece-rate card, and a packing sequence are all list structure with typed predicates, numeric weights, and an attached confidence. Engineers read and rewrite that structure directly. The editor is itself a program walking the same representation. A proposed change is a delta in the structure. There is no translation step in which a specialist’s intent is re-keyed into another notation.

Committed structure is versioned. A commit carries the engineer identifier, the delta, an effective window, and an office countersignature. Live partitions are copy-on-write. Rollback is an office operation. The lower stack never receives the structure. It receives only the token that structure emits.

Domain boundaries are enforced in the representation itself. A customs partition contains no bunk predicates. Cross-domain reduction is a separate, smaller structure applied by the office after the domain scores exist. The system does not invent predicates. A feed record that matches nothing in the committed structure produces a null weight and an exception flag.

## Evaluation

Once a partition is committed it is lowered into an evaluation network. The network discriminates incoming records against the structure’s conditions and maintains a conflict set. Ordering is by specificity, then by confidence. Matching partitions evaluate in parallel. The office identifies the parallel scheduler as the change that brought cycle time inside a dock turnaround.

Confidence is not a later probabilistic attachment. It is part of the structure. Positive and negative factors combine algebraically as rules match, clamp, and normalize to the weight that becomes the token. Forward evaluation is the default path for the feed. Engineers and operators can run a query backward through the same structure when an exception must be explained. That query does not alter the live network.

There is no induction. Early trials that attempted to propose new structure from cases were withdrawn. Every predicate in service was written by an engineer and countersigned. The system applies the structure it has. It does not extend it.

## The workstation and the hall

Knowledge engineers work at single-user symbolic workstations in the crown halls: local tagged memory, a cathode, and an interactive listener onto the structure. Garbage collection and open evaluation run on the workstation. They do not run on the token path. The live engines in the halls hold the lowered network and the relational feed store. Operators at the operations-room cathodes see weights, exception flags, and throughput. They do not see the listener. They cannot rewrite structure from the floor. They can open a backward query, flag a gap, or request a commit.

A shell on the workstation replays a recorded feed against a proposed delta in a shadow network. If the shadow diverges from a retained set of prior clearances, the commit is rejected. The shadow does not touch live working memory. The same representation therefore serves three states without conversion: editable structure on the workstation, shadow evaluation against a recorded feed, and lowered parallel evaluation against the live feed.

Feeds arrive by leased line and, inside the wall, by cable. Latency from a dock report to a token is measured in minutes. A weight change can reassign a shift or hold a hull inside one reporting cycle. Retired cathode tubes from the halls are rebuilt into display boards in the lower city. They reproduce phosphor. They do not hold structure.

## Operational examples

Figures below illustrate the structure in service. They are not a published log.

### Dock clearance

A bulk carrier reports: class bulk, cargo code on the bonded list, three prior clearances in the quarter, declared value under the cargo threshold. The customs partition matches three conditions. Specificity orders them. Confidences combine to 0.82. The office structure emits a berth token and a discharge window inside one cycle. No clerk retypes the declaration.

### Failed clearance

The same class of hull reports with declared value above threshold and a prior failed-inspection flag. Negative factors drop the weight to 0.31. The network writes a null token and an exception. The hull stays at the buoy. A service-band clerk may open a manual review. The review does not rewrite structure. Until an engineer commits a delta and the office countersigns, the null stands.

### Bunk and water

A temporary-worker record matches an open shift. Bunk occupancy on the rib is 0.94. The slab is at its water cap. The labor structure fires one positive skill condition and two negative resource conditions. Net weight 0.44. The office emits a shift ticket and withholds the bunk token, raising a water-wait flag. The outcome is logged as an allocation. The landing sees a man with valid paper and no bed.

### Production scheduling

A mill reports three lines idle for tooling, two running, one waiting on a bonded component. The production structure matches open export orders against line state, tooling, and component availability. Running lines are assigned to a sealed electronics order. Tooling-idle lines are held for a garment lot. The component-wait line receives a null production weight and an exception. The office emits revised piece-rate tokens and a material-release token for the electronics order. The garment lot is deferred, not canceled. Deferral is a changed weight.

### Fulfillment

An export order enters the packing structure when its production weight crosses the completion threshold. Conditions include crate count, seal status, pre-clearance, and berth window. A match assigns a bay, a seal sequence, and a lighter token. If the berth window has closed, a negative factor withholds the loading token. Goods remain in the bonded cage. Fulfillment is incomplete until the loading token exists. A crate that leaves without one is logged as untokened movement, outside the model.

### Piece-rate

Completed units raise a worker’s credit weight only when skill and rate-card conditions clear. The office emits a credit token only if the weight passes the pay threshold and bunk or water flags are not blocking. A worker can finish a shift and receive nothing. The mill’s fulfillment of the order and the worker’s fulfillment of the wage are separate weights. They do not coincide by default.

### Service gates

Inspection slots, power windows, cooling, and bonded components are their own structure. No inspection token means a completed crate cannot enter the packing structure. No power-window token means a line remains at idle weight. Service fulfillment is a gate in the representation, not a side record.

## What does not run

The system accepts structured records and returns weights. It does not accept unconstrained queries. Appeals in ordinary language stop at clerks on the service band and do not enter the network. Bootleg listings that circulate in the lower stack are static transcriptions of earlier revisions. They lack current confidences and cannot be loaded. The live structure is not published below the band.

## Political status

The Zone Committee files the halls under regulation by the market inside the plan. Official statements do not claim abolition of the commodity. They claim its use for clearance and allocation. Changing structure is an upper-city procedure. Being subject to the weight that structure emits is the ordinary condition of a temporary permit.

## See also

- [Project Tiaojie](project-tiaojie.md)
- [Regulation Office](regulation-office.md)
- [Lixin Precision](lixin.md)
