# 🎥 Media Index Tracker

This repository serves as a centralized index for tracking media entities, using unique identifiers (like IMDb's "tt" codes) as the primary source for filenames. The core purpose is to maintain and analyze data streams associated with these unique IDs.

## ⚙️ Automated Data Analysis

The workflow is set up to automatically analyze the entire index recursively. It focuses exclusively on files whose names start with `tt*` (e.g., `tt12345678`), ignoring repository metadata directories like `.git` and `.github`.

Every time the GitHub Action is triggered manually via `workflow_dispatch`, it performs the following:

1. **Counts** all processed `tt*` files.

2. **Sums** the value in the analyzed files. This sum is treated as **total size in bytes**.

3. Updates the summary table below with the latest calculation and a human-readable size format (MB, GB, TB).


## 📈 Data Analysis Summary
<!-- START_DATA_SUMMARY -->
<div align=center>

| Metric | Value |
| :--- | :---: |
| **Last Processed** | 2026-01-17 10:09 UTC |
| **Unique Titles** | 6050 |
| **Total Size** | 13.98 TB |

</div>
<!-- END_DATA_SUMMARY -->


## 🤝 Contributing

We welcome contributions to improve the Media Index Tracker! Whether you're fixing a bug, improving the documentation, or adding a new feature, your help is appreciated.

To contribute:
- Fork this repository.
- Create a new branch for your feature or fix.
- Commit your changes.
- Submit a Pull Request (PR) detailing your changes.

For major changes or new feature proposals, please open an issue first to discuss what you would like to implement.

## 📜 License

This project is licensed under the [GNU Affero General Public License v3.0](https://www.gnu.org/licenses/agpl-3.0.en.html).
