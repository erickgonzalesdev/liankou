![plate](plates/project-tiaojie.png)

# Project Tiaojie

**Project Tiaojie** (Chinese: 调节工程; lit. “Regulation Project”) was the coordination project commissioned in 1978 for the [Liankou Special Zone](liankou.md). It built a real-time reporting and allocation loop from docks, mills, dormitories, and customs to a central operations room. The standing institution is the [Regulation Office](regulation-office.md). From the early 1980s the reduction step has been performed by the [expert systems](expert-systems.md).

Tiaojie is a cybernetic regulator that was required to clear an operating export port. The machine layer is not a set of separate techniques placed side by side. It is one substrate: operating knowledge held as editable symbolic structure, lowered without reinterpretation into a parallel evaluation network that scores the live feed and returns tokens.

## History

### Commission and clerical phase

Commissioned with the 1978 opening. The brief was to coordinate the zone without returning each decision to interior ministries. Reports arrived by telex and leased line. Clerks in the operations room aggregated them and issued quotas, bunk lists, and clearances. Published growth series used the room’s throughput as the exhibit.

### Machine reconstruction

In the early 1980s the clerical layer was replaced. The replacement was not a faster clerk. It was a representation in which a specialist procedure could be held as structure, edited interactively by engineers on single-user workstations, shadow-evaluated against a recorded feed, and then lowered into parallel evaluation against the live port. [Lixin Precision](lixin.md) supplied the inference boards. [Liankou Development](huanan-development.md) held the hall leases. The project name remained on the plaques. Operational control passed to the Regulation Office.

Private commercial courts in the upper city lay outside the brief. The lower stack lay inside it. A failed token is a Tiaojie event whether or not the project name is known on the landing.

## Cybernetic design

Tiaojie was specified as a regulator for a high-variety export port.

The port generates more states than a clerical staff can enumerate: hulls, cargo codes, shift combinations, bunk occupancy, water draw, inspection flags, tooling state, component availability. Variety is absorbed by collapsing each feed record, through the committed structure, into a weight. The weight is the regulated variable. The token is the signal returned to the point of action.

Reporting is recursive in form. A mill regulates its lines, the service band regulates the mills and slabs that report through it, and the operations room regulates the zone. Each level is supposed to absorb the variety proper to it and pass only exceptions upward. On the machine side the recursion is complete. Below the band it is not. The lower stack has no regulator of its own. Routine allocations and exceptions both arrive as tokens.

There is no separate alarm channel. Failed tokens, water-wait flags, and canceled shifts travel the same circuits as ordinary allocations. The operations room distinguishes them by exception flags. Positive feedback is a reassignment inside the same cycle. Negative feedback is a hold.

The operations room is the metacontroller. Cathodes show domain weights, flags, and clearance throughput. Operators do not rewrite structure from the floor. They may run a backward query through the committed structure, open a manual review, or request an engineer commit. The room’s public function is to keep export clearance inside the published window. Its private function is to keep the variety of the port from reaching the interior ministries.

The design assumes the committed structure is an adequate model of the port. Gaps produce null weights, not reorganization. Forged papers, unticketed movement, and landing bosses generate variety that never fully enters the feed. That variety is absorbed, if at all, by men with tools. Tiaojie regulates the port it can see.

## System architecture

### Reporting

Docks, mills, dormitory slabs, and customs desks emit structured status records. Transmission is by leased line to the wall and by internal cable thereafter. Records land in a store partitioned by domain.

### Structure and evaluation

Domain structure is authored on crown workstations as symbolic list structure. A commit that survives shadow replay against a retained clearance set is lowered into an evaluation network. The network matches the live feed, orders the conflict set by specificity then confidence, combines factors, and writes a weight. Independent partitions evaluate in parallel so that dock events resolve inside a turnaround. Cross-domain synthesis is a separate office structure applied after the domain weights exist. No open listener is exposed on the live path. No induction is in service.

### Allocation

The office structure emits the token: clearance, shift, bunk, water, material release, loading. Tokens return down the same circuits. Exception flags surface at the operations-room cathodes. Latency after reconstruction is intra-cycle for dock events.

### Hardware

Crown halls hold the stores, the evaluation networks, the operator cathodes, and the engineer workstations. Cooling and power are dedicated. No live network is sited below the service band.

## Legacy

Tiaojie is no longer a separate budget line. The name denotes the build. The Zone Committee retains it in official statements. Operators say the operations room. The lower city says the weights. The expert systems remain the scoring layer. The Regulation Office remains the allocating organ.

## See also

- [Expert systems in Liankou](expert-systems.md)
- [Regulation Office](regulation-office.md)
- [Liankou Special Zone](liankou.md)
- [Lixin Precision](lixin.md)
