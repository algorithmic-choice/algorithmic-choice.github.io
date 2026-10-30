# What Does an Algorithmic Choice Demonstrate?
## A Formal Analysis of Evidence, Comparison, and Preference Attribution

**Author:** Nuño Valenzuela  
**Research area:** Philosophy of artificial intelligence, formal logic, epistemology, and algorithmic decision-making  
**Publication type:** Independent research preprint (Paper 1)  
**Year:** 2026  
**Persistent identifier (DOI):** [10.5281/zenodo.23647211](https://doi.org/10.5281/zenodo.23647211)  
**Publication record:** [Zenodo](https://zenodo.org/records/23647211)

## Overview

**Does choosing an action demonstrate that an algorithm prefers it?** *What Does an Algorithmic Choice Demonstrate?* investigates this foundational question in the philosophy of artificial intelligence and the logic of algorithmic decision-making.

The paper distinguishes an **observed algorithmic selection**—the fact that a system outputs a particular action—from a **demonstrated preference**—a comparative claim that requires evidence and a valid rule of inference. Its central thesis is that an algorithm's output, considered alone, does not justify assertions that the selected alternative was shown to be superior, that all relevant alternatives were compared, or that the decision was globally optimal.

The work develops a **philosophical-computational formal framework** for determining what can legitimately be inferred from an algorithmic choice. It is a logical and epistemological contribution, not a claim that the paper empirically audits all artificial intelligence systems.

**Core finding in plain language:** An algorithmic choice tells us *what was selected*; evidence and explicit comparison standards determine *what has been demonstrated about that selection*.

## Abstract

An observed algorithmic choice is often interpreted as evidence that a system prefers the selected action to its alternatives. This paper questions that inference and develops a formal philosophical-computational account of evidence, comparison, and preference attribution. It establishes that selection alone does not logically entail demonstrated preference. Under a declared evidential standard and its attribution premises, a resolved comparison is necessary but not sufficient for a strict preference attribution: the comparison must also support the relevant conclusion. The framework distinguishes absence of sufficient justification from evidence of an opposite preference and separates local comparative claims from global optimality. Its contribution is a formal foundation for assessing the legitimacy and limits of conclusions drawn from algorithmic decisions. **The foundational result is formally established in Paper 1; its executable computational materialization and empirical examination have also been undertaken in subsequent research and will be presented in follow-up papers.**

## The research problem

Algorithms used for search, recommendation, planning, and automated decision-making can return an action even when computational budgets, available information, or architecture-specific procedures limit the comparisons they perform. The existence of an output therefore must be distinguished from evidence supporting a particular explanation or assessment of that output.

This paper asks:

1. **What can be established from an observed algorithmic decision?** The selection itself is observable; preference, superiority, and optimality require additional justification.
2. **Under what conditions does computational evidence support comparative claims?** Such claims depend on an identified comparator, a specified evidential standard, and the premises governing valid attribution.
3. **What distinguishes a successful execution from a justified conclusion?** Completing a computation and returning an answer do not independently establish the correctness or evidential sufficiency of every claim about that answer.

These questions concern the *epistemic status of an algorithmic decision*—what an observer is entitled to conclude—not whether an artificial system has human desires, consciousness, or psychological preferences.

## Central logical result

The central formula of Paper 1 is:

$$
\boxed{\operatorname{Selected}_h(b)\not\models DP_h^C(b,a)}
$$

**Plain-text form for indexing:** `Selected_h(b) does not logically entail DemonstratedPreference_h^C(b,a)`.

The symbols mean:

- **`Selected_h(b)`**: action **b** was selected in information state **h**.
- **`DP_h^C(b,a)`**: a **demonstrated preference** (*DP*) for action **b** over alternative **a**, relative to evidential standard **C**.
- **`h`**: the relevant information state at the time of the decision.
- **`a`, `b`**: distinct actions being compared.
- **`C`**: the explicitly declared standard governing the evidence required for an attribution.
- **`\not\models`**: **does not semantically entail**; the conclusion does not follow from selection alone.

**Interpretation:** Seeing an algorithm select **b** does not, without further premises or evidence, prove that **b** was shown to be preferable to **a**. This is a statement about the logical limits of an inference, not an assertion that the chosen action is necessarily wrong.

### Resolved comparison as a necessary condition

Within the formal attribution premises **Γ_C**, the paper establishes:

$$
\boxed{\Gamma_C\vdash\bigl(DP_h^C(b,a)\rightarrow RC_h^C(b,a)\bigr)}
$$

Here, **`RC_h^C(b,a)`** means that the comparison between **b** and **a** is **resolved under standard C**, and **`\vdash`** denotes derivability from the declared premises. Thus, **a demonstrated preference requires a resolved comparison under the governing framework**.

Under classical logic, the corresponding contrapositive is:

$$
\boxed{\Gamma_C\vdash\bigl(\neg RC_h^C(b,a)\rightarrow\neg DP_h^C(b,a)\bigr)}
$$

**Interpretation:** If the required comparison is established to be unresolved, a demonstrated-preference attribution cannot be derived under those premises. This does **not** prove that the opposite alternative is preferable. Nor does merely failing to find a certificate automatically establish the factual negation of a comparison.

### Why a resolved comparison is not enough

Even when a comparison is resolved, it may yield a tie or favor the other action. Accordingly, **comparison resolution is necessary but not sufficient for strict demonstrated preference**. The inference additionally depends on the comparative relation, admissibility, direction, and other conditions stipulated by the evidential framework.

The paper therefore distinguishes:

| Concept | What it establishes | What it does not establish by itself |
|---|---|---|
| **Observed selection** | Which action the algorithm returned. | Comparative superiority or optimality. |
| **Resolved comparison** | That a relation between two actions is established under a specified standard. | Strict preference for the selected action. |
| **Demonstrated preference** | A justified comparative attribution under the declared premises and evidential standard. | Global optimality across all possible actions or objectives. |
| **Global optimality** | That no admissible alternative improves on the selected action under the full objective. | It cannot be inferred from selection or a limited local comparison alone. |

## What the formal argument demonstrates

The paper establishes a precise distinction between a **fact of execution** and a **warranted comparative conclusion**. In particular, it shows why a selected output is insufficient to infer demonstrated preference and why comparison resolution must be assessed within stated evidential premises. The framework also makes clear that an unresolved comparison and a preference for the opposite action are not interchangeable claims.

Importantly, the work does not require that every valid comparison involve directly visiting or exhaustively evaluating every alternative. A suitable evidential standard may permit comparisons established through formally valid bounds or other justified inferences. The question is not simply *how many options were visited*, but *what the evidence actually warrants*.

## Completeness, optimality, and evidential limits

Claims about **completeness** require a defined domain and evidence that the relevant alternatives or cases have been accounted for, whether directly or through valid inferential mechanisms. Claims about **global optimality** demand stronger grounds than a locally favorable result: they require justification with respect to the full objective and all relevant admissible alternatives.

Paper 1 supplies a logical discipline for evaluating such claims, **not a universal certification algorithm for completeness or optimality**. A decision may be successful in the sense that a program terminates and outputs an answer without establishing every comparative property that a commentator might attribute to it. Conversely, a computational procedure may reach a good or optimal answer without having produced the particular evidence required for a specified demonstrated-preference claim.

The formal distinction prevents the following mistaken equivalences:

- **Selection ≠ demonstrated preference.**
- **Resolved comparison ≠ strict preference for the selected action.**
- **Lack of justification ≠ proof of an opposite preference.**
- **Locally justified superiority ≠ global optimality.**
- **Successful execution ≠ certification of every claim about the output.**

## Scientific contribution and relevance

Paper 1 contributes a **formal philosophical-computational vocabulary and logical foundation for evidence-based preference attribution**. It helps separate questions that are often conflated in assessments of artificial intelligence: *what a system did*, *what it compared*, *what it can demonstrate*, and *which stronger claims remain unjustified*.

This matters for research on **algorithmic decision-making, explainable artificial intelligence (XAI), interpretable AI, formal verification, computational epistemology, automated planning, search algorithms, and evidence-based AI accountability**. The framework encourages transparent statement of the comparator, the evidential standard, and the limits of the conclusion. It is also relevant to policy discussions about **trustworthy AI, traceability, transparency, and accountable automated decisions**, including in the European Union, without claiming that any particular legal instrument requires this specific formula or that the formula alone establishes regulatory compliance.

## Formal proof and subsequent computational materialization

**The logical result is formally demonstrated in Paper 1 under the stated framework and attribution premises.** The next stage of the research program is distinct: translating those formal conditions into executable checks over evidence produced by actual algorithmic runs.

**That computational materialization has already been carried out in follow-up research** through an evidence-based preference-attribution verifier and a trace-based experimental audit. Its implementation, conformance tests, reproducibility evidence, and experimentally observed scope and limitations **will be presented in subsequent papers**. The subsequent work does not replace the formal argument of Paper 1; it examines how that argument can be operationalized under explicitly defined standards.

For clarity, **Paper 1 is the formal theoretical foundation**. Implementation details, benchmark statistics, and computational validation results belong to those follow-up studies and are not presented here as if they were experiments reported in Paper 1.

## Scope and limitations

Paper 1 does **not** claim to demonstrate that:

- an artificial intelligence system has psychological preferences, intentions, or consciousness;
- every algorithm must explicitly inspect every possible action before a comparison can be resolved;
- a selection lacking demonstrated preference is necessarily incorrect;
- a justified local comparison establishes global optimality;
- the formula by itself is an executable verifier or a guarantee of software correctness;
- the proposed framework supplies a general legal, moral, or safety certification for deployed AI systems.

Its contribution is a **formal account of inference and justification**. Stronger operational or empirical claims require additional evidence and are addressed separately in subsequent work.

## Citation

**Suggested reference:**

Valenzuela, N. (2026). *What Does an Algorithmic Choice Demonstrate? A Formal Analysis of Evidence, Comparison, and Preference Attribution*. Zenodo preprint. https://doi.org/10.5281/zenodo.23647211

**BibTeX:**

```bibtex
@misc{valenzuela2026algorithmicchoice,
  author       = {Valenzuela, Nuño},
  title        = {What Does an Algorithmic Choice Demonstrate? A Formal Analysis of Evidence, Comparison, and Preference Attribution},
  year         = {2026},
  howpublished = {Zenodo preprint},
  doi          = {10.5281/zenodo.23647211},
  url          = {https://doi.org/10.5281/zenodo.23647211}
}
```

The Zenodo record is the canonical reference for the deposited work. Consult that record for the publication files and applicable reuse terms.

## Keywords and discoverability

**Primary terms:** algorithmic choice; demonstrated preference; preference attribution; resolved comparison; comparative evidence; evidential standards; epistemology of artificial intelligence; philosophical-computational framework; formal logic; algorithmic decision-making.

**Related research areas:** AI accountability; trustworthy artificial intelligence; explainable AI (XAI); interpretable machine learning; formal verification; computational epistemology; algorithmic transparency; decision provenance; search algorithms; global optimality; completeness; inference validity; AI governance.

**Concepts in Spanish:** elección algorítmica; preferencia demostrada; comparación resuelta; evidencia comparativa; justificación epistemológica; filosofía de la inteligencia artificial; verificación formal de decisiones algorítmicas.

---

**Key takeaway:** *An algorithmic choice is observable; a demonstrated preference is an evidence-dependent conclusion. Paper 1 proves the logical distinction, and subsequent research materializes and evaluates its computational verification. freedom for all mankind*
