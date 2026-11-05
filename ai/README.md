# AI service

Python service that classifies a fault description into a category and a UWE repair priority.

Planned models, compared on the same test set:

1. Baseline: a simple text classifier (built for the PiP demo)
2. Fine-tuned model
3. General AI API (for comparison)

Safety rules force Emergency for keywords such as fire, flooding, gas or exposed wiring. Emergency recall is the key safety metric.

Folders:

- `data/`: labelled descriptions (see `data/README.md` for the format)
- `notebooks/`: experiments and evaluation
