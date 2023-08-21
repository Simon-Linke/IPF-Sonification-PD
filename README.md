# IPF-Sonification-PD

This repository provides three different Pure Data scripts showing the Impulse Pattern Formulations (IPF) capabilities for Model-Based Sonification [[1](#1),[2](#2)] (MBS).

The **first script** *"1_Study.pd"* was used in a user study. Here a keyboard can play different tones or melodies while the modulation wheel (*CC1*) controls the input strength $\alpha$. The sound is produced by five wavetable oscillators (wavetable can be changed in the script by clicking on its name). The volume of these oscillators is modulated by the system state $g_i$, while the derivative of $g$ introduces a phase shift.

The **second script** *"2_excitation_beta.pd"* shows how different material parameters $\beta$ influence the dynamic bahviour of the IPF. Again a Keyboard is used for input, but now the pitch is fixed. Instead, different keys (in the range of midi note number 48 to 72) are assigned to different $\beta$, where beta increases (0-0.5) with note number. The velocity is assigned to the input strength $\alpha$ (0.25-0.602) to explore the different dynamical behavior. The sound is produced in the same manner as in the first script, but here, the derivative introduces a frequency modulation rather than a phase shift. 

The folder *"DemoSounds_PdSonifikationBeta"* contains demo sounds produced with the script for all combinations of three different $\alpha$ (0.379, 0.511, and 0.573) and three different $\beta$ (0, 0.24, and 0.5). Each file name consists of four numbers, where the first two refer to the incoming midi parameters, while the latter two refer to the resulting modeling parameters of the IPF: The first number always begins with *nn* and describes the pressed midi note number, the second one beginning with *vl* shows the related velocity, the third number beginning with *a* names the related $\alpha$ (where a decimal point should be imagined after the first zero) and the last number beginning with *b* refers to $\beta$ (again with an imaginary decimal point after the first zero).


The **third script** *"3_SoundDesign.pd"* is an extended version of the second script. It was designed to explore the sonic capabilities of an IPF model freely. The scaling of the reflection point $\beta$ was slightly changed to increase the occurrence of chaotic results. The five different oscillators are further spread across the stereo panorama. The script is again controlled with a keyboard, where the velocity determines $\alpha$. However, $\beta$ is controlled by the modulation wheel (*CC1*) while different keys change the pitch. The underlying waveform can now be morphed continuously using the midi controller *CC24*. *CC25* also affects $\alpha$ to allow more detailed control (and further allow modification after a key is pressed). Additionally, pressing a sustain pedal (*CC64*) prevents the velocity from affecting $\alpha$ while still preventing the influence of *CC25*.

Finally, the file *ipf-tilt.apk* is a ready-to-install Android app where an IPF model was included in the *Tiltification* sound leveling app (https://github.com/TimZiemer/sonic-tilt-1). Here the angle of the smartphone controls the input strength $\alpha$. The values were scaled in a way that bifurcations and chaotic behavior occur at angles $>5^\circ$.


## References
<a id="1">[1]</a> 
Bader, R. (2013). 
Impulse Pattern Formulation. 
In: Nonlinearities and Synchronization in Musical Acoustics and Music Psychology. Current Research in Systematic Musicology, vol 2. Springer, Berlin, Heidelberg. 
https://doi.org/10.1007/978-3-642-36098-5_8


<a id="2">[2]</a> 
Linke, S., Bader, R., Mores, R (2019). 
The impulse pattern formulation (IPF) as a model of musical instruments—Investigation of stability and limits.
In: Chaos: An Interdisciplinary Journal of Nonlinear Science 29(10)
https://doi.org/10.1063/1.5092511 
