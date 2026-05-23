---
title: "Aeneas transforms how historians connect the past"
vendor: google
source_url: https://deepmind.google/blog/aeneas-transforms-how-historians-connect-the-past/
published_at: 2025-07-23T00:00:00.000Z
crawled_at: 2026-05-23T14:18:59.000Z
word_count: 2050
reading_time_minutes: 11
tags: [ai-research, nature, multimodal, history, gemini]
---

Aeneas transforms how historians connect the past — Google DeepMind

July 23, 2025 Research

# Aeneas transforms how historians connect the past

The Aeneas team

Introducing the first model for contextualizing ancient inscriptions, designed to help historians better interpret, attribute and restore fragmentary texts.

Writing was everywhere in the Roman world — etched onto everything from imperial monuments to everyday objects. From political graffiti, love poems and epitaphs to business transactions, birthday invitations and magical spells, inscriptions offer modern historians rich insights into the diversity of everyday life across the Roman world.

Often, these texts are fragmentary, weathered or deliberately defaced. Restoring, dating and placing them is nearly impossible without contextual information, especially when comparing similar inscriptions.

Today, we're publishing a paper in Nature introducing Aeneas, the first artificial intelligence (AI) model for contextualizing ancient inscriptions.

When working with ancient inscriptions, historians traditionally rely on their expertise and specialized resources to identify "parallels" — texts that share similarities in wording, syntax, standardized formulas or provenance.

Aeneas greatly accelerates this complex and time-consuming work. It reasons across thousands of Latin inscriptions, retrieving textual and contextual parallels in seconds that allow historians to interpret and build upon the model's findings.

Our model can also be adapted to other ancient languages, scripts and media, from papyri to coinage, expanding its capabilities to help draw connections across a wider range of historical evidence.

We co-developed Aeneas with the University of Nottingham, and in partnership with researchers at the Universities of Warwick, Oxford and Athens University of Economics and Business (AUEB).

## Aeneas' advanced capabilities

Named after the wandering hero of Graeco-Roman mythology, Aeneas builds upon Ithaca, our earlier work using AI to restore, date and place ancient Greek inscriptions.

Aeneas goes a step further, helping historians interpret and contextualize a text, give meaning to isolated fragments, draw richer conclusions and piece together a better understanding of ancient history.

Our model's advanced capabilities include:
- **Parallels search:** Searches for parallels across a vast collection of Latin inscriptions. By turning each text into a kind of historical fingerprint, Aeneas identifies deep connections.
- **Processing multimodal input:** Aeneas is the first model to determine a text's geographical provenance using multimodal inputs, analyzing both text and visual information.
- **Restoring gaps of unknown length:** For the first time, Aeneas can restore gaps in texts where the missing length is unknown.
- **State-of-the-art performance:** Aeneas sets a new state-of-the-art benchmark in restoring damaged texts and predicting when and where they were written.

## How Aeneas works

Aeneas is a multimodal generative neural network that takes an inscription's text and image as input. To train Aeneas, we curated a large and reliable dataset, drawing from decades of work by historians to create digital collections, especially the Epigraphic Database Roma (EDR), Epigraphic Database Heidelberg (EDH) and Epigraphic Database Clauss Slaby (EDCS-ELT).

We cleaned, harmonized and linked these records into a single machine-actionable dataset that we refer to as the Latin Epigraphic Dataset (LED), comprising over 176,000 Latin inscriptions from across the ancient Roman world.

Our model uses a transformer-based decoder to process the textual input of an inscription. Specialized networks handle character restoration and dating using text, while geographical attribution also uses images of the inscriptions as input. The decoder retrieves similar inscriptions from the LED, ranked by relevance.

For each inscription, Aeneas' contextualization mechanism retrieves a list of parallels using a technique called "embeddings" — encoding the textual and contextual information of each inscription into a kind of historical fingerprint containing details of what the text says, its language, when and where it came from, and how it relates to other inscriptions.

## State-of-the-art performance

Aeneas restores damaged inscriptions with a Top-20 accuracy of 73% in gaps of up to ten characters. This only decreases to 58% when the restoration length is unknown — itself an incredibly challenging task. It also shows its reasoning in an interpretable way, providing saliency maps that highlight which parts of the inputs influenced its predictions. Thanks to its use of visual data, our model can attribute an inscription to one of 62 ancient Roman provinces with 72% accuracy. For dating, Aeneas places a text within 13 years of the date ranges provided by historians.

## A new lens on historical debates

To test Aeneas' capabilities on an ongoing research debate, we gave it one of the most famous Roman inscriptions: the Res Gestae Divi Augusti, Emperor Augustus' first-person account of his achievements.

Historians have long-argued about the dating of this inscription. Rather than predicting a single fixed date, Aeneas produced a detailed distribution of possible dates, showing two distinct peaks, with one smaller peak around 10-1 BCE and a larger, more confident peak between 10-20 CE. These results captured both prevailing dating hypotheses in a quantitative way.

## Advancing historical research collaboratively

To assess Aeneas' impact as an aid for research, we conducted a large-scale Historian and AI collaborative study. We invited twenty-three historians who regularly work with inscriptions to restore, date and place a set of texts using Aeneas.

Aeneas helped the historians in our study identify new parallels and increased their confidence when tackling complex epigraphic tasks. Historians consistently highlighted Aeneas' value in accelerating their work and expanding the range of most relevant parallel inscriptions.

## Sharing the tools, shaping the future

Aeneas is designed to integrate within historians' existing research workflows. By combining expert knowledge with machine learning, it opens up a collaborative process, offering interpretable suggestions that serve as valuable starting points for historical inquiry.

As part of today's release, we're upgrading Ithaca, our ancient Greek model, to be powered by Aeneas and include the contextualization function, restorations of unknown length and better performance overall.

We've also co-designed a new teaching syllabus for bridging technical skills with historical thinking in the classroom. This syllabus aligns with AI literacy initiatives, including the European Commission's Digital Competences Framework for Citizens (DigComp 2.2) and UNESCO's AI Competency Framework for Students.