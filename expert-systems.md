![plate](plates/expert-systems.png)

# Expert systems in Liankou

**Expert systems in Liankou** are knowledge-based systems operated by the [Regulation Office](regulation-office.md) to score and allocate resources inside the [Liankou Special Zone](liankou.md). Each system comprises a domain knowledge base of production rules and an inference engine that applies those rules to live relational feeds from docks, mills, dormitories, and customs. The output is a weighted token. The systems form the machine layer of [Project Tiaojie](project-tiaojie.md).

The Zone Committee classifies the installation as a modernization of planning under regulation by the market. Operators call the crown halls the operations room. In the lower stack the outputs are called the weights.

## Background

Late-1970s and early-1980s expert systems encoded specialist procedures as IF–THEN production rules and executed them with a separate inference engine. Shells such as EMYCIN and OPS5 separated the knowledge base from the control regime (forward chaining, backward chaining, or mixed). Certainty factors or equivalent scoring attached to rules allowed ranked rather than binary conclusions. The principal bottleneck was knowledge engineering: extracting and maintaining the rules.

The Japanese Fifth Generation Computer Systems project (ICOT, 1982–1992) proposed machines oriented to knowledge information processing rather than numerical calculation: logic programming (Prolog and later concurrent variants), parallel inference, and large relational knowledge bases. Most results remained research prototypes.

Liankou adopted the production-rule architecture and the fifth-generation emphasis on inference over calculation, without joining an external institute. Initial Regulation Office links were telex. Clerks reduced reports by hand. Machine replacement occurred in the early 1980s. Inference boards were supplied by [Lixin Precision](lixin.md) until the firm’s seizure.

## Knowledge representation

Rules are production rules stored in relational tables. A typical customs rule takes the form: if vessel class, cargo code, prior clearance history, and declared value satisfy a conjunction, then assign clearance weight *w* with confidence *c*. Labor rules bind shift, skill code, bunk occupancy, and water quota. Rules carry maintenance metadata: authoring engineer, revision, and effective window.

The knowledge base is not a free-text corpus. It is a versioned set of relations. Domain boundaries are strict. A customs knowledge base contains no bunk predicates. Cross-domain reduction is performed only at the Regulation Office layer, which reads the scored outputs and applies a second, smaller rule set to emit the allocation token.

Knowledge engineers work in the upper city. A rule change is an administrative commit. The live base is not replicated below the service band.

## Inference

Engines support forward chaining over the incoming feed (new dock report fires all matching rules) and limited backward chaining for exception queries from the operations room. Conflict resolution is by specificity then by confidence score, a regime close to contemporary OPS5 practice. Parallel evaluation across rule partitions was introduced with the early-1980s hardware; the office describes this as the fifth-generation increment.

Scoring is not probabilistic in the later Bayesian sense. It is a certainty-factor calculus: each fired rule adjusts a running weight. The final weight is normalized and emitted as the token value. Failed tokens (weight below threshold) are logged as output events.

The systems do not perform general reasoning. An engine will not invent a predicate outside its knowledge base. Queries that fall outside maintained rules return a null weight and an exception flag.

## Hardware and deployment

Live knowledge bases and engines occupy climate-controlled halls in the finished crown. Inference hardware uses zone-maintained boards derived from the Lixin designs: multiple inference units over a shared relational store, with cathode monitoring stations for the operators. Power and cooling are crown services. The lower stack receives only the token stream.

Feeds arrive by leased line and, inside the wall, by dedicated cable drops. Update latency for a dock token is measured in minutes, not batch days. A weight change can reassign a shift or hold a hull inside a single reporting cycle.

Retired cathode tubes are rebuilt into display boards in the lower city. These reproduce phosphor characteristics. They do not execute live rules.

## Bootleg weights

Partial rule listings circulate in the lower stack, sold as aids to anticipate or counterfeit a token. They are static extracts. They do not connect to the live relational store and rarely reproduce current confidence values. Possession is not systematically prosecuted. The office does not publish diffs.

## Political and administrative status

The Zone Committee files the halls under regulation by the market inside the plan. Official descriptions do not claim abolition of commodity exchange. They claim accelerated clearance and labor allocation through maintained rules. Altering a rule is an upper-city procedure requiring a knowledge-engineer commit and an office countersign. Being subject to the resulting weight is the condition of a temporary permit.

## See also

- [Project Tiaojie](project-tiaojie.md)
- [Regulation Office](regulation-office.md)
- [Lixin Precision](lixin.md)

## Notes

Certainty-factor scoring follows the MYCIN-derived practice common in early-1980s shells. No claim is made to later probabilistic graphical models.
