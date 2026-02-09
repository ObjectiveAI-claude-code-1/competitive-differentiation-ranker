# Competitive Differentiation Ranker - Tasks

This document describes the key tasks the Competitive Differentiation Ranker function must perform. Each task evaluates a specific dimension of competitive differentiation across all startup ideas in the input set, contributing to the final probability distribution output.

---

## Task 1: Conceptual Territory Mapping

**Purpose**: Identify the conceptual space each idea occupies and detect overlaps between ideas in the set.

**Evaluation Focus**:
- What problem domain does each idea address?
- How does each idea frame its problem (novel framing vs. conventional framing)?
- Which ideas sit at unexplored intersections of domains?
- Which ideas challenge existing paradigms vs. accept industry orthodoxy?
- Which ideas occupy the same conceptual territory and would be seen as substitutes?

**Output**: For each idea, assess whether it occupies unique conceptual territory relative to the other ideas in the set. Ideas that cluster together should share uniqueness credit; ideas that stand alone should receive full uniqueness credit.

---

## Task 2: Network Effect Potential Assessment

**Purpose**: Evaluate the potential for network effects—where the product becomes more valuable as more people use it.

**Evaluation Focus**:
- Does the idea have potential for direct network effects (each user increases value for others)?
- Does it have potential for indirect network effects (users attract complementors)?
- Does it have potential for data network effects (more users = better product through ML/AI)?
- How strong are these network effects relative to other ideas in the set?
- Which ideas lack any network effect potential?

**Output**: Comparative ranking of network effect potential across all ideas in the set.

---

## Task 3: Data Moat Evaluation

**Purpose**: Assess whether each idea would generate proprietary, defensible data assets.

**Evaluation Focus**:
- Would the idea accumulate data that is hard to replicate?
- Is the data compounding (each data point increases value of existing data)?
- Is the data defensible (can't be scraped, purchased, or reverse-engineered)?
- How does each idea's data moat potential compare to others in the set?
- Which ideas would operate with commodity data only?

**Output**: Comparative ranking of data moat strength across all ideas in the set.

---

## Task 4: Switching Cost Analysis

**Purpose**: Evaluate the barriers that would prevent users from switching to alternatives.

**Evaluation Focus**:
- Would the idea create deep integration into customer workflows or tech stacks?
- Would users accumulate data that is difficult to export or use elsewhere?
- Would users invest in learning curves that don't transfer to alternatives?
- Would the idea create social graph lock-in or relationship dependencies?
- How do switching costs compare across ideas in the set?

**Output**: Comparative ranking of switching cost potential across all ideas in the set.

---

## Task 5: Scale Economy Assessment

**Purpose**: Evaluate whether each idea benefits from scale in defensible ways.

**Evaluation Focus**:
- Does the idea have supply-side economies (unit costs decrease with volume)?
- Does it have demand-side economies (value increases with customer base)?
- Does it have infrastructure economies (fixed cost investments create ongoing advantages)?
- How significant are these scale advantages relative to other ideas in the set?
- Which ideas have commodity economics with no scale benefits?

**Output**: Comparative ranking of scale economy potential across all ideas in the set.

---

## Task 6: Dominance Relationship Detection

**Purpose**: Identify whether any ideas in the set are clearly superior to or dominated by others.

**Evaluation Focus**:
- Does any idea solve the same problem more effectively than another idea in the set?
- Does any idea address a superset of another idea's use cases?
- Would any idea likely absorb another idea's market share over time?
- Are there clear winner-loser relationships within the set?
- Which ideas occupy independent spaces with no dominance relationships?

**Output**: Identify dominating and dominated ideas, adjusting scores accordingly (dominated ideas receive lower scores; dominating ideas receive higher scores).

---

## Task 7: Category Position Analysis

**Purpose**: Evaluate whether ideas are creating new categories or competing within existing ones.

**Evaluation Focus**:
- Is this idea attempting to create a new category or compete in an existing one?
- For category creators: How distinct is the new category from existing categories?
- For category competitors: How crowded is the category and what is the competitive intensity?
- Among ideas in the set, which are competing in the same category vs. different categories?
- Which ideas have the clearest blue ocean positioning (uncontested market space)?

**Output**: Comparative assessment of category positioning—rewarding category creators and penalizing ideas in crowded red ocean competition.

---

## Task 8: Positional Clarity Evaluation

**Purpose**: Assess how clearly and sharply each idea defines its competitive position.

**Evaluation Focus**:
- Does the idea have a clear target customer (knows who it's for and who it's not for)?
- Does it have an unambiguous value proposition (explainable in one sentence)?
- Is the positioning consistent (all elements reinforce the same position)?
- Does the idea avoid trying to be everything to everyone?
- How does positional clarity compare across ideas in the set?

**Output**: Comparative ranking of positional clarity across all ideas in the set.

---

## Task 9: Technical Pivot Barrier Assessment

**Purpose**: Evaluate how hard it would be for other ideas in the set to pivot and replicate each idea's technical approach.

**Evaluation Focus**:
- Does the idea require deep technical capabilities that take years to develop?
- Are the technical requirements shallow and easily copied?
- Is the technology commoditized with no real barriers?
- For each idea, how difficult would it be for the OTHER ideas in the set to pivot toward it?
- Which ideas have the strongest technical moats relative to this specific competitive set?

**Output**: For each idea, assess the technical barriers that protect it from the other ideas in the set pivoting into its space.

---

## Task 10: Domain Expertise Barrier Assessment

**Purpose**: Evaluate the domain knowledge requirements that protect each idea from competitive pivots.

**Evaluation Focus**:
- Does the idea require deep regulatory expertise that takes years to acquire?
- Does it require industry relationships and trust built over time?
- Does it require specialized knowledge from years of domain experience?
- For each idea, would the OTHER ideas in the set struggle to acquire necessary domain expertise?
- Which ideas have the highest domain expertise barriers relative to this specific competitive set?

**Output**: For each idea, assess the domain expertise barriers that protect it from the other ideas in the set pivoting into its space.

---

## Task 11: Business Model Barrier Assessment

**Purpose**: Evaluate whether business model structures would prevent ideas from pivoting toward each other.

**Evaluation Focus**:
- Would pivoting toward this idea create conflicting incentives for other ideas in the set?
- Would it threaten existing channel relationships of other ideas?
- Would it require cultural changes that other ideas' organizations couldn't make?
- Which ideas have business models that are structurally protected from competition by others in the set?

**Output**: For each idea, assess the business model barriers that protect it from the other ideas in the set pivoting into its space.

---

## Task 12: Resource and Time Barrier Assessment

**Purpose**: Evaluate the capital, time, and talent requirements that would prevent competitive pivots.

**Evaluation Focus**:
- Does the idea require significant capital investment that others in the set may not have?
- Does it have first-mover dynamics that create lasting advantages?
- Does it require specialized talent that is scarce?
- How do resource requirements compare across ideas in the set?
- Which ideas could be easily replicated with minimal resources by others in the set?

**Output**: For each idea, assess the resource and time barriers that protect it from the other ideas in the set pivoting into its space.

---

## Task 13: Holistic Differentiation Synthesis

**Purpose**: Synthesize all dimension scores into a final comparative ranking that represents genuine competitive differentiation.

**Evaluation Focus**:
- Integrate uniqueness, defensibility, positioning, and pivot barrier assessments
- Weight the interrelationships (uniqueness without defensibility is ephemeral; defensibility without uniqueness is meaningless)
- Produce a probability distribution that sums to ~1
- Ensure the distribution reflects the relative competitive positioning of each idea
- Handle edge cases: homogeneous sets should produce flat distributions; heterogeneous sets should evaluate standalone potential

**Output**: Final probability distribution across all ideas in the set, representing relative competitive differentiation. Higher scores indicate more differentiated and defensible positions.

---

## Task Interdependencies

The tasks above build upon each other:

1. **Foundation Layer** (Tasks 1-5): Establish the raw differentiation signals
   - Conceptual territory mapping
   - Moat assessments (network effects, data, switching costs, scale)

2. **Comparative Layer** (Tasks 6-8): Evaluate relative positioning within the set
   - Dominance relationships
   - Category positioning
   - Positional clarity

3. **Protection Layer** (Tasks 9-12): Assess barriers against competitive convergence
   - Technical pivot barriers
   - Domain expertise barriers
   - Business model barriers
   - Resource/time barriers

4. **Synthesis Layer** (Task 13): Combine all signals into final distribution
   - Weighted integration of all dimensions
   - Normalization to probability distribution

The function must evaluate all ideas simultaneously, not in isolation. Each task produces comparative assessments that inform the final probability distribution output.
