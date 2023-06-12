# Notions
- **[ARPAbet](https://en.wikipedia.org/wiki/ARPABET)** is an alphabet for transcribing American English phonetic sounds;
- **Partially-Observed Markov Decision Processes** is a research area in Deep RL;
- **Large Vocabulary Continuous Speech Recognition**;
- **Articulatory Phonetics** studies how speech sounds are made by articulators (moving organs) in mouth;
- **Acoustic Phonetics** studies acoustic properties of speech sounds;
- **Phonetic categories** are derived from how humans produce speech
- **[International Phonetic Alphabet (IPA)](https://en.wikipedia.org/wiki/IPA_pulmonic_consonant_chart_with_audio)**
# Articulatory Phonetics
## **Articulatory parameters** for English consonants in ARPAbet:
- PLACE OF ARTICULATION:
    - bilabial,
    - labio-dental,
    - inter-dental,
    - alveolar,
    - palatal,
    - velar,
    - glottal;
- MANNER OF ARTICULATION:
    - stop,
    - fricative,
    - affricate,
    - nasal,
    - approximant,
    - flapped;
- VOICING:
    - voiceless,
    - voiced;
## ARPAbet Vowels:
||b_d|ARPA||b_d|ARPA|
|---|---|---|---|---|---|
|1|bead|`iy`|9|bode|`ow`|
|2|bid|`ih`|10|booed|`uw`|
|3|bayed|`ey`|11|bud|`ah`|
|4|bed|`eh`|12|bird|`er`|
|5|bad|`ae`|13|bide|`ay`|
|6|bod(y)|`aa`|14|bowed|`aw`|
|7|bawd|`ao`|15|Boyd|`oy`|
|8|Budd(hist)|`uh`||||
Note: Many speakers pronounce Buddhist with the vowel uw as in booed, So for them `uh` is instead the vowel in “put” or “book”
## Speech Production: Flow, Resonance, & Articulation
- Pulmonic egressive airstream + Vibration of vocal folds = produces sounds;
Sound is then modulated by:
- Sound is modulated by **Resonance**,
---

![Image_3](notes/learning-courses/Stanford%20CS224S%20—%20Spoken%20Language%20Processing/Week%201/images/Lec%202/Image_3.jpg)

---
- Sound is modulated by **Articulation**:
    - Oral tract: uvula, soft palate (velum), hard palate, tongue, lips, teeth
    - Nasal tract;
---

![Image_4](notes/learning-courses/Stanford%20CS224S%20—%20Spoken%20Language%20Processing/Week%201/images/Lec%202/Image_4.jpg)

---
## Larynx and Vocal Folds
- The Larynx (voice box)
    - A structure made of cartilage and muscle
    - Located above the trachea (windpipe) and below the pharynx (throat)
    - Contains the vocal folds (adjective for larynx: laryngeal)
- Vocal Folds (older term: vocal cords)  
    - Two bands of muscle and tissue in the larynx
    - Can be set in motion to produce sound (voicing)
## Voicing
---

![image_voicing](notes/learning-courses/Stanford%20CS224S%20—%20Spoken%20Language%20Processing/Week%201/images/Lec%202/image_voicing.png)

---
- Air comes up from lungs  
- Forces its way through vocal cords, pushing open (2,3,4)  
- This causes air pressure in glottis to fall, since:
    -  when gas runs through constricted passage, its velocity increases (**Venturi tube effect**)  
    - this increase in velocity results in a drop in pressure (**Bernoulli principle**)
- Because of drop in pressure, vocal cords snap together again (6-10)
- Single cycle: ~1/100 of a second.
### Voicelessness
- When vocal cords are open, air passes through unobstructed
- Voiceless sounds: `p`/`t`/`k`/`s`/`f`/`sh`/`th`/`ch`
- If the air moves very quickly, the turbulence causes a different kind of phonation: whisper
## Consonants and Vowels
- **Consonants** phonetically sound with audible noise produced by a constriction
- **Vowels** phonetically sound with no audible noise produced by a constriction
> it’s more complicated than this, since we have to consider **syllabic function**, but this will do for now
## Place of Articulation
_Consonants'_ **place of articulation** is the location where the airflow is most constricted. Three major kinds of place articulation:
- Labial (with lips)  
- Coronal (using tip or blade of tongue)
- Dorsal (using back of tongue)
---

![image_place_of_articulation](notes/learning-courses/Stanford%20CS224S%20—%20Spoken%20Language%20Processing/Week%201/images/Lec%202/image_place_of_articulation.png)

---
## Manner of Articulation
- **Stop** is a complete closure of articulators, so no air escapes through mouth
- **Oral stop** occurs when palate is raised, no air escapes through nose. Air pressure builds up behind closure, explodes when released: `p`, `t`, `k`, `b`, `d`, `g`
- **Nasal stop** occurs when oral closure, but palate is lowered, air escapes through nose: `m`, `n`, `ng`
---
- **Fricative** is a close approximation of two articulators, resulting in turbulent airflow between them, producing a hissing sound: `f`, `v`, `s`, `z`, `th`, `dh`;
- **Approximant** is a not quite-so-close approximation of two articulators, so no turbulence: `y`, `r`;
- **Lateral approximant** is an obstruction of airstream along center of oral tract, with opening around sides of tongue: `l`.
## Oral vs. Nasal Sounds
---

![image_oral_vs_nasal](notes/learning-courses/Stanford%20CS224S%20—%20Spoken%20Language%20Processing/Week%201/images/Lec%202/image_oral_vs_nasal.png)

---
## Tongue position for vowels
- Front–Middle-Back
- Close–Mid–Open
---

![Image_14](notes/learning-courses/Stanford%20CS224S%20—%20Spoken%20Language%20Processing/Week%201/images/Lec%202/Image_14.jpg)

---
# Acoustic Phonetics
Sound waves are longitudinal waves.

---

![image_sound_waves_are_longitudinal](notes/learning-courses/Stanford%20CS224S%20—%20Spoken%20Language%20Processing/Week%201/images/Lec%202/image_sound_waves_are_longitudinal.png)
![image_sound_wave_particle_dispalcement_pressure](notes/learning-courses/Stanford%20CS224S%20—%20Spoken%20Language%20Processing/Week%201/images/Lec%202/image_sound_wave_particle_dispalcement_pressure.png)

---
## Fundamental frequency

---

Waveform of the vowel `iy`:

![image_wave_iy](notes/learning-courses/Stanford%20CS224S%20—%20Spoken%20Language%20Processing/Week%201/images/Lec%202/image_wave_iy.png)
- Frequency: 10 repetitions / .03875 seconds = 258 Hz;
- This is speed that vocal folds move, hence voicing;
- Each peak corresponds to an opening of the vocal folds;
- The low frequency of the complex wave is called the fundamental frequency of the wave or F0.
---

Waveform of the phrase "She just had a baby":

![image_wave_she_just_had_a_baby](notes/learning-courses/Stanford%20CS224S%20—%20Spoken%20Language%20Processing/Week%201/images/Lec%202/image_wave_she_just_had_a_baby.png)
- The vowels all have regular amplitude peaks;
- Stop consonant:
    - Closure followed by release,
    - The silence followed by slight bursts of emphasis: very clear for `b` of “baby”;
- Fricative:noisy. `sh` of “she” at beginning.

Spectrogram of the phrase "She just had a baby":

![Image_22](notes/learning-courses/Stanford%20CS224S%20—%20Spoken%20Language%20Processing/Week%201/images/Lec%202/Image_22.jpg)

---
## Source-filter model of speech production
---

![image_source_filter_model](notes/learning-courses/Stanford%20CS224S%20—%20Spoken%20Language%20Processing/Week%201/images/Lec%202/image_source_filter_model.png)
- Source and filter are independent:  
    - Different vowels can have same pitch,
    - The same vowel can have different pitch
---
### Source filter model of vowels
- Any body of air will vibrate in a way that depends on its size and shape;
- Vocal tract amplifies certain harmonics;
- Formants are result of different shapes of vocal tract.
### Resonances of the vocal tract
---

The human vocal tract as an open tube:

![Image_26](notes/learning-courses/Stanford%20CS224S%20—%20Spoken%20Language%20Processing/Week%201/images/Lec%202/Image_26.jpg)

---

Shapes of vocal tract:

![Image_27](notes/learning-courses/Stanford%20CS224S%20—%20Spoken%20Language%20Processing/Week%201/images/Lec%202/Image_27.jpg)

---
## Defining Intonation
- Ladd (1996) “Intonational phonology”
- **suprasegmental phonetic features**:
    - F0,
    - Intensity (energy),
    - Duration.
- **sentence-level** pragmatic **meanings** are meanings that apply to phrases or utterances as a whole, not lexical stress, not lexical tone.
##### Pitch is not Frequency
- **Pitch** is the mental sensation or perceptual correlated of F0;
- Relationship between pitch and F0 is not linear:
    - Linear between 100Hz and 1000Hz,
    - Logarithmic above 1000Hz;
- **Mel scale** is one model of this F0-pitch mapping: A mel is a unit of pitch defined so that pairs of sounds which are perceptually equidistant in pitch are separated by an equal number of mels:
    - Frequency in mels = 1127 ln (1 + f/700)
> I've seen something similar in the 1st volume of [Musimathics](http://www.musimathics.com/). Probably, it is somehow related to "Critical Bands"
## Intensity
![image_plot_of_intensity](notes/learning-courses/Stanford%20CS224S%20—%20Spoken%20Language%20Processing/Week%201/images/Lec%202/image_plot_of_intensity.png)
##### Aspects of prosody
- **Prominence**: some syllables/words are more prominent than others;
- **Structure/boundaries**: sentences have prosodic structure:
    - Some words group naturally together,
    - Others have a noticeable break or disjuncture between them
- **Tune**: the intonational melody of an utterance.
# The Speech Chain (Denes and Pinson)
Speaker:
![Image_31](notes/learning-courses/Stanford%20CS224S%20—%20Spoken%20Language%20Processing/Week%201/images/Lec%202/Image_31.jpg)
Hearer:
![Image_32](notes/learning-courses/Stanford%20CS224S%20—%20Spoken%20Language%20Processing/Week%201/images/Lec%202/Image_32.jpg)
# Appendix
## How to read spectrograms
![image_how_to_read_spectrograms](notes/learning-courses/Stanford%20CS224S%20—%20Spoken%20Language%20Processing/Week%201/images/Lec%202/image_how_to_read_spectrograms.png)
- bab: closure of lips lowers all formants: so rapid increase in all formants at beginning of "bab”
- dad: first formant increases, but F2 and F3 slight fall
- gag: F2 and F3 come together: this is a characteristic of velars. Formant transitions take longer in velars than in alveolars or labials

An example rom Ladefoged “A Course in Phonetics”.
Spectrogram of a phrase "She came back and started again":
![image_how_to_read_spectogram_2](notes/learning-courses/Stanford%20CS224S%20—%20Spoken%20Language%20Processing/Week%201/images/Lec%202/image_how_to_read_spectogram_2.png)
1. lots of high-freq energy
2. 
3. closure for `k`
4. burst of aspiration for `k`
5. `ey` vowel; faint 1100 Hz formant is nasalisation
6. bilabial nasal,
7. short b closure, voicing barely visible
8. `ae` — upward transitions after bilabial stop at beginning
9. F2 and F3 coming together for `k`
## More on manner of articulation of consonants
- Tap or flap
    - Tongue makes a single tap against the alveolar ridge: `dx` in “butter”
- Affricate
    - Stop immediately followed by a fricative `ch`, `jh`
## Vowels
![image_vovels](notes/learning-courses/Stanford%20CS224S%20—%20Spoken%20Language%20Processing/Week%201/images/Lec%202/image_vowels.png)
### The oral cavity amplifies some harmonics
![image_oral_cavity_amplifies_some_harmonics](notes/learning-courses/Stanford%20CS224S%20—%20Spoken%20Language%20Processing/Week%201/images/Lec%202/image_oral_cavity_amplifies_some_harmonics.png)
# Words
>  utterance; HSR versus ASR; syllables and phones and _whatnot_; uvula;  velum – soft palate; hard palate; Venturi tube effect; syllabic function; intonational phonology; suprasegmental phonetic features; prosody;
# Comment
Comment: quite dense material. Next steps are:
# References
- [ ] [A Course in Phonetics](https://linguistics.berkeley.edu/acip/)
    - [ ] [Home | Linguistics](https://lx.berkeley.edu/)
- [ ] [The Art of Language Invention | David Peterson | Talks at Google - YouTube](https://youtu.be/Z50T-tslrgs)
- [ ] [ARPABET](https://web.stanford.edu/class/cs224s/arpabet.html)
- [ ] [The CMU Pronouncing Dictionary](http://www.speech.cs.cmu.edu/cgi-bin/cmudict)
- [ ] [International Phonetic Alphabet - Wikipedia](https://en.wikipedia.org/wiki/International_Phonetic_Alphabet)