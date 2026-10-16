[![DOI](https://img.shields.io/badge/DOI-10.82901%2Fnemar.nm000501-blue)](https://doi.org/10.82901/nemar.nm000501)

Huashan tonal speech ECoG (Zhang et al. Sci Data 2026), BIDS ingest.
SIGNAL IS HIGH-GAMMA ENVELOPE (70-150 Hz Hilbert), not raw voltage.
Source NWB iEEG series + *_ieeg.json document the envelope derivation.
EDF stores envelope in uV; round-trip max error per file in convert_report.json.
One misnamed duplicate NWB (sub-01 ses-05 run-05) excluded; requirements.txt excluded.

## Ethics

Zhang et al. (2026), Methods (verbatim):

> The study was approved by the Huashan Hospital Institutional Review Board of Fudan University (HIRB, KY2017-437), and the conducting of research complied with all relevant ethical considerations.
>
> Participants signed their names on informed consent the day before surgery and were told that the task was only for research purposes, which could be terminated at any time during the task.

Source: Zhang H, Zhang D, Wu J, Li Y, Lu J, et al. (2026). A Fine-grained Spatiotemporal ECoG Dataset during Speech Perception in Tonal Language. Scientific Data. https://doi.org/10.1038/s41597-026-07619-z (PMC13635214)
