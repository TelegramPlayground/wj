# 🎥 Media Index Tracker

This repository serves as a centralized index for tracking media entities, using unique identifiers (like IMDb's "tt" codes) as the primary source for filenames. The core purpose is to maintain and analyze data streams associated with these unique IDs.

## ⚙️ Automated Data Analysis

The workflow is set up to automatically analyze the entire index recursively. It focuses exclusively on files whose names start with `tt*` (e.g., `tt12345678`), ignoring repository metadata directories like `.git` and `.github`.

Every time the GitHub Action is triggered manually via `workflow_dispatch`, it performs the following:

1. **Counts** all processed `tt*` files.

2. **Sums** the value in the analyzed files. This sum is treated as **total size in bytes**.

3. Updates the summary table below with the latest calculation and a human-readable size format (MB, GB, TB).

<!-- START_DATA_SUMMARY -->

## 📈 Data Analysis Summary

<div align="center">

| **Metric** | **Value** | 
| :--- | :---: | 
| **Last Processed** | *Awaiting First Run* | 
| **Files Analysed** | `0` | 
| **Total Size** | `0 Bytes` | 

</div>
<!-- END_DATA_SUMMARY -->

## 💾 Data File Format

The system expects each file to represent a unique media ID, containing data streams delimited by commas. The 4th column is designated for a raw byte count (or a similar numerical metric) that is accumulated by the analysis script.

**Example File Content:**
```
0,0,,597197000,1673933352
0,0,,450000000,1673933358
```

In this example, the script sums `597197000` and `450000000`.
