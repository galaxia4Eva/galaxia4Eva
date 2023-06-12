# Phonetics
**Speech recognition** is transcribing waveforms into text. **Text-to-speech**  is converting text into waveforms. A computational perspective on **phonetics**, the study of the speech sounds used in the languages of the world, how they are produced in the human vocal tract, how they are realised acoustically, and how they can be digitised and processed.

## Speech Sounds and Phonetic Transcription
A string of **phones**, which are speech sounds, each represented with symbols adapted from the Roman alphabet. The standard phonetic representation for transcribing the world’s languages is the **International Phonetic Alphabet (IPA)**, an evolving standard first developed in 1888. **ARPAbet** (Shoup, 1980) is a simple phonetic alphabet that conveniently uses ASCII symbols to represent an American-English subset of the IPA.

![Phonetics_chapter_1](notes/learning-courses/Stanford%20CS224S%20—%20Spoken%20Language%20Processing/Week%201/figures/Phonetics_1.png)
#todo: convert to table

In general, however, the mapping between the letters of English orthography and phones is relatively **opaque**; a single letter can represent very different sounds in different contexts. The English letter c corresponds to phone `k` in cougar `k uw g axr`, but phone `s` in cell `s eh l`. Besides appearing as c and k, the phone `k` can appear as part of x (fox `f aa k s`), as ck (jackal `jh ae k el`) and as cc (raccoon `r ae k uw n`). Many other languages, for example, Spanish, are much more **transparent** in their sound-orthography mapping than English.

## Articulatory Phonetics
**Articulatory phonetics** is the study of how these phones are produced as the various organs in the mouth, throat, and nose modify the airflow from the lungs.

![Phonetics_2](notes/learning-courses/Stanford%20CS224S%20—%20Spoken%20Language%20Processing/Week%201/figures/Phonetics_2.png)

Phones are divided into two main classes: **consonants** and **vowels**. Both kinds of sounds are formed by the motion of air through the mouth, throat or nose. Consonants are made by restriction or blocking of the airflow in some way, and can be voiced or unvoiced. Vowels have less obstruction, are usually voiced, and are generally louder and longer-lasting than consonants. The technical use of these terms is much like the common usage; `p`, `b`, `t`, `d`, `k`, `g`, `f`, `v`, `s`, `z`, `r`, `l`, etc., are consonants; `aa`, `ae`, `ao`, `ih`, `aw`, `ow`, `uw`, etc., are vowels. **Semivowels** (such as `y` and `w`) have some of the properties of both; they are voiced like vowels, but they are short and less syllabic like consonants.

### Consonants: Place of Articulation

![Phonetics_3](notes/learning-courses/Stanford%20CS224S%20—%20Spoken%20Language%20Processing/Week%201/figures/Phonetics_3.png)

**Labial**: Consonants whose main restriction is formed by the two lips coming together have a **bilabial** place of articulation. In English these include `p` as in possum, `b` as in bear, and `m` as in marmot. The English **labiodental** consonants `v` and `f` are made by pressing the bottom lip against the upper row of teeth and letting the air flow through the space in the upper teeth.

**Dental**: Sounds that are made by placing the tongue against the teeth are dentals. The main dentals in English are the `th` of thing and the `dh` of though, which are made by placing the tongue behind the teeth with the tip slightly between the teeth.

**Alveolar**: The alveolar ridge is the portion of the roof of the mouth just behind the upper teeth. Most speakers of American English make the phones `s`, `z`, `t`, and `d` by placing the tip of the tongue against the alveolar ridge. The word **coronal** is often used to refer to both dental and alveolar.

**Palatal**: The roof of the mouth (the **palate**) rises sharply from the back of the alveolar ridge. The **palato-alveolar** sounds `sh` (shrimp), `ch` (china), `zh` (Asian), and `jh` (jar) are made with the blade of the tongue against the rising back of the alveolar ridge. The palatal sound `y` of yak is made by placing the front of the tongue up close to the palate

**Velar**: The **velum**, or soft palate, is a movable muscular flap at the very back of the roof of the mouth. The sounds `k` (cuckoo), `g` (goose), and `ŋ` (kingfisher) are made by pressing the back of the tongue up against the velum.

**Glottal**: The glottal stop `q` is made by closing the glottis (by bringing the vocal folds together).

### Consonants: Manner of Articulation

A **stop** is a consonant in which airflow is completely blocked for a short time. This blockage is followed by an explosive sound as the air is released. The period of blockage is called the **closure**, and the explosion is called the **release**. English has voiced stops like `b`, `d`, and `g` as well as unvoiced stops like `p`, `t`, and `k`. Stops are also called **plosives**.

The **nasal** sounds `n`, `m`, and `ng` are made by lowering the velum and allowing air to pass into the nasal cavity.

In **fricatives**, airflow is constricted but not cut off completely. The turbulent airflow that results from the constriction produces a characteristic “hissing” sound. The English labiodental fricatives `f` and `v` are produced by pressing the lower lip against the upper teeth, allowing a restricted airflow between the upper teeth. The dental fricatives `th` and `dh` allow air to flow around the tongue between the teeth. The alveolar fricatives `s` and `z` are produced with the tongue against the alveolar ridge, forcing air over the edge of the teeth. In the palato-alveolar fricatives `sh` and `zh`, the tongue is at the back of the alveolar ridge, forcing air through a groove formed in the tongue. The higher-pitched fricatives (in English `s`, `z`, `sh` and `zh`) are called **sibilants**. Stops that are followed immediately by fricatives are called **affricates**; these include English `ch` (chicken) and `jh` (giraffe).

In **approximants**, the two articulators are close together but not close enough to cause turbulent airflow. In English `y` (yellow), the tongue moves close to the roof of the mouth but not close enough to cause the turbulence that would characterise a fricative. In English `w` (wood), the back of the tongue comes close to the velum. American `r` can be formed in at least two ways; with just the tip of the tongue extended and close to the palate or with the whole tongue bunched up near the palate. `l` is formed with the tip of the tongue up against the alveolar ridge or the teeth, with one or both sides of the tongue lowered to allow air to flow over it. `l` is called a **lateral** sound because of the drop in the sides of the tongue.

A **tap** or **flap** `dx` is a quick motion of the tongue against the alveolar ridge. The consonant in the middle of the word lotus (`l ow dx ax s`) is a tap in most dialects of American English; speakers of many U.K. dialects would use a `t` instead.

### Vowels

![Phonetics_4](notes/learning-courses/Stanford%20CS224S%20—%20Spoken%20Language%20Processing/Week%201/figures/Phonetics_4.png)

The three most relevant parameters for vowels are what is called vowel **height**, which correlates roughly with the height of the highest part of the tongue, vowel **frontness** or **backness**, indicating whether this high point is toward the front or back of the oral tract and whether the shape of the lips is **rounded** or not.

![Phonetics_5](notes/learning-courses/Stanford%20CS224S%20—%20Spoken%20Language%20Processing/Week%201/figures/Phonetics_5.png)
A schematic characterisation of the height of different vowels.

It is schematic because the abstract property **height** correlates only roughly with ac- tual tongue positions; it is, in fact, a more accurate reflection of acoustic facts. Note that the chart has two kinds of vowels: those in which tongue height is represented as a point and those in which it is represented as a path. A vowel in which the tongue position changes markedly during the production of the vowel is a **diphthong**. English is particularly rich in diphthongs.

The second important articulatory dimension for vowels is the shape of the lips. Certain vowels are pronounced with the lips rounded (the same lip shape used for whistling). These **rounded** vowels include `uw`, `ao`, and `ow`.

### Syllables

![Phonetics_6](notes/learning-courses/Stanford%20CS224S%20—%20Spoken%20Language%20Processing/Week%201/figures/Phonetics_6.png)
Syllable structure of ham, green, eggs. σ =syllable.

Consonants and vowels combine to make a **syllable**. A syllable is a vowel-like (or **sonorant**) sound together with some of the surrounding consonants that are most closely associated with it. We call the vowel at the core of a syllable the **nucleus**. Initial consonants, if any, are called the **onset**. Onsets with more than one consonant (as in strike `s t r ay k`), are called **complex onsets**. The **coda** is the optional consonant or sequence of consonants following the nucleus. The **rime**, or **rhyme**, is the nucleus plus coda.

The task of automatically breaking up a word into syllables is called **syllabification**. Syllable structure is also closely related to the **phonotactics** of a language. The term **phonotactics** means the constraints on which phones can follow each other in a language. Phonotactics can be represented by a language model or finite-state model of phone sequences.

## Prosody
**Prosody** is the study of the intonational and rhythmic aspects of language, and in particular the use of **F0**, **energy**, and **duration** to convey pragmatic, affective, or conversation-interactional meanings.
> The word is used in a different but related way in poetry, to mean the study of verse metrical structure.

Prosody can be used to mark **discourse structure**, like the difference between statements and questions, or the way that a conversation is structured. Prosody is used to mark the **saliency** of a particular word or phrase. Prosody is heavily used for paralinguistic functions like conveying affective meanings like happiness, surprise, or anger. And prosody plays an important role in managing turn-taking in conversation.

In summary, there is a continuum of prosodic **prominence**, for which it is often useful to represent levels like accented, stressed, full vowel, and reduced vowel.

### Prosodic Prominence: Accent, Stress and Schwa
In a natural utterance of American English, some words sound more **prominent** than others, and certain syllables in these words are also more **prominent** than others. What we mean by prominence is that these words or syllables are perceptually more salient to the listener. Speakers make a word or syllable more salient in English by saying it louder, saying it slower (so it has a longer duration), or by varying F0 during the word, making it higher or more variable.

#### Accent 
We represent prominence via a linguistic marker called **pitch accent**. Words or syllables that are prominent are said to **bear** (be associated with) a pitch accent. Thus this utterance might be pronounced by **accenting** the _emphasised_ words:
> I’m a little _surprised_ to hear it _characterised_ as _happy_.

#### Lexical Stress
The syllables that bear pitch accent are called **accented** syllables. Not every syllable of a word can be accented: pitch accent has to be realised on the syllable that has **lexical stress**. Lexical stress is a property of the word’s pronunciation in dictionaries; the syllable that has lexical stress is the one that will be louder or longer if the word is accented. The following example shows underlined accented words with the stressed syllable bearing the accent (the louder, longer syllable) in boldface:
> I’m a little _sur**prised**_ to hear it _**char**acterised_ as _**hap**py_.

Stress is marked in dictionaries. The CMU dictionary (CMU, 1993), for example, marks vowels with 0 (unstressed) or 1 (stressed) as in entries for counter: `K AW1 N T ER0`, or table: `T EY1 B AH0 L`. Difference in lexical stress can affect word meaning; the noun content is pronounced `K AA1 N T EH0 N T`, while the adjective is pronounced `K AA0 N T EH1 N T`.

#### Reduced Vowels and Schwa
Unstressed vowels can be weakened even further to **reduced vowels**, the most common of which is **schwa** (`ax`), as in the second vowel of parakeet: `p ae r ax k iy t`. In a reduced vowel the articulatory gesture isn’t as complete as for a full vowel. Not all unstressed vowels are reduced; any vowel, and diphthongs in particular, can retain its full quality even in unstressed position. For example, the vowel `iy` can appear in stressed position as in the word eat `iy t` or in unstressed position as in the word carry `k ae r iy``.

### Prosodic Structure
Spoken sentences have prosodic structure: some words seem to group naturally together, while some words seem to have a noticeable break or disjuncture between them. Prosodic structure is often described in terms of **prosodic phrasing**, meaning that an utterance has a prosodic phrase structure in a similar way to it having a syntactic phrase structure. For example, the sentence _I wanted to go to London, but could only get tickets for France_ seems to have two main **intonation phrases**, their boundary occurring at the comma. Furthermore, in the first phrase, there seems to be another set of lesser prosodic phrase boundaries (often called **intermediate phrases**) that split up the words as _I wanted | to go | to London_. These kinds of intonation phrases are often correlated with syntactic structure constituents (Price et al. 1991, Bennett and Elfner 2019).

Automatically predicting prosodic boundaries can be important for tasks like TTS. Modern approaches use sequence models that take either raw text or text an- notated with features like parse trees as input, and make a break/no-break decision at each word boundary. They can be trained on data labeled for prosodic structure like the Boston University Radio News Corpus (Ostendorf et al., 1995).

### Tune
Two utterances with the same prominence and phrasing patterns can still differ prosodically by having different **tunes**. The **tune** of an utterance is the rise and fall of its F0 over time. A very obvious example of tune is the difference between statements and yes-no questions in English. The same words can be said with a final F0 rise to indicate a yes-no question (called a **question rise**):
![Phonetics_7](notes/learning-courses/Stanford%20CS224S%20—%20Spoken%20Language%20Processing/Week%201/figures/Phonetics_7.png)
or a final drop in F0 (called a **final fall**) to indicate a declarative intonation:
![Phonetics_8](notes/learning-courses/Stanford%20CS224S%20—%20Spoken%20Language%20Processing/Week%201/figures/Phonetics_8.png)
Languages make wide use of tune to express meaning (Xu, 2005). In English, for example, besides this well-known rise for yes-no questions, a phrase containing a list of nouns separated by commas often has a short rise called a **continuation rise** after each noun. Other examples include the characteristic English contours for expressing **contradiction** and expressing **surprise**.

#### Linking Prominence and Tune

![Phonetics_9](notes/learning-courses/Stanford%20CS224S%20—%20Spoken%20Language%20Processing/Week%201/figures/Phonetics_9.png)
The accent and boundary tones labels from the ToBI transcription system for American English intonation (Beckman and Ayers 1997, Beckman and Hirschberg 1994). #todo: convert to table.

Pitch accents come in different varieties that are related to tune; high pitched accents, for example, have different functions than low pitched accents. There are many typologies of accent classes in different languages. One such typology is part of the **ToBI** (Tone and Break Indices) theory of intonation (Silverman et al. 1992). Each word in ToBI can be associated with one of five types of **pitch accents** shown above Each utterance in ToBI consists of a sequence of intonational phrases, each of which ends in one of four **boundary tones**, representing the utterance final aspects of tune. There are version of ToBI for many languages.

## Acoustic Phonetics and Signals
### Waves

![Phonetics_10](notes/learning-courses/Stanford%20CS224S%20—%20Spoken%20Language%20Processing/Week%201/figures/Phonetics_10.png)
A sine wave with a frequency of 10 Hz and an amplitude of 1.

Acoustic analysis is based on the sine and cosine functions. Figure above shows a plot of a sine wave, in particular the function $$y = A∗sin(2π ft)$$ where we have set the amplitude A to 1 and the frequency f to 10 cycles per second. The two important characteristics of a wave are its **frequency** and **amplitude**. The frequency is the number of times a second that a wave repeats itself, that is, the number of **cycles**. We usually measure frequency in **cycles per second** Cycles per second are usually called **hertz** (shortened to **Hz**). The **amplitude** A of a sine wave is the maximum value on the Y axis. The **period** T of the wave is the time it takes for one cycle to complete, defined as $$ T = {1 \over f} $$

### Speech Sound Waves
We represent sound waves by plotting the change in air pressure over time. One metaphor which sometimes helps in understanding these graphs is that of a vertical plate blocking the air pressure waves (perhaps in a microphone in front of a speaker’s mouth, or the eardrum in a hearer’s ear). The graph measures the amount of **compression** or **rarefaction** (uncompression) of the air molecules at this plate.

![Phonetics_11](notes/learning-courses/Stanford%20CS224S%20—%20Spoken%20Language%20Processing/Week%201/figures/Phonetics_11.png)
A short segment of a waveform taken from the Switchboard corpus of telephone speech of the vowel `iy` from someone saying “she just had a baby”. Notice that the wave repeats regularly.

The first step in digitising a sound wave is to convert the analog representations (first air pressure and then analog electric signals in a microphone) into a digital signal. This **analog-to-digital conversion** has two steps: **sampling** and **quantisation**. To sample a signal, we measure its amplitude at a particular time; the **sampling rate** is the number of samples taken per second. To accurately measure a wave, we must have at least two samples in each cycle: one measuring the positive part of the wave and one measuring the negative part. More than two samples per cycle increases the amplitude accuracy, but fewer than two samples causes the fre- quency of the wave to be completely missed. The maximum frequency wave that can be measured is one whose frequency is half the sample rate and is called the **Nyquist frequency**.

The process of representing real-valued numbers as integers is called **quantisation** because the difference between two integers acts as a minimum granularity (a quantum size) and all values that are closer together than this quantum size are represented identically.

**Telephone-bandwidth** speech is often sampled at 8 kHz and stored as 8-bit samples, and microphone data is often sampled at 16 kHz and stored as 16-bit samples.

Another parameter is the number of **channels**. For stereo data or for two-party conversations, we can store both channels in the same file or we can store them in separate files.

A final parameter is individual sample storage—linearly or compressed.

The intuition of log compression algorithms like *μ-law* is that human hearing is more sensitive at small intensities than large ones; the log represents small values with more faithfulness at the expense of more error on large values. The linear (unlogged) values are generally referred to as **linear PCM** values (PCM stands for pulse code modulation). Here’s the equation for compressing a linear PCM sample value x to 8-bit μ-law, (where μ=255 for 8 bits): $$ F(x) = { {sgn(x)\log{(1 + \mu|x|)}} \over {\log{(1 + \mu)}}} ~~~~ -1 \le x \le +1$$ There are a number of standard file formats for storing the resulting digitised wave–file, such as Microsoft’s .wav and Apple’s AIFF all of which have special headers; simple header–less “raw” files are also used.

### Frequency and Amplitude; Pitch and Loudness
The frequency of the vocal fold vibration, or the frequency of the complex wave, is called the **fundamental frequency** of the waveform, often abbreviated **F0**. We can plot F0 over time in a pitch track.
![Phonetics_12](notes/learning-courses/Stanford%20CS224S%20—%20Spoken%20Language%20Processing/Week%201/figures/Phonetics_12.png)
Pitch track of the question _Three o’clock?_, shown below the wave–file. Note the rise in F0 at the end of the question. Note the lack of pitch trace during the very quiet part (the _o’_ of _o’clock_; automatic pitch tracking is based on counting the pulses in the voiced regions, and doesn’t work if there is no voicing (or insufficient sound).

In addition to this value of the amplitude at any point in time, we also often need to know the average amplitude over some time range, to give us some idea of how great the average displacement of air pressure is. We generally use the RMS (root-mean-square) amplitude, which squares each number before averaging (making it positive), and then takes the square root at the end. $$ \text{RMS~amplitude}_{i=1}^{N} = \sqrt{ {1 \over N} \sum _{i=1}^{N} {x_i^2} } $$

The **power** of the signal is related to the square of the amplitude. If the number of samples of a sound is N, the power is $$ \text{Power} = {1 \over N} \sum _{i=1}^{N} {x_i^2} $$

Rather than power, we more often refer to the **intensity** of the sound, which normalises the power to the human auditory threshold and is measured in dB. If P0 is the auditory threshold pressure $2 \times {10}^{-5}$, then intensity is defined as follows: $$ \text{Intensity} = 10\log_{10}{1 \over {N P_0}} \sum _{i=1}^{N} {x_i^2} $$
![Phonetics_13](notes/learning-courses/Stanford%20CS224S%20—%20Spoken%20Language%20Processing/Week%201/figures/Phonetics_13.png)
Intensity plot for the sentence _Is it a long movie?_. Note the intensity peaks at each vowel and the especially high peak for the word _long_.

Two important perceptual properties, **pitch** and **loudness**, are related to frequency and intensity. The **pitch** of a sound is the mental sensation, or perceptual correlate, of fundamental frequency; in general, if a sound has a higher fundamental frequency we perceive it as having a higher pitch. We say “in general” because the relationship is not linear, since human hearing has different acuities for different frequencies. Roughly speaking, human pitch perception is most accurate between 100 Hz and 1000 Hz and in this range pitch correlates linearly with frequency. Human hearing represents frequencies above 1000 Hz less accurately, and above this range, pitch correlates logarithmically with frequency. Logarithmic representation means that the differences between high frequencies are compressed and hence not as accurately perceived. There are various psychoacoustic models of pitch perception scales. One common model is the **mel** scale (Stevens et al. 1937, Stevens and Volkmann 1940). A mel is a unit of pitch defined such that pairs of sounds which are perceptually equidistant in pitch are separated by an equal number of mels. The mel frequency m can be computed from the raw acoustic frequency as follows: $$ m ={1227}\ln(1 + {f \over 700}) $$

The **loudness** of a sound is the perceptual correlate of the **power**. So sounds with higher amplitudes are perceived as louder, but again the relationship is not linear. First of all, as we mentioned above when we defined μ-law compression, humans have greater resolution in the low-power range; the ear is more sensitive to small power differences. Second, it turns out that there is a complex relationship between power, frequency, and perceived loudness; sounds in certain frequency ranges are perceived as being louder than those in other frequency ranges. #todo: find graphs from [musimathics](http://www.musimathics.com).

Various algorithms exist for automatically extracting F0. In a slight abuse of terminology, these are called **pitch extraction** algorithms. The autocorrelation method of pitch extraction, for example, correlates the signal with itself at various offsets. The offset that gives the highest correlation gives the period of the signal. There are various publicly available pitch extraction toolkits; for example, an augmented autocorrelation pitch tracker is provided with Praat (Boersma and Weenink, 2005).

### Interpretation of Phones from a Waveform

# References
1. (Shoup, 1980): Shoup, J. E. 1980. Phonological aspects of speech recognition. In W. A. Lea, editor, Trends in Speech Recognition, pages 125–138. Prentice Hall.
2. (CMU, 1993): CMU. 1993. The Carnegie Mellon Pronouncing Dictionary v0.1. Carnegie Mellon University.
3. (Price et al. 1991): Price, P. J., M. Ostendorf, S. Shattuck- Hufnagel, and C. Fong. 1991. The use of prosody in syntactic disambiguation. JASA, 90(6).
4. (Bennett and Elfner 2019): Bennett, R. and E. Elfner. 2019. The syntax–prosody interface. Annual Review of Linguistics, 5:151–171.
5. (Ostendorf et al., 1995): Ostendorf, M., P. Price, and S. Shattuck-Hufnagel. 1995. The Boston University Radio News Corpus. Technical Report ECS-95-001, Boston University.
6. (Xu, 2005): Xu, Y. 2005. Speech melody as articulatorily implemented communicative functions. Speech communication, 46(3-4):220–251.
7. (Beckman and Ayers 1997): Beckman, M. E. and G. M. Ayers. 1997. Guidelines for ToBI labelling. Unpublished manuscript, Ohio State University, http://www.ling.ohio-state.edu/research/phonetics/E_ToBI/.
8. (Beckman and Hirschberg 1994): Beckman, M. E. and J. Hirschberg. 1994. The ToBI annotation conventions. Manuscript, Ohio State University.
9. (Silverman et al. 1992): Silverman, K., M. E. Beckman, J. F. Pitrelli, M. Ostendorf, C. W. Wightman, P. J. Price, J. B. Pierrehumbert, and J. Hirschberg. 1992. ToBI: A standard for labelling English prosody. ICSLP.
10. (Stevens et al. 1937): Stevens, S. S., J. Volkmann, and E. B. Newman. 1937. A scale for the measurement of the psychological magnitude pitch. JASA, 8:185–190.
11. (Stevens and Volkmann 1940): Stevens, S. S. and J. Volkmann. 1940. The relation of pitch to frequency: A revised scale. The American Journal of Psychology, 53(3):329–353.
12. (Boersma and Weenink, 2005): Boersma, P. and D. Weenink. 2005. Praat: doing phonetics by computer (version 4.3.14). [Computer program]. Retrieved May 26, 2005, from http://www.praat.org/.