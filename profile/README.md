# Dhi Technologies

Dhi builds edge-native video analytics: perception software that runs
directly on the camera-side compute (NVIDIA Jetson-class hardware) instead
of shipping raw video to a cloud GPU. The goal is analytics that keep
working when the network doesn't, at a power and cost budget a fixed
camera can actually carry.

## What we build

- **Edge-native pipelines.** Detection, tracking, re-identification, scene
  understanding, and alerting run on-device (Jetson Orin class hardware
  today), with cloud/cloud-edge sync as an addition, not a dependency.
- **Model compression that ships or refuses.** Distillation and
  quantization are only useful if the compressed model still meets its
  accuracy bar. We gate compressed artifacts against a measured accuracy
  floor and refuse to ship one that misses it, rather than silently
  degrading quality.
- **Honesty-as-a-feature engineering.** Across our products this shows up
  as concrete mechanisms, not slogans:
  - **Refusal gates** - a component that cannot meet its stated bar (an
    accuracy floor, a confidence threshold) declines to produce an answer
    instead of guessing.
  - **Calibration** - reported confidence is checked against measured
    correctness, not asserted.
  - **Falsification ledgers** - claims and experiments are recorded so
    they can be checked and disproven, not just cited.

  We would rather say "this doesn't work yet, here is the measurement"
  than overstate a result.

## Where to find us

- **Website:** [dhi-tech.com](https://dhi-tech.com)
- **Hugging Face:** [huggingface.co/Dhi-Technologies](https://huggingface.co/Dhi-Technologies)
  - benchmark datasets and interactive demo Spaces built from our
    engineering work
  - engineering blog: [huggingface.co/datasets/Dhi-Technologies/blog](https://huggingface.co/datasets/Dhi-Technologies/blog)
- **Public code:** [Prompt2Model - Language-Guided Vision Model Factory](https://github.com/DHI-Technologies-Inc/Prompt2Model-Language-Guided-Vision-Model-Factory) -
  a natural-language front end that compiles a plain-English task
  description into a trained, calibrated, edge-deployable vision model
  (classification and detection), with an optional distill/quantize
  compression stage gated on measured accuracy.

## Research track

Dhi Labs is our research track. We are working through a portfolio of
papers on edge perception (thermal-only sensing, fixed-camera 3D from
monocular video, causal predictive alerting, neuro-symbolic scene graphs,
and related topics). These are in preparation and internal review; none
are published on arXiv or elsewhere yet. We will link them here once they
are public, and we will not claim otherwise before then.

## How we work

- Every product ships with tests against synthetic ground truth before
  any real-data claim, and real measurements before a README states a
  number.
- GPU-dependent work is published as recipes and CPU-verified math until
  the on-device measurement exists - we do not fake training runs or
  invent benchmark numbers.
- Repos are organized one product per repository. Most are private while
  under active development; we open-source pieces as they mature, starting
  with Prompt2Model above.

## Contact

Reach us through [dhi-tech.com](https://dhi-tech.com) or open an issue on
one of our public repositories.
