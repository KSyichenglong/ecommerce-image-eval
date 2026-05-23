---
name: ecommerce-image-eval
description: Evaluate and score e-commerce product main images (主图) for Chinese online marketplaces like JD, Tmall, Taobao, and Douyin. Use when the user asks to evaluate, score, rate, or assess a product's main image, banner, or primary visual for e-commerce listings. Also triggers for phrases like "主图评分", "主图评估", "帮我看看这张图", "这个主图怎么样", or when discussing product image optimization for shoes cabinets, cat villas, pet cages, or similar home/pet products.
---

# Ecommerce Image Evaluation

## Overview

This skill provides a structured, data-driven scoring framework for evaluating e-commerce product main images (主图) on Chinese marketplaces. It is based on 13 years of real-world e-commerce operations experience and validated against actual sales performance data.

## When to Use

- User provides a product image and asks for evaluation
- User discusses main image strategy, design direction, or optimization
- User mentions specific product categories: shoes cabinet (鞋柜), cat villa (猫别墅), pet cage (狗笼/鸟笼), or similar home goods
- User asks for competitive analysis of product images on search result pages

## Category Selection

Before scoring, determine which category standard applies:

| Trigger Word | Standard | Reference File |
|-------------|----------|----------------|
| "鞋柜" or shoes cabinet materials (板材/实木/楠竹/塑料/金属) | 鞋柜主图 v1.5 | `references/鞋柜主图评分标准_v1.5.md` |
| "猫别墅" or "猫柜" | 猫别墅主图 v1.0 | `references/猫别墅主图评分标准_v1.0.md` |

If the user specifies a standard explicitly ("用鞋柜标准" / "用猫别墅标准"), follow their instruction regardless of category keywords.

## Scoring Workflow

### Step 1: Collect Required Information

Before scoring, confirm these 7 items with the user (do not guess):

1. **Core selling point** (1 item) — What makes this product different?
2. **Core search keyword** — Category word / Feature word / Brand word?
3. **Product material** — Body + door panel + frame material
4. **Sub-category** — Specific type within the category
5. **Main image spec vs. hot-selling spec** — Size/price shown on image vs. actual best seller
6. **Target channel** — JD / Tmall / PDD / Douyin
7. **Target audience** + **Differentiation details** — Who buys this, and what specific product features support the claim?

**Critical rule**: If any of the above is missing, score must be labeled as "[推测项]" (speculative). Never invent product features or selling points.

### Step 2: Determine Search Type

| Search Type | Definition | Scoring Adjustment |
|-------------|-----------|-------------------|
| **Category word** (品类词) | e.g. "鞋柜", "猫别墅" | Standard scoring, strictest |
| **Feature word** (特性词) | e.g. "免安装鞋柜", "实木猫别墅" | Relax information readability, but still evaluate differences |
| **Brand word** (品牌词) | e.g. "XX牌鞋柜" | Focus on brand recognition, relax difference communication |

### Step 3: Score by Four Dimensions

Load the appropriate reference file and score each dimension. Total = 100 points.

| Dimension | Weight | Key Checks |
|-----------|--------|-----------|
| **1. Prominence (突出)** | 35 | Product ratio ≥60%, color distinction, readable text ≤6 chars, clean edges, category signal within 0.5s |
| **2. Differentiation (差异化)** | 35 | Difference exists (P1-P4), visually verifiable, strong conversion power, ≤5 visual elements, not fake |
| **3. Semantic Interception (语义截流)** | 15 | Cognitive pause in 0.5s, precise targeting, conflict with competitors, manageable expectation |
| **4. Visual Trust (视觉信任)** | 15 | Material texture honest, scene matches positioning, user can imagine "this looks good in my home" |

### Step 4: Apply Veto Rules

If any of these triggers, score is capped or requires redo:

- Product ratio < 40%
- Claimed difference has no detail page evidence
- Scene and product positioning severely mismatched
- Category recognition > 1 second
- Legal/safety risk (e.g., fire corridor placement for shoe cabinets)
- Main image spec severely mismatched with hot-selling spec

### Step 5: Output Format

Deliver results in this order:

1. **Competitive environment notes** — What do search result pages look like?
2. **Item-by-item scores** with brief justification
3. **Total score / Grade** — Explosive (≥85), Good (75-84), Revise (60-74), Redo (<60)
4. **Market positioning conclusion** — What role does this image play?
5. **Top 3 core problems** — Ranked by impact on conversion
6. **Optimization plan** — P0 (must fix), P1 (should fix), P2 (nice to have)

## Key Rules Summary

- **Search type matters**: Category search = grab attention; Brand search = lock attention
- **Price gap**: Main image vs. hot-selling price difference ≤50% = no penalty; >50% or functional gap = penalty
- **Visual proof > text**: For visual-verifiable selling points (size, appearance), zero text on main image is acceptable. For non-visual selling points (installation-free, silent), must have text or auxiliary image
- **Category signal**: Full product display with items inside = strongest signal, do not deduct points for internal lights/decoration
- **Information density**: ≤5 visual elements, all pointing to one unified impression

## References

- `references/鞋柜主图评分标准_v1.5.md` — Shoes cabinet full standard with scoring rubric and copy-paste score card
- `references/猫别墅主图评分标准_v1.0.md` — Cat villa initial standard (migrated from shoes cabinet v1.5, pending real-world validation for v1.1/v1.2)

## Version History

- v1.0: Initial skill packaging with shoes cabinet v1.5 and cat villa v1.0 standards
