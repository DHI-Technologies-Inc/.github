# Dhi Technologies

Dhi builds edge-native video analytics: perception software that runs on a local edge
node next to the cameras a site already has, on any GPU. The aim is analytics that keep
working when the network is slow, on a power and cost budget a fixed camera can carry.

## What we build

- **Edge-native pipelines.** Detection, tracking, re-identification, scene
  understanding, and alerting run on the site's edge node, small enough for an 8 GB
  module at a remote site with no rack. Cloud and cloud-edge sync are additions to that
  path.
- **Model compression with a measured gate.** Distillation and quantization ship only
  when the compressed model meets its accuracy floor. Each compressed artifact is
  measured against that floor, and the factory keeps the uncompressed model when the
  floor is not met.
- **Evidence-first engineering.** Across our research systems this shows up as concrete
  mechanisms:
  - **Refusal gates.** A component that cannot meet its stated bar, such as an accuracy
    floor or a confidence threshold, returns an explicit, logged refusal.
  - **Calibration.** Reported confidence is checked against measured correctness.
  - **Recorded experiments.** Claims and experiments are recorded with their inputs and
    code hashes, so each result can be re-run and checked.

## Where to find us

- **Website:** [dhi-tech.com](https://dhi-tech.com)
- **Hugging Face:** [huggingface.co/Dhi-Technologies](https://huggingface.co/Dhi-Technologies)
  - benchmark datasets and demo Spaces built from our engineering work
  - engineering blog: [huggingface.co/datasets/Dhi-Technologies/blog](https://huggingface.co/datasets/Dhi-Technologies/blog)
- **Intent2Edge** (Language-Guided Vision Model Factory): a natural-language front end that compiles a
  plain-English task description into a trained, calibrated, edge-deployable vision
  model (classification and detection), with an optional distill and quantize
  compression stage gated on measured accuracy. Paper:
  *Intent2Edge: Compiling Natural-Language Intent into Refuse-Closed Edge Vision Artifacts*.
  Demo: [huggingface.co/spaces/Dhi-Technologies/intent2edge-demo](https://huggingface.co/spaces/Dhi-Technologies/intent2edge-demo).
  Reference model: [huggingface.co/Dhi-Technologies/intent2edge-reference-onnx](https://huggingface.co/Dhi-Technologies/intent2edge-reference-onnx).

## Research track

Dhi Labs is our research track. Its papers cover edge perception: thermal sensing,
fixed-camera 3D from monocular video, scene graphs, causal predictive alerting,
multi-camera reasoning memory, amodal counting, appearance-based re-identification, and
Intent2Edge. Paper repositories state their title, venue, results, and reproduction
steps, with the evidence records committed alongside.

## How we work

- Each research system is built with tests against synthetic ground truth first, and
  its README states real-data numbers once they are measured.
- GPU-dependent work is published as recipes and CPU-verified math, with the on-device
  measurement recorded when it exists.
- Repositories are organized one research system per repository.

## Licensing

- **Research use.** Research, academic, and evaluation use of our public repositories is
  covered by the license in each repository.
- **Commercial use.** Commercial licensing is arranged directly with us. Contact
  [hello@dhi-tech.com](mailto:hello@dhi-tech.com) or visit
  [dhi-tech.com](https://dhi-tech.com).

## Contact

Reach us through [dhi-tech.com](https://dhi-tech.com) or open an issue on one of our
repositories.
