# IPF-Sonification-PD


This repository provides three different Pure Data scripts showing the IPF's capability for Model-Based Sonification (MBS).

The **first skript** *"1_Study.pd"* was used in a user study. Here a keyboard can play different Tones or Melodies, while the Modulation Wheel (CC1) controls the input strength $\alpha$. The sound is produced by five wavetable oscillators (wavetable can be changed in the script by clicking on its name). The Volumen of these Pszilators is modulated by the system state $g_i$, while the derivative of $g$ introduces a phase shift.


The **second skript** *"2_excitation_beta.pd"* shows how different material parameters $\beta$ influence the dynamic bahviour of the IPF. Again a Keyboard is used for input, but now the pitch is fixed. Instead, different keys (in the range of midi note number 48 to 72) are assigned to different $\beta$, where beta increases (0-0.5) with note number. The velocity is assigned to the input strength $\alpha$ (0.25-0.602) to explore the different dynamical behavior. The sound is produced in the same manner as in the first script, but here, the derivative introduces a frequency modulation rather than a phase shift. 

The folder *"DemoSounds_PdSonifikationBeta"* contains demo sounds produced with the script for all combinations of three different $\alpha$ (0.379, 0.511, and 0.573) and three different $\beta$ (0, 0.24, and 0.5). Each file name consists of for numbers, where the first two refer to the incoming midi parameters, while the latter two refer to the resulting modeling parameters of the IPF: The first number always begins with *nn* and describes the pressed midi note number, the second one beginning with *vl* shows the related velocity, the third number beginning with *a* names the related $\alpha$ (where a decimal point should be imagined after the first zero) and the last number beginning with *b* refers to $\beta$ (again with an imaginary decimal point after the first zero).


The **third skript** *"3_SoundDesign.pd"*
