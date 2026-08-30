# smiles_project

Exploratory 3D CNN for classifying viral pneumonia (COVID-19) from chest CT scans.

- **Data:** [MosMedData: Chest CT Scans with COVID-19 Related Findings](https://www.medrxiv.org/content/10.1101/2020.05.20.20100362v1) (public subset).
- **Task:** binary classification — CT scan shows signs of viral pneumonia, or is normal.
- **Approach:** a PyTorch 3D CNN trained on a small (200-scan) subset, plus a setup step for
  [MedNeXt](https://github.com/MIC-DKFZ/MedNeXt) as an alternative 3D architecture.
- **Notebook:** [`3D_image_classification.ipynb`](3D_image_classification.ipynb).

This is an adaptation of Hasib Zunair's [3D image classification tutorial](https://github.com/hasibzunair/3D-image-classification-tutorial)
(ported from Keras to PyTorch), not original architecture work. On the full ~1,000-scan
dataset the source tutorial reports ~83% accuracy with 6-7% run-to-run variance; this
repository's own run used only the 200-scan subset with no fixed seed, so its result is
not a reliable estimate — treat this as an exploratory notebook, not a validated model.

## Related repositories

- [`radiomics`](https://github.com/denis-samatov/radiomics) — the author's other medical-imaging
  work (myocardial radiomic feature extraction), unrelated task and dataset.
- [`smiles`](https://github.com/denis-samatov/smiles) — an unrelated repository (vision-language
  model guides); the similar name is coincidental.
