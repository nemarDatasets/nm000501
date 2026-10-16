[![DOI](https://img.shields.io/badge/DOI-10.82901%2Fnemar.nm000501-blue)](https://doi.org/10.82901/nemar.nm000501)

Huashan tonal speech ECoG (Zhang et al. Sci Data 2026), BIDS ingest.
SIGNAL IS THE HIGH-GAMMA BAND (70-150 Hz band-passed voltage, 400 Hz, common average reference), not raw broadband
voltage and not an amplitude envelope.
The release's *_ieeg.json ("Envelope of band-passed signal via Hilbert transform") and its
code/utils/Hilbert_transform.py call it a Hilbert envelope, and the first NEMAR versions repeated that. The stored
values are not an envelope: in all 20 recordings every channel has mean ~0 (|mean|/SD <= 0.0004), about half of the
samples are negative (49.7-50.0 % per channel), and 94-96 % of the power lies in 70-150 Hz (spectral peak ~79-82 Hz)
with almost none below 20 Hz. An amplitude envelope would be positive with most of its power below 20 Hz. For the high-gamma
envelope, take the magnitude of the analytic signal (e.g. abs(scipy.signal.hilbert(x))).
EDF stores the signal in uV (NWB values in V x 1e6); round-trip max error per file in convert_report.json.
One misnamed duplicate NWB (sub-01 ses-05 run-05) excluded; requirements.txt excluded.

## Ethics

Zhang et al. (2026), Methods (verbatim):

> The study was approved by the Huashan Hospital Institutional Review Board of Fudan University (HIRB, KY2017-437), and the conducting of research complied with all relevant ethical considerations.
>
> Participants signed their names on informed consent the day before surgery and were told that the task was only for research purposes, which could be terminated at any time during the task.

Source: Zhang H, Zhang D, Wu J, Li Y, Lu J, et al. (2026). A Fine-grained Spatiotemporal ECoG Dataset during Speech Perception in Tonal Language. Scientific Data. https://doi.org/10.1038/s41597-026-07619-z (PMC13635214)
