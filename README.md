# Ecommerce Image Evaluation Skill

A structured, data-driven scoring framework for evaluating e-commerce product main images (主图) on Chinese marketplaces.

Based on 13 years of real-world e-commerce operations experience and validated against actual sales performance data.

## Supported Categories

- **Shoes Cabinet (家具)** — v1.5 standard (fully validated)
- **Cat Villa / Cat Cabinet (宠物)** — v1.0 standard (migrated from shoes cabinet, pending real-world validation)

## Scoring Dimensions

| Dimension | Weight | Focus |
|-----------|--------|-------|
| Prominence (突出) | 35% | Product visibility, color distinction, readability |
| Differentiation (差异化) | 35% | Unique selling points, visual proof, conversion power |
| Semantic Interception (语义截流) | 15% | Cognitive pause, competitor conflict, expectation control |
| Visual Trust (视觉信任) | 15% | Material honesty, scene fit, purchase imagination |

## Usage

This is an [OpenClaw](https://docs.openclaw.ai) AgentSkill. Place the `ecommerce-image-eval` directory in your OpenClaw skills folder.

## License

MIT
