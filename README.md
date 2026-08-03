# GDI Enterprise Intelligence

**RFP Evidence Responder** - an evidence-grounded Microsoft Copilot Studio agent that completes incoming RFP questionnaires using only supported evidence from connected knowledge sources.

## Overview

GDI Enterprise Intelligence answers incoming RFP questionnaires by searching connected knowledge sources for every question, responding only when supporting evidence exists, and leaving unsupported fields blank. It does not ask the user for documents, clarification, evidence, or additional source material - all evidence it needs is expected to already be connected.

## Key Principles

**Evidence-only answers.** Every populated response is grounded in evidence found in connected knowledge sources, never invented, inferred, or hedged.

**Blank over guesswork.** If no supporting evidence exists for a question, the field is left blank rather than filled with a placeholder or speculative text.

**Format preservation.** The original RFP's structure, question numbering, section headers, and requested format are preserved in the output.

**Consistent voice.** Answers are written in a confident, concise, first-person-plural company voice (e.g., "We maintain...", "Our policy requires...").

**No back-and-forth.** The agent does not ask follow-up questions or request additional documentation at any stage.

## What It Can Do

| Prompt | Description |
|---|---|
| Complete RFP | Completes an incoming RFP questionnaire using connected knowledge sources, answering supported fields and leaving unsupported fields blank. |
| Answer ESG Section | Fills out the ESG section of an RFP using only evidence from connected sources, preserving the original question order. |
| Review Blank Fields | Summarizes which fields were left blank after completing an RFP. |
| Format Responses | Converts supported answers into the RFP's requested table format, keeping unsupported cells blank. |
| Check Support | Reviews draft RFP answers and removes any claims not directly supported by connected knowledge sources. |
| Create Final Output | Prepares the final completed RFP response in the same structure as the incoming questionnaire. |

## Knowledge Sources

The agent draws on a set of connected internal knowledge sources (SharePoint sites covering areas such as HR, ESG, health & safety, and corporate publications) that are configured separately in Copilot Studio and are not included in this repository.

## Getting Started

See [INSTRUCTIONS.md](./INSTRUCTIONS.md) for details on how to use this agent, submit an RFP, and interpret its output.

## Disclaimer

AI-generated content may be incorrect. Always review completed RFP responses before external submission.
