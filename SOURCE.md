# Source

## datus-de-lever-quickstart-v1.zip

This archive is a quickstart-focused subset extracted from the public DAComp
data-engineering dataset:

- Dataset: `DAComp/dacomp-de`
- Source URL: https://huggingface.co/datasets/DAComp/dacomp-de
- Original archive: `dacomp-de.zip`
- Base directory: `dacomp-de-impl-001/`
- SQL assets: `dacomp-de-evol-001/sql/`
- Original dataset license: MIT

The archive is repackaged for the Datus data-engineering quickstart so users do
not need to download the full DAComp archive when the tutorial only uses this
Lever example data.

The resulting release archive expands to:

```text
datus-de-lever-quickstart/
```

Local runtime artifacts are intentionally excluded:

- `.datus/`
- `lever_workbench.duckdb`

Users should create `lever_workbench.duckdb` from `lever_start.duckdb` when
running the tutorial.

The packaged SQL assets contain the layer files used by the quickstart:

- `sql/staging/`: 24 files
- `sql/intermediate/`: 17 files
- `sql/marts/`: 14 files

## Citation

If you use DAComp, cite the original work:

```bibtex
@misc{lei2025dacompbenchmarkingdataagents,
      title={DAComp: Benchmarking Data Agents across the Full Data Intelligence Lifecycle},
      author={Fangyu Lei and Jinxiang Meng and Yiming Huang and Junjie Zhao and Yitong Zhang and Jianwen Luo and Xin Zou and Ruiyi Yang and Wenbo Shi and Yan Gao and Shizhu He and Zuo Wang and Qian Liu and Yang Wang and Ke Wang and Jun Zhao and Kang Liu},
      year={2025},
      eprint={2512.04324},
      archivePrefix={arXiv},
      primaryClass={cs.CL},
      url={https://arxiv.org/abs/2512.04324},
}
```
