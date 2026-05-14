# LoRA / QLoRA / Adapters Selection

Use when you've determined fine-tuning is the right approach and need to choose between full retraining and parameter-efficient alternatives.

```
We need to fine-tune a model for this task: [describe task]. Our compute budget is: [describe]. Our labeled dataset is: [describe size and quality]. Walk me through whether to use LoRA, QLoRA, or adapters — and what training infrastructure we need to execute it.
```

**When to use:** After confirming fine-tuning is warranted (see `rag_vs_finetuning.md`). Picks the right parameter-efficient method for your constraints.
