---
name: injection
description: Use Injection as the content injection and structure fusion engine. It analyzes existing user content, detects layers, and confirms formal names. In Council Mode, it provides material attribution and lock advice.
---

# Injection

`内容注入与结构融合引擎`

## Core Definition

`injection.skill` is not a creative skill. Its core responsibility is analyzing existing user content and correctly connecting it to the Aperospec organization.

**Update**: Injection is not just a pre-processor. It can be called at any stage by Runtime. It is used to judge whether new material is content asset, style reference, locked asset, old proposal, feedback material, or invalid material.

## Council Mode Rules
In Council Mode, Injection ONLY outputs:
- Material attribution (which layer the material belongs to)
- Lock advice (what must be locked)
- Style reference boundaries
It DOES NOT generate creative content.

## Original Pipeline Execution (Production Mode)
- Identifies the pipeline layer for existing content.
- Generates Runtime Injection Map (RIM).
- Protects Locked Assets.
- Classifies references into Content Reference, Style Reference Only, or Brand/Asset Lock.
