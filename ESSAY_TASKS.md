# Competitive Differentiation Ranker: Task Definitions

This document defines the tasks that compose the Competitive Differentiation Ranker function. Each task evaluates a specific dimension of competitive differentiation, producing scores that together form the probability distribution output.

Because this is a **vector function** comparing multiple startup ideas simultaneously, each task must evaluate ALL items in the input array together and produce a comparative ranking. The tasks use `vector.completion` to generate a probability distribution across all items for each evaluation dimension.

---

## Task 1: Relative Uniqueness - Problem Space Novelty

**Purpose:** Evaluate which startup ideas occupy the most novel problem spaces relative to the others in the set.

**Description:** This task examines the fundamental problem each idea addresses and determines which problems are most distinct from others in the comparison set. Ideas targeting rarely-addressed problems or unexplored market gaps score higher. Ideas addressing problems already well-represented in the set score lower.

**Evaluation Criteria:**
- Is the problem fundamentally different from what others in the set are targeting?
- Does the idea address an underexplored market gap?
- How much conceptual overlap exists between this idea's problem space and others?
- Would solving this problem create a distinct market category?

**Output:** A probability distribution across all items indicating relative problem space novelty.

---

## Task 2: Relative Uniqueness - Solution Approach Originality

**Purpose:** Evaluate which startup ideas employ the most original solution approaches relative to the others.

**Description:** Even within similar problem spaces, solution approaches can diverge meaningfully. This task assesses whether each idea's technical approach, methodology, or product design represents a distinct path compared to alternatives in the set.

**Evaluation Criteria:**
- Does the solution approach diverge meaningfully from others in the set?
- Is the technical or methodological approach distinctive?
- Does the idea combine familiar elements in novel configurations?
- Would this approach be immediately recognizable as different from the alternatives?

**Output:** A probability distribution across all items indicating relative solution originality.

---

## Task 3: Relative Uniqueness - Business Model Innovation

**Purpose:** Evaluate which startup ideas have the most distinctive value capture mechanisms.

**Description:** This task examines how each idea plans to make money and whether that mechanism differs from alternatives. Subscription vs. transactional, platform vs. product, B2B vs. B2C—these distinctions create conceptual separation even when offerings seem similar on the surface.

**Evaluation Criteria:**
- Does the value capture mechanism differ from others in the set?
- Is the revenue model innovative or distinctive?
- Does the business model create different incentive structures?
- Would switching between these business models require fundamental restructuring?

**Output:** A probability distribution across all items indicating relative business model distinctiveness.

---

## Task 4: Relative Uniqueness - Target Segment Specificity

**Purpose:** Evaluate which startup ideas target the most distinctive customer segments.

**Description:** Who is being served matters as much as what is being offered. This task assesses whether each idea's target market creates differentiation from alternatives in the set.

**Evaluation Criteria:**
- Does the target segment differ meaningfully from others in the set?
- Is the segment definition specific enough to create a defensible niche?
- Would the same customer consider multiple ideas in the set, or are they targeting different people?
- Does the segment specificity create natural barriers to competition?

**Output:** A probability distribution across all items indicating relative target segment distinctiveness.

---

## Task 5: Defensibility and Moats - Network Effects Potential

**Purpose:** Evaluate which startup ideas have the strongest potential for network effects relative to others.

**Description:** This task assesses whether each idea becomes more valuable as more users join, and compares the strength and inevitability of these effects across the set.

**Evaluation Criteria:**
- Does the idea have same-side network effects (more users = more valuable for each user)?
- Does it have cross-side network effects (more of one user type = more valuable for another type)?
- How strong and inevitable are these effects compared to alternatives?
- Would network effects create winner-take-all dynamics?

**Output:** A probability distribution across all items indicating relative network effects strength.

---

## Task 6: Defensibility and Moats - Data Advantage Potential

**Purpose:** Evaluate which startup ideas will accumulate the most defensible proprietary data.

**Description:** This task assesses data moat potential—whether each idea will generate unique data that improves the offering over time and that competitors couldn't easily replicate.

**Evaluation Criteria:**
- Will the idea accumulate proprietary data that improves the offering?
- Is this data truly unique, or could competitors gather similar data?
- How quickly does the data accumulate and how long does it remain relevant?
- Does the data advantage compound over time?

**Output:** A probability distribution across all items indicating relative data advantage strength.

---

## Task 7: Defensibility and Moats - Switching Cost Creation

**Purpose:** Evaluate which startup ideas create the highest switching costs for users.

**Description:** This task assesses how painful it would be for users to switch away from each idea once adopted, creating stickier competitive positions.

**Evaluation Criteria:**
- What technical integration costs would switching require?
- What learning curve or data migration costs exist?
- Are there social or workflow disruption costs?
- How do these switching costs compare across the set?

**Output:** A probability distribution across all items indicating relative switching cost strength.

---

## Task 8: Defensibility and Moats - Brand and Trust Requirements

**Purpose:** Evaluate which startup ideas benefit most from trust-based moats.

**Description:** Some ideas inherently require deep trust (financial services, healthcare, security), creating moats for whoever establishes that trust first. This task assesses trust-based defensibility.

**Evaluation Criteria:**
- Does the idea operate in a domain requiring deep trust?
- Would establishing trust create durable competitive advantage?
- How easily could competitors commoditize the offering regardless of brand?
- Which ideas would benefit most from first-mover trust advantages?

**Output:** A probability distribution across all items indicating relative trust-based moat strength.

---

## Task 9: Defensibility and Moats - Technical and IP Barriers

**Purpose:** Evaluate which startup ideas have the strongest technical moats.

**Description:** This task assesses genuine technological innovations that would be difficult to reproduce—not just patents, but accumulated technical know-how that competitors couldn't easily replicate.

**Evaluation Criteria:**
- Are there genuine technological innovations that would be difficult to reproduce?
- Does the approach represent accumulated know-how beyond simple replication?
- How much technical capability gap exists between this idea and alternatives?
- Would competitors face significant R&D timelines to catch up?

**Output:** A probability distribution across all items indicating relative technical moat strength.

---

## Task 10: Competitive Positioning - Value Proposition Clarity

**Purpose:** Evaluate which startup ideas articulate the clearest and most distinctive value propositions.

**Description:** This task assesses whether each idea can articulate a clear reason why someone would choose it over alternatives in the set—not general appeal, but distinctive positioning.

**Evaluation Criteria:**
- Can the idea articulate why someone would choose it over these specific alternatives?
- Is the value proposition clear and memorable?
- Does the positioning avoid generic claims like "best for everyone"?
- Would a customer immediately understand why this is different?

**Output:** A probability distribution across all items indicating relative value proposition clarity.

---

## Task 11: Competitive Positioning - Segment Dominance Potential

**Purpose:** Evaluate which startup ideas can claim the clearest dominance in specific market segments.

**Description:** Even if an idea isn't universally superior, it can claim clear dominance in a specific segment. This task assesses niche dominance potential.

**Evaluation Criteria:**
- Can the idea claim clear dominance in a specific segment?
- Is it the obvious choice for a well-defined group, even if not for everyone?
- Does specialization create stronghold positioning?
- Would segment focus create defensible territory?

**Output:** A probability distribution across all items indicating relative segment dominance potential.

---

## Task 12: Competitive Positioning - Performance Dimension Superiority

**Purpose:** Evaluate which startup ideas win most clearly on specific performance dimensions.

**Description:** Different ideas optimize for different dimensions—speed, price, quality, convenience, status, safety, sustainability. This task assesses which ideas create the clearest superiority on their chosen dimensions.

**Evaluation Criteria:**
- What performance dimension does each idea optimize for?
- How clearly does it win on that dimension versus alternatives?
- Are the chosen dimensions important to meaningful customer segments?
- Does optimization create sustainable performance gaps?

**Output:** A probability distribution across all items indicating relative performance dimension superiority.

---

## Task 13: Competitive Positioning - Market Timing Advantage

**Purpose:** Evaluate which startup ideas are best positioned relative to market timing and urgency.

**Description:** This task assesses whether each idea addresses a problem whose urgency is increasing, creating timing-based positioning advantages.

**Evaluation Criteria:**
- Does the idea address a problem with increasing urgency?
- Is the market timing favorable or unfavorable?
- Would earlier entry create lasting advantages?
- How do timing considerations compare across the set?

**Output:** A probability distribution across all items indicating relative market timing advantage.

---

## Task 14: Cross-Idea Pivot Barriers - Technical Capability Gaps

**Purpose:** Evaluate how protected each idea is from others pivoting into its territory due to technical barriers.

**Description:** This task assesses whether pivoting toward each idea's territory would require technical capabilities the other teams are unlikely to develop.

**Evaluation Criteria:**
- Would pivoting to this idea's territory require rare technical skills?
- Is there accumulated domain expertise that couldn't be quickly replicated?
- How significant are the technical capability gaps between ideas?
- Would technical barriers prevent competitive convergence?

**Output:** A probability distribution across all items indicating relative protection from technical pivot attempts.

---

## Task 15: Cross-Idea Pivot Barriers - Business Model Incompatibility

**Purpose:** Evaluate how protected each idea is from others pivoting due to business model conflicts.

**Description:** This task assesses whether pivoting toward each idea's territory would require abandoning core assumptions of the other business models.

**Evaluation Criteria:**
- Would pivoting require abandoning core business model assumptions?
- Are there revenue model conflicts that prevent easy pivoting?
- Would structural changes alienate existing users or partners?
- How incompatible are the business models in the set?

**Output:** A probability distribution across all items indicating relative protection from business model pivot attempts.

---

## Task 16: Cross-Idea Pivot Barriers - Resource Requirements

**Purpose:** Evaluate how protected each idea is from others pivoting due to resource barriers.

**Description:** This task assesses whether pivoting toward each idea's territory would require resources that alternatives are unlikely to obtain.

**Evaluation Criteria:**
- Would pivoting require capital, time, or talent that others lack?
- Are there infrastructure requirements that create barriers?
- How significant are the resource gaps between ideas?
- Would resource requirements prevent competitive convergence?

**Output:** A probability distribution across all items indicating relative protection from resource-limited pivot attempts.

---

## Task 17: Cross-Idea Pivot Barriers - First-Mover Advantage Potential

**Purpose:** Evaluate which ideas would create the strongest barriers by moving first.

**Description:** This task assesses whether moving first would create barriers that prevent others from following—through partnerships, brand associations, or network effects.

**Evaluation Criteria:**
- Would moving first capture key partnerships or relationships?
- Would early brand associations be hard to displace?
- Would early network effects prevent later entrants?
- How significant are first-mover dynamics for each idea?

**Output:** A probability distribution across all items indicating relative first-mover advantage potential.

---

## Task 18: Holistic Differentiation Assessment

**Purpose:** Provide an integrated assessment of overall competitive differentiation across all dimensions.

**Description:** This final task synthesizes all previous evaluations into a holistic judgment of which ideas occupy the most defensible and distinctive competitive territory overall. It considers trade-offs between dimensions and produces the master probability distribution.

**Evaluation Criteria:**
- Considering all dimensions together, which ideas are most differentiated?
- How do strengths in one area compensate for weaknesses in another?
- Which ideas would be hardest for others to compete with or copy?
- If an investor had to choose, which ideas occupy the most valuable competitive positions?

**Output:** A probability distribution across all items representing overall relative competitive differentiation.

---

## Task Aggregation Strategy

The final output of the function aggregates across all tasks. Each task produces a probability distribution over the input items. The aggregation strategy should:

1. **Weight dimensions appropriately:** Not all dimensions contribute equally to differentiation. Moats and pivot barriers may be weighted higher than pure positioning clarity.

2. **Recognize trade-offs:** An idea strong in uniqueness but weak in defensibility differs from one strong in defensibility but weak in uniqueness.

3. **Produce a normalized distribution:** The final output must sum to approximately 1.0, representing a true probability distribution across the competitive set.

4. **Respect the holistic assessment:** Task 18's holistic judgment should serve as a calibrating force, ensuring the aggregation reflects intuitive comparative judgment.
