<div align="center">

# TIO-Former

### Ultra-Lightweight 6-Directional ToF-Inertial Odometry for Nano-UAVs via a Streaming Causal Transformer

[![arXiv](https://img.shields.io/badge/arXiv-2609.17198-b31b1b.svg)](https://arxiv.org/abs/2609.17198)
![Code](https://img.shields.io/badge/Code-Coming_Soon-345779)
![Models](https://img.shields.io/badge/Models-Coming_Soon-6b7280)
![Dataset](https://img.shields.io/badge/Dataset-Coming_Soon-2f855a)

Yang Liu · Yifan He · Wenhao Zhao · Xiangyu Mo · Yang Xu · Hao Wei<br>
Mingze Ma · Huan Li · Yifan Wu · Fei Gao · Zipeng Dai · Xin Zhou

<p align="center">
  <img src="assets/affiliations.png" alt="Zhejiang University · Differential Robotics" width="660">
</p>

**arXiv 2026**

</div>

## Overview

TIO-Former is a camera-free, optical-flow-free, and mapless range-inertial odometry framework for resource-constrained nano-UAVs. Given six orthogonal 8 × 8 time-of-flight (ToF) arrays and synchronized IMU measurements, it estimates continuous 6-DoF motion with bounded inference cost and memory.

<div align="center">
<table>
<tr>
<td align="center" width="25%"><strong>384</strong><br><sub>ToF ranges per frame</sub></td>
<td align="center" width="25%"><strong>15 g</strong><br><sub>ToF sensor payload</sub></td>
<td align="center" width="25%"><strong>15 Hz</strong><br><sub>online inference</sub></td>
<td align="center" width="25%"><strong>10.466 ms</strong><br><sub>P95 edge latency</sub></td>
</tr>
</table>
</div>

<table>
<tr>
<td width="33%"><strong>Reliability-aware ToF encoding</strong><br><sub>Bilateral gated differences preserve valid metric changes while suppressing artifacts from invalid returns.</sub></td>
<td width="33%"><strong>IMU-guided directional fusion</strong><br><sub>Inertial queries dynamically route the six directional ToF tokens according to platform motion.</sub></td>
<td width="33%"><strong>Bounded streaming memory</strong><br><sub>Local KV and compressed Chunk-FIFO memory keep the per-step cost fixed over long flights.</sub></td>
</tr>
</table>

<p align="center">
  <img src="assets/model_architecture.png" alt="Architecture of TIO-Former" width="100%">
</p>

<p align="center"><em>Architecture of TIO-Former.</em></p>

## News

- **[Sep 15, 2026]** The paper is available on [arXiv](https://arxiv.org/abs/2609.17198).
- **[Sep 14, 2026]** The repository was created. Code, pretrained models, and the dataset will be released here.

## Release Status

Resource | Status
:--- | :---
Paper | [Available on arXiv](https://arxiv.org/abs/2609.17198)
Training and evaluation code | Coming soon
Pretrained models and configurations | Coming soon
Dataset and preparation tools | Coming soon

## Acknowledgements

This work was conducted during the author's internship at Differential Robotics, under the mentorship of [Zipeng Dai](https://scholar.google.com/citations?hl=zh-CN&user=e2c7Kt0AAAAJ).

## Citation

If you find this work useful, please cite:

```bibtex
@misc{liu2026tioformer,
  title         = {TIO-Former: Ultra-Lightweight 6-Directional ToF-Inertial Odometry for Nano-UAVs via a Streaming Causal Transformer},
  author        = {Liu, Yang and He, Yifan and Zhao, Wenhao and Mo, Xiangyu and Xu, Yang and Wei, Hao and Ma, Mingze and Li, Huan and Wu, Yifan and Dai, Zipeng and Zhou, Xin and Gao, Fei},
  year          = {2026},
  eprint        = {2609.17198},
  archivePrefix = {arXiv},
  primaryClass  = {cs.RO},
  url           = {https://arxiv.org/abs/2609.17198}
}
```

## Contact

For questions about the paper or future releases, please open an issue in this repository.
