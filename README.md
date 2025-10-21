# OpenThermal

### The World's Largest Open-Source Thermal Video Dataset

by [GeoFire Labs](https://geofirelabs.com)

---

## Overview

**OpenThermal** is an open-source initiative by **GeoFire Labs** to build the world's largest publicly available dataset of thermal video imagery — targeting over **1,000 hours** of high-resolution thermal recordings and structured metadata.

The goal is to accelerate global research in **AI-based wildfire detection**, **thermal anomaly recognition**, and **computer vision for climate resilience** by making large-scale, real-world thermal data openly accessible.

---

## Status

The dataset is **in progress** and will be released in stages beginning in **2026**.

At this time, the repository includes:

* Documentation
* Example metadata schema
* Contribution guidelines

Thermal video files and annotations will be made publicly available upon completion of data collection and curation.

---

## Objectives

* Provide an open, standardized dataset for AI and computer vision research on thermal imagery.
* Support the development of detection and segmentation models for wildfire, smoke, and heat anomalies.
* Enable reproducible benchmarks for edge-AI performance using real thermal data.
* Foster collaboration across research institutions, startups, and public agencies working on wildfire and environmental monitoring.

---

## Dataset Structure

```
OpenThermal/
│
├── videos/
│   ├── site_A_2025-01-12_T1.mp4
│   ├── site_B_2025-02-03_T2.mp4
│   └── ...
│
├── metadata/
│   ├── site_A_2025-01-12.json
│   ├── site_B_2025-02-03.json
│   └── ...
│
├── annotations/
│   ├── bounding_boxes/
│   │   ├── site_A_fire_labels.csv
│   │   └── ...
│   └── segmentation_masks/
│       ├── site_A_masks/
│       └── ...
│
└── README.md
```

---

## Metadata Schema

Each `.json` metadata file includes the following fields:

| Field                   | Description                                                 |
| ----------------------- | ----------------------------------------------------------- |
| `timestamp_start`       | UTC ISO start time of recording                             |
| `duration_s`            | Video length in seconds                                     |
| `gps_lat`, `gps_lon`    | Approximate camera location                                 |
| `camera_model`          | Thermal camera make/model                                   |
| `fov_deg`               | Field of view                                               |
| `temperature_range`     | Minimum and maximum measurable range (°C)                   |
| `environment`           | Environment type (e.g., forest, grassland, urban, test lab) |
| `annotations_available` | Boolean indicating whether annotations exist                |

---

## Access and Download

The dataset is not yet available.
When released, thermal video and metadata files will be hosted on open data platforms such as **Zenodo** or **AWS Open Data**.

A download script will be provided for programmatic access:

```bash
python scripts/download_dataset.py --subset thermal --region global
```

---

## Example Usage

```python
import json
data = json.load(open("metadata/site_A_2025-01-12.json"))
print(data["temperature_range"])
```

---

## Planned Benchmark Tasks

* Fire detection and segmentation
* Thermal anomaly detection
* Object classification in thermal imagery
* Edge-AI deployment benchmarking (Jetson, Raspberry Pi, Hailo)

---

## Contributing

We welcome contributions of:

* New **thermal video footage** with metadata
* **Annotations** (bounding boxes, segmentation masks)
* **Preprocessing scripts** and **data utilities**

### How to Contribute

1. Fork this repository
2. Add your data or scripts
3. Ensure metadata follows the defined schema
4. Submit a pull request with a clear description

See `CONTRIBUTING.md` for detailed contribution instructions.

---

## License

All thermal video and metadata files will be released under the **Creative Commons Attribution 4.0 (CC-BY-4.0)** license.
You may use, share, and adapt the data with appropriate attribution to **GeoFire Labs**.

---

## Citation

If you use this dataset in research, please cite:

```
@dataset{geofirelabs_openthermal_2025,
  title={OpenThermal: The World's Largest Open Thermal Video Dataset},
  author={GeoFire Labs},
  year={2025},
  url={https://github.com/GeoFireLabs/OpenThermal}
}
```

---

## Contact

Website: [https://geofirelabs.com](https://geofirelabs.com)
Email: [hello@geofirelabs.com](mailto:hello@geofirelabs.com)
