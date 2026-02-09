# Competitive Differentiation Ranker: Task Definitions

This document defines the key tasks that the Competitive Differentiation Ranker function must perform. Each task evaluates a specific dimension of competitive differentiation across all startup ideas in the input batch, contributing to the final probability distribution output.

The function is a **vector function** that takes an array of startup ideas (each potentially multimodal: text, image, audio, video, or composite) and produces a vector of scores summing to ~1, representing relative differentiation.

---

## Task 1: Conceptual Territory Mapping

**Purpose:** Identify what conceptual space each startup idea occupies and measure the distance between ideas.

**Description:** Evaluate all startup ideas simultaneously to determine their conceptual positions. For each idea, identify the core problem domain, solution approach, target market, and strategic framing. Then assess how conceptually distant each idea is from all others in the batch.

**What to Consider:**
- What problem domain does each idea address? (healthcare, fintech, productivity, social, etc.)
- What is the core solution approach? (AI/ML, marketplace, SaaS, hardware, etc.)
- Who is the target customer? (enterprise, SMB, consumer, specific verticals)
- How is the idea framed and positioned? (what category does it claim?)
- How far is each idea from the "centroid" of all ideas in the batch?
- Are there clusters of similar ideas, with some ideas isolated?

**Evaluation Goal:** Ideas that occupy unique conceptual territory—far from other ideas in the batch—should receive higher relative scores. Ideas clustered with others should share their differentiation value.

---

## Task 2: Problem Novelty Assessment

**Purpose:** Evaluate whether each idea addresses a novel problem compared to others in the batch.

**Description:** Compare the problems being solved across all ideas. Some ideas may tackle well-known problems (scheduling, payments, messaging) while others address emerging or underexplored problems. Evaluate how novel each problem is relative to the other problems in the batch.

**What to Consider:**
- Is this problem frequently addressed by startups, or is it underexplored?
- How many other ideas in this batch address similar problems?
- Does the idea identify a problem that others haven't recognized?
- Is the problem framing itself innovative (seeing an old problem in a new way)?
- Does the problem exist in an emerging space (new technology, regulation, behavior)?

**Evaluation Goal:** Ideas solving problems that no other idea in the batch addresses should score higher. Ideas solving the same problem as others should share their problem-novelty score.

---

## Task 3: Solution Approach Distinctiveness

**Purpose:** Evaluate how unique each idea's solution approach is compared to others.

**Description:** Even ideas solving similar problems may use radically different solution approaches. Compare the technical and strategic approaches across all ideas to determine which have truly distinctive methods.

**What to Consider:**
- What technologies or methods does each solution employ?
- Are multiple ideas using similar technical stacks or architectures?
- Does any idea use an unconventional or unexpected approach to its problem?
- Is the solution approach hard to categorize or does it create a new category?
- Does the approach combine elements from different domains in novel ways?

**Evaluation Goal:** Ideas with solution approaches unlike any other in the batch should score higher. Ideas using common approaches (yet another AI chatbot, yet another marketplace) should receive lower relative scores.

---

## Task 4: Target Market Differentiation

**Purpose:** Assess how distinct each idea's target market is from the others.

**Description:** Compare the intended customers across all ideas. Ideas targeting the same market segments compete more directly than those targeting different segments.

**What to Consider:**
- What specific customer segment does each idea target?
- Are there multiple ideas targeting the same segment (e.g., enterprise SaaS, Gen Z consumers)?
- How narrow or specific is each idea's target market definition?
- Does any idea target an underserved or overlooked market?
- Would the target customers of different ideas ever be the same people/companies?

**Evaluation Goal:** Ideas targeting unique, non-overlapping markets should score higher. Ideas competing for the same customers should share their target-market differentiation value.

---

## Task 5: Network Effects Potential

**Purpose:** Evaluate which ideas have the potential for network effects that create defensible moats.

**Description:** Compare the structural potential for network effects across all ideas. Ideas with strong network effect potential have inherent defensibility that compounds over time.

**What to Consider:**
- Does the product become more valuable as more users join?
- Are there two-sided marketplace dynamics that create lock-in?
- Does user-generated content or data create compounding value?
- Would users have reasons to invite or depend on other users?
- How strong are the network effects compared to other ideas in the batch?

**Evaluation Goal:** Ideas with stronger network effect potential should receive higher relative defensibility scores. Ideas with no network effects should receive lower scores on this dimension.

---

## Task 6: Technical Moat Depth

**Purpose:** Assess the technical complexity and barriers to replication for each idea.

**Description:** Compare the technical defensibility across all ideas. Some ideas require deep technical expertise, proprietary algorithms, unique data, or years of R&D that competitors cannot easily replicate.

**What to Consider:**
- Does the solution require rare technical expertise?
- Is there significant R&D or engineering complexity?
- Does the idea depend on proprietary data or unique data access?
- Are there patents, trade secrets, or algorithmic innovations?
- How long would it take a well-funded competitor to replicate the technology?
- How do the technical moats compare across all ideas in the batch?

**Evaluation Goal:** Ideas with deeper technical moats should score higher on defensibility. Ideas using commodity technology should score lower relative to others with technical advantages.

---

## Task 7: Regulatory and Compliance Barrier Evaluation

**Purpose:** Identify which ideas operate in spaces with high regulatory barriers that protect incumbents.

**Description:** Compare the regulatory environments across all ideas. Ideas in heavily regulated spaces (healthcare, finance, education, transportation) have natural moats that competitors must also navigate.

**What to Consider:**
- Does the idea operate in a regulated industry?
- Are there licenses, certifications, or approvals required?
- Has the team demonstrated understanding of regulatory requirements?
- Would new entrants face significant compliance costs?
- How do regulatory barriers compare across all ideas in the batch?

**Evaluation Goal:** Ideas in regulated spaces with demonstrated compliance understanding should score higher on defensibility. Ideas in unregulated commodity markets should score lower on this dimension.

---

## Task 8: Switching Cost and Lock-in Assessment

**Purpose:** Evaluate the switching costs and ecosystem lock-in potential for each idea.

**Description:** Compare how sticky each product would be once adopted. Ideas that integrate deeply into customer workflows, accumulate valuable customer data, or create high switching costs have stronger defensibility.

**What to Consider:**
- How deeply does the product integrate into existing workflows?
- Would customers lose valuable data or history by switching?
- Are there network effects within the customer's organization?
- How painful would migration to a competitor be?
- How do switching costs compare across all ideas in the batch?

**Evaluation Goal:** Ideas with higher switching costs and deeper integration should score higher. Ideas that are easy to replace should score lower on this dimension.

---

## Task 9: Value Proposition Clarity Comparison

**Purpose:** Compare how clearly each idea articulates its value proposition.

**Description:** Evaluate the clarity, specificity, and crispness of each idea's value proposition relative to others. Clear value propositions signal deep market understanding and strong positioning.

**What to Consider:**
- Can the idea be summarized in one clear sentence?
- Is the target customer and benefit immediately apparent?
- Is there buzzword inflation or vague language?
- Does the pitch demonstrate specific understanding of customer pain?
- How does the clarity compare across all ideas in the batch?

**Evaluation Goal:** Ideas with crystal-clear value propositions should score higher on competitive positioning. Ideas with vague or confusing pitches should score lower.

---

## Task 10: Strategic Coherence Evaluation

**Purpose:** Assess whether each idea's strategy is internally coherent and well-reasoned.

**Description:** Compare the strategic coherence across all ideas. A coherent strategy aligns target market, solution approach, go-to-market, and business model in ways that reinforce each other.

**What to Consider:**
- Does the target market match the product approach?
- Is the go-to-market strategy appropriate for the customer segment?
- Does the business model make sense for the solution type?
- Are there contradictions or misalignments in the strategy?
- How does strategic coherence compare across all ideas?

**Evaluation Goal:** Ideas with fully coherent strategies should score higher. Ideas with strategic contradictions or misalignments should score lower relative to others.

---

## Task 11: Market Timing Assessment

**Purpose:** Evaluate whether each idea is well-timed for current market conditions.

**Description:** Compare market timing across all ideas. Ideas that are too early face education costs; ideas that are too late face entrenched competition. The best-timed ideas identify inflection points.

**What to Consider:**
- Is there a recent change (technology, regulation, behavior) enabling this idea now?
- Is the market ready for this solution, or does it require education?
- Are incumbents already established in this space?
- Is there evidence of market pull (emerging demand, failed predecessors)?
- How does market timing compare across all ideas in the batch?

**Evaluation Goal:** Ideas with superior market timing should score higher on competitive positioning. Ideas that are mistimed (too early or too late) should score lower.

---

## Task 12: Execution Credibility Signals

**Purpose:** Assess signals of execution capability evident in each pitch.

**Description:** Compare execution credibility across all ideas based on the quality, specificity, and confidence of the pitches. Well-prepared pitches with specific plans signal teams that can deliver.

**What to Consider:**
- Is the pitch well-prepared and professional?
- Are there specific metrics, milestones, or plans mentioned?
- Does the pitch demonstrate deep domain expertise?
- In audio/video: Is the delivery confident and competent?
- How does execution credibility compare across all ideas?

**Evaluation Goal:** Ideas demonstrating stronger execution credibility should score higher. Ideas with weak or poorly-prepared pitches should score lower on this dimension.

---

## Task 13: Technical Pivot Barrier Analysis

**Purpose:** Evaluate how hard it would be for other ideas in the batch to pivot into each idea's technical space.

**Description:** For each idea, assess how difficult it would be for the other ideas to acquire the technical capabilities needed to compete directly. High technical pivot barriers protect differentiation.

**What to Consider:**
- Would competitors need entirely different technical stacks?
- Would they need to hire different kinds of engineers?
- Would they need years of R&D to build comparable technology?
- Would they need access to data they don't have?
- How asymmetric are the technical pivot barriers between ideas?

**Evaluation Goal:** Ideas that are technically hard for others to pivot into should score higher. Ideas that others could easily expand into should score lower.

---

## Task 14: Market Pivot Barrier Analysis

**Purpose:** Evaluate how hard it would be for other ideas to pivot into each idea's market position.

**Description:** For each idea, assess how difficult it would be for others to build the customer relationships, brand positioning, and go-to-market capabilities to compete directly.

**What to Consider:**
- Would competitors need entirely different customer relationships?
- Would they need different brand positioning or marketing approaches?
- Would they need different sales motions or distribution channels?
- Would they confuse their existing customers by pivoting?
- How asymmetric are the market pivot barriers between ideas?

**Evaluation Goal:** Ideas that are hard for others to pivot into from a market perspective should score higher. Ideas that are easy to expand into should score lower.

---

## Task 15: Strategic Pivot Barrier Analysis

**Purpose:** Evaluate how hard it would be for other ideas to pivot into each idea's strategic space.

**Description:** For each idea, assess whether others could strategically justify a pivot into this space without abandoning their core identity, confusing investors, or diluting focus.

**What to Consider:**
- Would a pivot make strategic sense for other ideas, or would it be a distraction?
- Would pivoting require abandoning current strategic positioning?
- Would a pivot confuse existing investors or stakeholders?
- Is the strategic distance too great for a credible pivot?
- How asymmetric are the strategic pivot barriers between ideas?

**Evaluation Goal:** Ideas that are strategically isolated from others should score higher. Ideas that are natural pivot targets for others should score lower.

---

## Task 16: Similarity Clustering and Duplicate Detection

**Purpose:** Identify clusters of similar ideas and near-duplicates that should share differentiation value.

**Description:** Group ideas that are highly similar to each other. Ideas within a cluster compete directly and should split their combined differentiation value. Isolated ideas outside clusters retain their full differentiation.

**What to Consider:**
- Are any ideas essentially duplicates or near-duplicates?
- Are there clusters of ideas targeting the same market with similar approaches?
- How many distinct competitive spaces are represented in the batch?
- Which ideas stand alone, and which exist in crowded clusters?

**Evaluation Goal:** Identify the cluster structure of the batch to ensure similar ideas share differentiation value appropriately.

---

## Task 17: Holistic Differentiation Synthesis

**Purpose:** Combine all evaluation dimensions into a final relative differentiation ranking.

**Description:** Synthesize scores from all previous tasks—uniqueness, defensibility, competitive positioning, and pivot barriers—into a single probability distribution that represents overall competitive differentiation.

**What to Consider:**
- How do the four pillars (uniqueness, defensibility, positioning, pivot barriers) combine?
- Are there ideas that score highly on some dimensions but poorly on others?
- Which ideas have the most balanced, robust differentiation?
- How should the scores be normalized to sum to ~1?

**Evaluation Goal:** Produce a final probability distribution where each score represents the idea's share of total differentiation value in the batch.

---

## Summary

The Competitive Differentiation Ranker performs 17 key tasks:

| # | Task | Pillar |
|---|------|--------|
| 1 | Conceptual Territory Mapping | Relative Uniqueness |
| 2 | Problem Novelty Assessment | Relative Uniqueness |
| 3 | Solution Approach Distinctiveness | Relative Uniqueness |
| 4 | Target Market Differentiation | Relative Uniqueness |
| 5 | Network Effects Potential | Defensibility |
| 6 | Technical Moat Depth | Defensibility |
| 7 | Regulatory and Compliance Barriers | Defensibility |
| 8 | Switching Cost and Lock-in | Defensibility |
| 9 | Value Proposition Clarity | Competitive Positioning |
| 10 | Strategic Coherence | Competitive Positioning |
| 11 | Market Timing Assessment | Competitive Positioning |
| 12 | Execution Credibility Signals | Competitive Positioning |
| 13 | Technical Pivot Barriers | Pivot Barriers |
| 14 | Market Pivot Barriers | Pivot Barriers |
| 15 | Strategic Pivot Barriers | Pivot Barriers |
| 16 | Similarity Clustering | Cross-Cutting |
| 17 | Holistic Differentiation Synthesis | Integration |

Each task evaluates all ideas simultaneously and contributes to the final probability distribution output.
