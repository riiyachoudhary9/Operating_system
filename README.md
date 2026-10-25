# Page Replacement Algorithm Simulator

An Operating Systems lab project that simulates **FIFO**, **LRU**, and **Optimal** page replacement in Python/Jupyter Notebook.

## Features
- Accepts a comma- or space-separated page reference string and a frame count.
- Validates page input and rejects non-numeric values, negative page numbers, and frame counts below 1.
- Displays step-by-step frame contents, hit/fault status, and the replaced page.
- Calculates page faults, page hits, hit ratio, and fault ratio.
- Compares all three algorithms on the same input.
- Includes Part B manual tracing and Part C experiments, including Belady's anomaly.

## Requirements
- Python 3
- Jupyter Notebook or JupyterLab
- pandas

Install dependencies:
```bash
python -m pip install notebook pandas
```

## Run
1. Download or clone this repository.
2. Open a terminal in the project folder.
3. Start Jupyter:
   ```bash
   jupyter notebook
   ```
4. Open `Page_Replacement_Simulator.ipynb`.
5. Run cells from top to bottom. In the interactive cell, enter a reference string and number of frames.

Example input:
```text
Enter page reference string (comma or space separated): 1 2 3 1 4 2 5
Enter number of frames: 3
```

## Algorithms
- **FIFO:** replaces the page that entered memory earliest.
- **LRU:** replaces the page that has not been used for the longest time in the past.
- **Optimal:** replaces the page whose next use is farthest in the future. This is a theoretical benchmark because future references are not known to a real operating system.

## Sample results from the assignment's example
Reference string: `1 2 3 1 4 2 5`, frames: `3`.

| Algorithm | Page faults | Page hits | Hit ratio | Fault ratio |
|---|---:|---:|---:|---:|
| FIFO | 5 | 2 | 28.57% | 71.43% |
| LRU | 6 | 1 | 14.29% | 85.71% |
| Optimal | 5 | 2 | 28.57% | 71.43% |

## Part B result
Reference string: `7 0 1 2 0 3 0 4 2 3 0 3 2`, frames: `3`.

| Algorithm | Page faults | Page hits | Hit ratio | Fault ratio |
|---|---:|---:|---:|---:|
| FIFO | 10 | 3 | 23.08% | 76.92% |
| LRU | 9 | 4 | 30.77% | 69.23% |
| Optimal | 7 | 6 | 46.15% | 53.85% |

See `screenshots/` for execution/tracing tables. See `Page_Replacement_Project_Report.pdf` for the manual trace and experiment analysis.

## Repository contents
- `Page_Replacement_Simulator.ipynb` — source code, example runs, manual trace, and experiments.
- `Page_Replacement_Project_Report.pdf` — brief project report and assignment answers.
- `screenshots/` — result tables for showcasing the project.
- `LinkedIn_Post.md` — suggested project showcase post.

## Learning outcomes
This project helped demonstrate demand paging, page faults and hits, victim-page selection, algorithm comparison, and Belady's anomaly.

## Reference
Operating Systems Lab Assignment PDF supplied for this assignment. The implementation and explanations should be reviewed and understood before submission.
