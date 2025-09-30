To create computational [[Computational Bone Adaptation Models]], researchers have developed mathematical formulas to quantify the mechanical stimulus that bone cells sense.

---

## Turner's Model (Frequency and Strain)
This model, based on the [[Rules of Bone Adaptation]], suggests that the stimulus is a function of both the strain magnitude and the loading frequency.

> The mechanical stimulus ($S$) is proportional to the peak-to-peak strain magnitude ($\epsilon_p$) multiplied by the frequency ($f$).
> $$ S \sim k \cdot \epsilon_p \cdot f $$

This can be generalised for complex loading signals by using a Fourier series expansion to break down the signal into its constituent sine waves.
> $$ S = k_1 \sum_{i=1}^{n} \epsilon_{pi} f_i $$

This formulation correctly predicts that static loading ($f=0$) provides no stimulus, and that high-frequency, low-strain signals can be equivalent to low-frequency, high-strain signals.

---

## Carter & Beaupre's Model (Daily Stress Stimulus)
An alternative and widely used model proposes that the daily stimulus ($\psi$) is a weighted sum of the stress cycles experienced throughout the day.

> The daily stimulus is calculated based on the number of cycles ($n_i$) at a given effective stress level ($\overline{\sigma}_i$).
> $$ \psi = \left( \sum_{\text{day}} n_i \overline{\sigma}_i^m \right)^{1/m} $$
> - The term $\overline{\sigma}$ is an "energy stress," related to the strain energy density.
> - The exponent **m** is an empirical weighting factor (typically between 4 and 8) that heavily weights higher stress levels.

This model effectively captures the idea that a few high-stress cycles can contribute more to the daily stimulus than thousands of low-stress cycles.