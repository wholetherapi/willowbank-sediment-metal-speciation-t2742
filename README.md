# Speciation of trace metals in anoxic sediment porewater

> **Release status: public release** — v1.0.4 (2025-02-11).
> Archived at https://doi.org/10.5281/zenodo.44120981.

We combine diffusive gradients in thin films with a speciation model to partition copper and zinc between sulphide-bound and dissolved phases in anoxic porewater. Sulphide availability explains most of the site-to-site variation.

## Repository layout

```
src/            reference implementation
data/           small example inputs and schemas
experiments/    configuration files used for the paper's runs
tests/          smoke tests for the public entry points
```

## Installation

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

## Quick start

```bash
python -m src.pipeline --config experiments/config.yaml --out results/run01
```

The sample configuration in `experiments/` runs end to end on the bundled
miniature input in under a minute.

## Data availability

The full field data set is archived by the regional monitoring agency.
`data/README.md` documents the schema and the subset that can be redistributed.

## Reproducing the reported results

1. Prepare the environment as above.
2. Run `python -m src.pipeline --config experiments/paper.yaml`.
3. Compare `results/run01/summary.json` with the values in the paper's Table 2.

## Citation

If you use this code, please cite the paper listed in `CITATION.cff`.

## License

MIT. See `LICENSE`.

## Contact

Willowbank Watershed Lab <lab@willowbank-labs.org>
