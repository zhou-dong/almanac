# Facts — When Many Cells Move as One

*This file holds facts specific to this chapter.*

## Overview

This chapter opens after the Cryogenian "Snowball Earth" glaciations, in the Ediacaran (imprecisely captioned in the script as "600 million years ago, end of the Proterozoic" — that's actually mid-Ediacaran, not the Proterozoic boundary). Multiple multicellular lineages have arisen independently by now — sponges, cnidarians, and bilaterians — and the chapter follows a fictional composite early bilaterian, Bila, small and soft-bodied with a front/back body axis enabling directional movement. The corrected framing (per the script's own flagged errata) is that tunable chemical synapses already exist earlier, in cnidarians' nerve nets — so that's not new here. What Bila actually introduces is **centralization**: a primitive ganglion that gathers sensory signals from across the whole body into one place, sums them with weights and a bias, and produces a single output — the chapter's biology-first analogy to Rosenblatt's perceptron. Internal-state signals like hunger or arousal plausibly feed into that same convergence point alongside external senses. This is the story's first appearance of *one place where many signals become one decision* — a real structural leap from ch1's single fixed sensor-to-motor loop, even though the underlying tunable-junction idea (the synapse) isn't new.

> **Status note:** this chapter's own script (`scripts/ch2-when-many-cells-move-as-one.md`) contains an unresolved `⚠️ UNRESOLVED` block (as of 2026-07-31) flagging that §1.1 and §1.2 of the current draft make claims that do not survive scrutiny. This facts file records the **corrected** framing below — Part 1/Part 2 of the script as currently written still needs a rewrite to match it. See "Open questions" for the specific sections affected.

## Setting — Earth history

- The Ediacaran period follows a series of severe glaciations ("Snowball Earth" events, the Cryogenian glaciations) during which much or all of Earth was covered in ice, then thawed. (established)
- Atmospheric oxygen built up gradually over billions of years, produced by bacterial (cyanobacterial) photosynthesis, prior to the Ediacaran. (established)
- The script's caption dates this chapter's opening to "600 million years ago, end of the Proterozoic." This is **imprecise**: the Proterozoic eon actually ends at ~538.8 Mya (its final period, the Ediacaran, runs roughly 635–538.8 Mya), so 600 Mya falls within the Ediacaran/late Proterozoic, not at its boundary. (established — dating correction; the ICS chronostratigraphic chart is the reference)

## Early multicellularity — divergent lineages

- Multiple multicellular lineages arose independently (or via independent elaborations) from single-celled ancestors in this general era, including sponges, cnidarians ("radiatans" in the script — anchored, radially symmetric forms such as corals, sea anemones, and jellyfish), and bilaterians (animals with a front/back, left/right body axis). (established, at the level of "these lineages diverged and coexist," though exact branching order and timing among early animal lineages remains an active research area)
- Cnidarian descendants alive today include corals, sea anemones, and jellyfish. (established)

## Bila — the chapter's fictional early bilaterian

- Bila is a fictional composite organism, analogous to Ch0's LUCA-like framing — not a specific documented fossil species. (framing, not a factual claim)
- The script's date of "555 million years ago" for Bila lands close to some of the earliest confirmed bilaterian trace fossils and body fossils (e.g., *Ikaria wariootia*, dated to roughly this period), and is plausibly inspired by that fossil record, but the script does not claim Bila *is* a specific named species. (plausible as an illustrative date; should not be presented as a specific fossil's date unless the script explicitly names a real analog)
- Small, soft-bodied, with a front/back body axis (bilateral symmetry) enabling directional movement — a general, established feature of early bilaterians as a group, not specific to any one species. (established as a general characteristic)

## Cnidarian ("radiatan") nervous system — corrected framing

*This section supersedes the framing in the script's current §1.1, which the script's own unresolved note flags as incorrect.*

- Nerve cells (neurons) appear earlier than bilaterians, in the cnidarian lineage. Cnidarians possess a **nerve net**: neurons distributed through the body with no central integration point. Stimulation at one location propagates outward through the net; there is no single site where signals from the whole body converge into one output. (established — high confidence per the script's own fact-check note)
- Cnidarians already have real chemical synapses between neurons, with variable transmission strength between different synapses. (established — high confidence per the script's own fact-check note)
- Consequence: the *tunable synapse* (a weight sitting in a connection, adjustable independently of the sensor) predates bilaterians and is not Bila's/bilaterians' innovation. What bilaterians add is **centralization** — a specific place where signals from across the body converge into one decision — not the synapse itself. (established, given the above)

## Signal propagation — chemistry vs. wiring (used as narrative device)

- Diffusion-based (chemical) signaling time scales with the square of the distance traveled — a well-established physics fact (diffusion times generally scale as distance²/diffusivity). (established as a general physical principle)
- The script uses this to argue that at a body scale roughly 1000× a bacterium's, diffusion-only signaling becomes impractical (minutes-to-hours to cross a body), motivating wired (synaptic/electrical) signaling for larger, coordinated bodies. (plausible as a narrative/order-of-magnitude argument; the specific "~1000×" scale factor and resulting time estimates are illustrative, not sourced figures, and should not be presented as precise)

## Bila's nervous cluster (ganglion) and the perceptron mapping

- A primitive ganglion — a small cluster of neurons receiving sensory input from across the body and sending motor output to muscles — is a real, established category of early nervous system organization in simple bilaterians. (established as a general biological structure; not verified here for any specific fossil species)
- The chapter maps this ganglion onto a perceptron (multiple weighted inputs, summed, plus a bias, producing a binary output) as a pedagogical analogy — biology first, math named second. This is a teaching framing, not a claim that early bilaterian ganglia are historically/literally identical to Rosenblatt's model. (plausible as a teaching model, explicitly flagged as a simplification in the script itself: "Bila's real cluster isn't a single perceptron... it is a small network of them")

## Math model

- Bila's ganglion is modeled with the **same formula as ch1's**: `signal ≈ Σ(wᵢ · xᵢ) + bias`, then `motor state ≈ threshold(signal)` (`ch1-the-world-before-learning.md § Math model`). Mathematically this is not a new equation — it's the same weighted-sum-plus-bias-plus-threshold shape recurring at a new physical scale, and the chapter should say so rather than presenting it as a fresh invention.
- What changes is what each `xᵢ` and `wᵢ` physically *are*. In ch1, the "many inputs" are receptor types on **one cell**, combined implicitly inside that cell via a single shared diffusible chemical (CheY-P), with weights fixed by gene-expression copy-numbers. In ch2, the inputs are **separate sensory neurons scattered across a whole multicellular body**, wired through discrete, individually tunable chemical synapses into one ganglion — a real multicellular convergence point, not one cell's internal chemistry. `xᵢ` can now include internal-state signals (hunger, arousal) alongside external senses, feeding the same convergence point.
- This tunability is **not new to Bila** — cnidarian nerve nets already have variable-strength synapses (`§ Cnidarian ("radiatan") nervous system`) — and nothing at this stage adjusts those weights based on outcome; there is no training/learning process yet. What is new is the **convergence**: for the first time, many separately-wired, individually-tunable junctions all feed into one place, producing one shared decision, rather than each sensor driving behavior locally or the whole net just propagating a stimulus outward. (plausible pedagogical simplification — the ganglion-as-perceptron mapping is a teaching framing per `§ Bila's nervous cluster`, not a claim that early bilaterian ganglia perform this exact arithmetic)

## Internal state signals (hunger, arousal)

- The claim that internal-state signaling (e.g., hunger signals from a gut, body-wide arousal under threat) co-evolved alongside nervous system integration in early bilaterians is a reasonable evolutionary inference but is stated flatly in the script with no citation. (plausible, not verified against a specific source)

## History — Rosenblatt and the perceptron

- Frank Rosenblatt is credited with formulating the perceptron and built a hardware implementation (the Mark I Perceptron) capable of learning, in the late 1950s. (established, widely documented)
- The script's specific date, "1958," and the quote attributed to Rosenblatt ("the simplest possible model of a neuron") are stated without citation — the underlying history is well documented, but this exact date and quote should be checked against Rosenblatt's original publications/reports before being treated as precisely sourced. (needs verification — established in broad strokes, unverified in exact wording/date)

## Framing notes

- Bila's foraging (moving toward food) and escape/withdrawal (moving away from danger) are plausibly still **fixed reflex arcs** at this stage — the same fundamental mechanism as ch1's chemotaxis (a fixed weighted sum, thresholded into a motor output), just now converged through a ganglion rather than driven by one cell's receptor cluster. The weights producing these behaviors are set by development/gene expression, shaped by natural selection *across generations*, not adjusted by any individual organism's own experience within its lifetime. A behavior can look adaptive and goal-directed from the outside while still being entirely fixed on the inside — evolution did the "learning," not the individual. (plausible — consistent with reflex-circuit models of simple bilaterian behavior; not a claim that Bila specifically lacks any capacity for individual learning, just that none is needed to explain foraging/escape at this stage)
- Genuine individual-lifetime learning about food and danger — associating a specific stimulus with an outcome and changing behavior because of it (classical/operant conditioning) — is documented in some invertebrates (e.g., Aplysia, various insects), but requires outcome-comparing machinery closer to ch3's error-driven perceptron rule (`ch3-when-weights-learn.md § The perceptron learning rule`) than to anything in this chapter. Attributing that capability to Bila specifically would be a stronger, less defensible claim than the fixed-reflex framing above. (plausible caution against overclaiming; the perceptron rule itself is established, per ch3)

## Open questions — sections needing a rewrite to match this file

- **Flag 1 (script §1.1):** "Bila's lineage is the first to evolve a nervous cluster" is incorrect as written — nerve nets (without centralization) predate bilaterians in the cnidarian lineage. Needs retitling/reframing around *centralization*, not *innervation*, as Bila's innovation.
- **Flag 2 (script §1.2):** "The weight moves out of the sensor" as Bila's invention is not safe as written — cnidarians already have tunable synapses. The chapter's territory narrows to: convergence (a place where dials are read *together*) and internal signals as inputs — not the existence of the tunable junction itself.
- These corrections do not affect §1.3 (internal signals) or the Ch0→Ch1 bridge about the bacterium's weight being welded to its detector — those comparisons are bacterium-vs-Bila and don't route through the cnidarian.
