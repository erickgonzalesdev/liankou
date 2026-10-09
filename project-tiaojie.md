![plate](plates/project-tiaojie.png)

# Project Tiaojie

**Project Tiaojie** (Chinese: 调节工程; lit. “Regulation Project”) was the cybernetic coordination project commissioned in 1978 for the [Liankou Special Zone](liankou.md). It created a recursive reporting loop from docks, mills, dormitories, and customs to a central operations room, with allocations returned as tokens. The standing body is the [Regulation Office](regulation-office.md). From the early 1980s the reduction step has been performed by [expert systems](expert-systems.md).

Tiaojie corresponds to earlier real-time economic coordination experiments. It differed in mandate: the system was required to clear a functioning export port rather than demonstrate feasibility. Fifth-generation inference methods that remained laboratory systems elsewhere were placed in continuous operation.

## History

### Commission and clerical phase (1978–early 1980s)

Commissioned at the zone’s opening. The brief required coordination of port, production, and labor allocation without per-decision referral to interior ministries. Implementation used telex and leased-line circuits. Clerks in the operations room (located in the sector that became the upper city) aggregated reports and issued quotas, bunk lists, and clearance orders. Published growth figures cited the room’s throughput.

### Machine reconstruction (early 1980s)

The clerical aggregation layer was replaced by domain expert systems. Knowledge bases were authored inside the zone. Inference hardware drew on boards supplied by [Lixin Precision](lixin.md). Hall leases were held by [Liankou Development](huanan-development.md). Parallel rule evaluation was introduced to meet cycle-time targets derived from dock turnaround. The project designation remained on plaques; day-to-day control resided with the Regulation Office.

The lower stack lay inside the original data perimeter. Upper-city private commercial courts did not. A failed token continues to be logged as a project event irrespective of local awareness of the name Tiaojie.

## Cybernetic design

Tiaojie was specified as a cybernetic regulator for a high-variety export port, not as a batch planning system. The design borrows the vocabulary and the control claims of 1970s management cybernetics (real-time feedback, variety engineering, recursive organization) and applies them inside the zone’s dual-track economy.

### Variety

The port generates more states than a clerical staff can enumerate: hulls, cargo codes, shift combinations, bunk occupancy, water draw, inspection flags. The project’s first claim was that this variety had to be absorbed in the operations room rather than attenuated by delay or by referral to interior ministries. Early attenuation was clerical aggregation. After the early-1980s reconstruction, attenuation is performed by the domain expert systems, which collapse a feed record into a weight. The office treats the weight as the regulated variable.

### Recursion

Reporting is recursive in the cybernetic sense. A mill is a regulator for its lines, the service band is a regulator for the mills and dormitory slabs that report through it, and the operations room is the regulator for the zone. Each level is supposed to handle the variety proper to it and pass only exceptions upward. In practice the lower stack has no functioning regulator of its own. Exceptions and routine allocations both arrive as tokens. The recursion is complete on the machine side and incomplete on the human side below the band.

### Feedback and the token

The token is the feedback signal. A clearance weight, a shift assignment, or a bunk refusal is the system’s output returned to the point of action. Positive feedback appears as a reassignment inside the same cycle (idle line cancels tickets and opens others). Negative feedback appears as a hold (weight below threshold, hull remains at the buoy). There is no separate “algedonic” channel in the published design. Pain signals—failed tokens, water-wait flags, shift cancellations—travel on the same circuits as ordinary allocations. The operations room distinguishes them by exception flags, not by a dedicated alarm line.

### Operations room

The operations room in the upper city is the system’s metacontroller. Cathode stations display domain weights, exception flags, and clearance throughput. Operators do not rewrite rules from the floor. They may initiate a backward-chaining query, open a manual review, or request a knowledge-engineer commit. The room’s public function is to keep export clearance inside the published window. Its private function is to keep the variety of the port from reaching the interior ministries.

### Limits of the cybernetic claim

The design assumes that the rule bases are an adequate model of the port. Rule gaps produce null weights rather than adaptive reorganization. The lower stack generates variety (forged papers, unticketed movement, landing bosses) that never fully enters the relational store. That variety is absorbed, if at all, by men with tools, not by the regulator. The project therefore regulates the port it can see. The port beneath the service band is only partly inside the model.

## System architecture

### Reporting layer

Docks, mills, dormitory slabs, and customs desks emit structured status records (vessel, cargo, shift, occupancy, quota consumption). Transmission is by leased line to the wall and by internal cable thereafter. Records land in a relational store partitioned by domain.

### Inference layer

Each domain expert system reads its partition, fires production rules, and writes a scored weight plus confidence. The engine is a Rete-derived forward-chaining production system. Working memory is the current feed. Conflict resolution is by specificity then confidence. Certainty factors are combined in the MYCIN manner and normalized. Parallel partition scheduling, added for dock cycle times, is the component the office attributes to fifth-generation practice. Backward chaining exists for operator exception queries only. Cross-domain synthesis is reserved to the office rule set. No rule induction is in service. All committed rules are hand-authored through the upper-city shell and its shadow-replay checker.

### Allocation layer

The Regulation Office applies a supervisory rule base to the domain weights and emits the token (clearance, shift, bunk, water). Tokens are pushed back down the same circuits. Latency target after reconstruction was intra-cycle for dock events. Exception flags (null weight, rule-gap) surface at the operations room cathode stations.

### Hardware

Crown halls contain the relational stores, inference units, and operator stations. Cooling and power are dedicated. No live engine is sited below the service band.

## Performance and limits

The system’s public metric is export clearance time. Internal metrics include rule-firing latency, token failure rate, and knowledge-base revision frequency. It does not optimize an open utility function. It applies the maintained rules. Rule gaps produce null weights rather than imputed decisions. Knowledge-engineering throughput remains the binding constraint on adding domains.

## Legacy

Budgetary status as a distinct project ended after the machine reconstruction. The name denotes the overall build. The Zone Committee retains it in official language. Operational reference is to the operations room; lower-stack reference is to the weights. Expert systems continue as the scoring layer; the Regulation Office continues as the allocating authority.

## See also

- [Expert systems in Liankou](expert-systems.md)
- [Regulation Office](regulation-office.md)
- [Liankou Special Zone](liankou.md)
- [Lixin Precision](lixin.md)
