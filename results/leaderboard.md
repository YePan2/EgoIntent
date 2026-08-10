# EgoIntent Leaderboard

Results are reported on all 3,014 benchmark steps. Reference-based scores and reference-free diagnostics use different judges and are not directly comparable.

- **Reference-based:** Local, Procedural, and Next measure semantic agreement with human references on a 0–100 scale. Overall is their arithmetic mean.
- **Reference-free:** GF (Visual Grounding Faithfulness), HIC (Hierarchical Intent Consistency), TPC (Temporal Progression Consistency), and NPF (Next-Plan Feasibility) are scored from the observation video and anonymized prediction without access to the reference answer.
- Missing predictions receive zero.

## Closed-Source MLLMs

| Model | Local | Procedural | Next | Overall | GF | HIC | TPC | NPF |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Doubao-Seed-2.1-Turbo | 57.98 | 63.62 | 43.78 | **55.13** | 74.47 | 85.19 | 78.86 | 76.75 |
| Qwen3.5-Plus | 57.99 | 57.76 | 42.38 | 52.71 | 73.30 | 81.62 | 76.97 | 75.52 |
| Gemini-3.5-Flash | 43.34 | 48.31 | 32.72 | 41.45 | 58.79 | 70.24 | 62.66 | 60.66 |
| Amazon-Nova-2-Lite-V1 | 37.98 | 42.96 | 22.84 | 34.59 | 55.05 | 63.75 | 56.77 | 54.93 |

## Open-Weight MLLMs

| Model | Local | Procedural | Next | Overall | GF | HIC | TPC | NPF |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Qwen3-VL-32B-Instruct | 45.14 | 52.81 | 30.44 | **42.80** | 69.84 | 81.32 | 75.12 | 72.68 |
| Qwen3-VL-8B-Instruct | 40.86 | 45.03 | 26.59 | 37.49 | 61.18 | 71.50 | 64.75 | 62.34 |
| Qwen2.5-VL-7B-Instruct | 35.41 | 42.45 | 22.53 | 33.46 | 52.20 | 64.98 | 53.85 | 51.87 |
| Qwen2-VL-7B-Instruct | 37.42 | 39.57 | 22.53 | 33.18 | 51.26 | 60.19 | 48.67 | 46.81 |
| Molmo2-8B | 35.10 | 41.01 | 20.55 | 32.22 | 52.50 | 62.14 | 54.01 | 51.83 |
| InternVL3-8B | 34.25 | 40.16 | 18.51 | 30.97 | 47.46 | 60.94 | 49.14 | 46.58 |
| Molmo2-O-7B | 32.36 | 37.32 | 19.02 | 29.57 | 49.29 | 57.77 | 48.42 | 46.33 |
| LLaVA-Video-7B-Qwen2 | 33.14 | 33.42 | 15.65 | 27.41 | 49.51 | 54.29 | 47.49 | 45.48 |
| Kimi-VL-A3B-Thinking-2506 | 27.11 | 33.19 | 14.98 | 25.09 | 40.15 | 50.94 | 39.35 | 37.10 |
| InternVL2-8B | 21.60 | 28.25 | 12.58 | 20.81 | 33.12 | 43.32 | 34.72 | 32.55 |
| LLaVA-NeXT-Video-7B | 13.36 | 15.51 | 5.76 | 11.54 | 24.37 | 27.89 | 20.59 | 19.53 |

## Metric Notes

- **GF:** whether the prediction is supported by visible evidence.
- **HIC:** whether Local and Procedural form a valid goal hierarchy.
- **TPC:** whether the current and future predictions follow a coherent temporal order.
- **NPF:** whether the proposed next action is immediately feasible from the observed state.
