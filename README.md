# eurosat-decision-site

Static results page for the [eurosat-decision](https://github.com/gokulkn/eurosat-decision) repository.

A benchmark result on EuroSAT only (RGB, 10 classes, 64×64 Sentinel-2 patches): fine-tuned torchvision ResNet-18 with a softmax-confidence abstention layer.

## Key results

| Metric | Value |
|--------|-------|
| Overall test accuracy (only unbiased figure) | 0.9627 (3,899 / 4,050) |
| Validation accuracy (validation-selected) | 0.9679 |
| Frozen abstention threshold | 0.50 |
| Coverage at threshold | 0.9938 (4,025 / 4,050 answered) |
| Accuracy on answered cells | 0.9650 |
| Cells abstained | 25 |
| SeaLake precision / recall / support | 0.9912 / 0.9956 / 450 |

## Scope

- Benchmark on **EuroSAT only**; no accuracy claimed on any other imagery.
- Not field imagery; single seed 42; no confidence interval.
- Own fixed stratified 70/15/15 split, not a published benchmark split.

## Live demo

Browser demo of the committed EuroSAT decision model (ResNet-18 with abstention layer):
https://eurosat-decision-tool.vercel.app

## Deploy

On Vercel: sign in with GitHub, import this repo (`eurosat-decision-site`), deploy with defaults (no build command, output directory `.`). The repo link in index.html is already set; commit and push again after any edits.
