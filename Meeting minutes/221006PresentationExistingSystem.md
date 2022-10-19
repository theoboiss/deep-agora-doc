# WEEKLY SPECIFICATION REPORT

## DESCRIPTION

**Topic:** Debriefing meeting with M. Ramel

**Objective:** Clarifying the dark spots in the specifications

**Author:** Théo Boisseau

**Creation date:** 06.10.2022

**Version:** 1.0

## SUMMARY

1. [MASTERY OF AGORA BY THE USER](#I.)
2. [OUTPUT SPECIFICATIONS](#II.)
3. [UPCOMING RESEARCH](#III.)
4. [IMPLEMENTATION PROCESS](#IV.)


# I. MASTERY OF AGORA BY THE USER <a id="I."></a>

The software interface is complex and therefore too difficult for the end user to use.

Many scenario rules require a lot of parameters and without being an expert user of AGORA, it can be very easy to get lost in the interface of complex scenarios.

Deep learning could be a solution to this complexity by avoiding all this configuration.

DL modules could then be used iteratively with simpler scenarios to extract specifically defined elements of content (EOCs).


# II. OUTPUT SPECIFICATIONS <a id="II."></a>

Related components only are not interesting enough to extract for the end user.
They are looking for elements that are valuable in term of information or rarity.

## TEXTUAL

Characters are among the most important EOCs to extract. Indeed, they can later be processed by RETRO for clustering and then transcription.

However, characters can be labeled in different ways that segment them into as many EOCs of the same value: *title*, *note*, *text*, ... **to pursue**


## VISUAL

In ancient document, *dropped capital letters*, *banners*, *photographs*, *tables* are all types of EOC that are extremely valuable for their amount of historical information.

They are therefore also of great importance to extract in this project.


# III. UPCOMING RESEARCH <a id="III."></a>

- Keep a bibliography
- **Specify the outputs** of the desired algorithm, like te EOCs to be extracted
- Make an overview of the librairies that could be interesting for the project and **analyse the competing libraries by a table**.
- **Analyse the ALTO standard** and why it is relevant for the storage of Deep-AGORA outputs.
- Schedule a meeting with Justine Pinsard (RETRO team) in order to **specify with her the outputs of Deep-Agora** in relation to the inputs of RETRO, according to the ALTO format.
- **Specify all dataset requirements** to **analyse those available by a table to build the most appropriate one**.
- Produce a simple **Jupyter notebook that implements the dhSegment library** on a few ancient document images containing textual or visual EOCs, in order to extract the list of their position and label.
- Produce a schedule (Gantt) for the implementation phase


# IV. IMPLEMENTATION PROCESS <a id="IV."></a>

The first iteration should be a Jupyter notebook in which a directory of relevant ancient document images is processed by Deep-Agora 1.0 core algorithm.
It should replace the binarization, semantically segment the page layout and return for each page a list of tuples each containing an EOC, its label and its coordinates.

A next iteration should orient the notebook towards targeted extractions, which should allow multiple algorithms which would target specific types of EOC.
Most of them will most likely be trained on different data sets.

Before or after the iteration above can be produced an iteration that will aim to design an appropriate output for RETRO, in relation to the ALTO XML standard.

A forth iteration should consist of training a model on handwritten documents and test its limits.

Accordingly to the future specifications, the fifth iteration should be about turning the notebook into a usable python module or group modules.
The number of modules will be defined in relation to the number of EOC types they return.
A generic module would return the whole layout as EOCs which can later be processed by scenarios.
Otherwise, several specialised extractor modules should be reusable as part of scenarios.

