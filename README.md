# UnityHairShader
A hair shader originally built for the sine.space virtual world, designed and built for Unity3D's PBR rendering system.

![Preview image](https://static.wixstatic.com/media/ba743f_57ea705e6f784935a1d2dbc688d094a4~mv2_d_4600_5152_s_4_2.png/v1/fit/w_300,h_300,al_c,q_5/file.png)

Leverages the Anisotropic Rendering released by Matt Dean availible from https://github.com/Kink3d/AnisotropicStandardShader - and incorporates features from Alan Zucconi's implementation of EA's Frostbite Fast Translucency algorithm (GDC 2011).

Quick Summary:
* Anisotropic highlights
* PBR-ish. Has option to tweak/remove unrealistic fresnel highlights.
* Optional variant with Normal Map support
* Double Sided (optional - delete the first pass if you dont need it)
* Works with Shader Model 3.0 (Normal Map variant requires SM 4.5, but will fallback to SM 3.0 variant)

Notes:
* Is going to be kinda heavy. Performance seems OK here, but could probably do with optimisation.
* We render the lower pass using alpha testing versus blending; this fixes a host of issues with ordering; it's a little smelly, but it works better over all.

Shows up as 'Sine Wave/Modern/Adam's Hair Shader 1.0' (Plain variant) and 'Sine Wave/Modern/Adam's Hair Shader 1.1' (Normal variant)
