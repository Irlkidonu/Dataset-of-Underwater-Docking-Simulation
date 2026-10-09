<div align="center">

# Transformer Multimodal Underwater Docking Dataset

Simulator-generated camera and forward-looking-sonar data for autonomous underwater docking.

## [⬇ Download the complete dataset ZIP](https://github.com/Irlkidonu/Dataset-of-Underwater-Docking-Simulation/releases/download/v1.0/Transformer_Multimodal_Underwater_Docking_Dataset.zip)

[View Dataset v1.0 release](https://github.com/Irlkidonu/Dataset-of-Underwater-Docking-Simulation/releases/tag/v1.0) · [Download SHA-256 checksum](https://github.com/Irlkidonu/Dataset-of-Underwater-Docking-Simulation/releases/download/v1.0/SHA256SUMS.txt)

</div>

## Dataset contents

The dataset contains synchronized rendered RGB camera observations,
forward-looking-sonar observations, sensor timing information, and dock-relative
pose labels. Included subsets cover:

- controlled multimodal perception;
- near-dock terminal support;
- BlueROV2 Heavy domain adaptation and qualification;
- markerless open-bore docking-station development;
- marker-assisted rich-world development; and
- tank-world domain-transfer assessment.

The ZIP contains 6,898 dataset files: 3,822 NumPy archives and 3,076 SDF
configuration files. It is distributed through GitHub Releases rather than Git
history because the archive is approximately 1.51 GiB.

## Simulated optical conditions

All observations were generated in simulation. The field
`simulated_nephelometric_index` is a modeled, dimensionless turbidity-related
simulator quantity. It is not measured and is not calibrated to NTU or FNU. It
replaces the legacy metadata name `measured_ntu`; the numerical payloads were
preserved byte-identically without conversion, scaling, or recalibration.

## Split-integrity disclosure

Exact camera-image hashing identified three cross-split groups in controlled
perception, three in terminal support, and five in the tank clean-dock subset.
The controlled and tank groups are repeated initialization frames. Terminal
support contains two initialization-frame groups and one repeated degenerate
sensor-view group. The controlled comparison was also evaluated after excluding
frame zero, without materially changing its principal interpretation.

The frozen Heavy V3 adaptation dataset contains zero cross-split identical poses
and zero cross-split duplicate-image groups.

## Verify the download

Download both release assets into the same directory and run:

```bash
sha256sum -c SHA256SUMS.txt
```

Expected ZIP SHA-256:

```text
0721159c367aa9b77da366e8a822086fb55e6baf376b34abf7fff49cd03f3a46
```

## Related software and manuscript

- [Docking Station in AUV-Simulator](https://github.com/Irlkidonu/Docking-Station-in-AUV-Simulator)
- [AUV-Simulator](https://github.com/Irlkidonu/AUV-Simulator)
- *Transformer-Based Multi-Modal Perception for Autonomous Underwater Docking under Variable Turbidity in Simulation Environment*

## Citation

Please cite the associated manuscript and this dataset release. A formal dataset
citation can be added here when an archival DOI is assigned.

**Authors:** Christos Alexandris, Panagiotis Papageorgas, and Dimitrios Piromalis.
