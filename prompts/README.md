# EgoIntent Benchmark Prompts

The files in this directory are the official prediction prompts used for the EgoIntent benchmark.

For each sample, send:

1. `benchmark_prediction_system.txt` as the system message;
2. `benchmark_prediction_user.txt` as the user message; and
3. the complete pre-outcome observation-window video as the visual input.

The expected response is a JSON object containing `local_intent`, `procedural_intent`, and `next_step`. Do not provide scene names, task names, annotations, or future frames to the model.
