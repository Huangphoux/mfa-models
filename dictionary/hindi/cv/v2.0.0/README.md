
# Hindi CV dictionary v2.0.0

[Link to documentation on mfa-models](https://mfa-models.readthedocs.io/en/main/dictionary/hindi_cv.html)

Jump to section:

- [Dictionary details](#dictionary-details)
- [Intended use](#intended-use)
- [Performance Factors](#performance-factors)
- [Ethical considerations](#ethical-considerations)

## Dictionary details

- **Maintainer:** [Vox Communis](https://osf.io/t957v/)
- **Language:** [Hindi](https://en.wikipedia.org/wiki/Hindi_language)
- **Dialect:** N/A
- **Phone set:** [Epitran](https://github.com/dmort27/epitran)
- **Number of words:** `11,113`
- **Phones:** {ipa_inline}`a`, {ipa_inline}`aː`, {ipa_inline}`b`, {ipa_inline}`b̤`, {ipa_inline}`d`, {ipa_inline}`d̤`, {ipa_inline}`d͡ʒ`, {ipa_inline}`d͡ʒ̤`, {ipa_inline}`e`, {ipa_inline}`f`, {ipa_inline}`h`, {ipa_inline}`i`, {ipa_inline}`iː`, {ipa_inline}`j`, {ipa_inline}`k`, {ipa_inline}`kʰ`, {ipa_inline}`l`, {ipa_inline}`m`, {ipa_inline}`n`, {ipa_inline}`o`, {ipa_inline}`p`, {ipa_inline}`pʰ`, {ipa_inline}`q`, {ipa_inline}`r`, {ipa_inline}`r̩`, {ipa_inline}`s`, {ipa_inline}`t`, {ipa_inline}`tʰ`, {ipa_inline}`t͡ʃ`, {ipa_inline}`t͡ʃʰ`, {ipa_inline}`u`, {ipa_inline}`uː`, {ipa_inline}`v`, {ipa_inline}`w`, {ipa_inline}`x`, {ipa_inline}`z`, {ipa_inline}`ã`, {ipa_inline}`ãː`, {ipa_inline}`æ`, {ipa_inline}`æː`, {ipa_inline}`ŋ`, {ipa_inline}`ũ`, {ipa_inline}`ũː`, {ipa_inline}`ɑ`, {ipa_inline}`ɔ`, {ipa_inline}`ɔː`, {ipa_inline}`ɖ`, {ipa_inline}`ɖ̤`, {ipa_inline}`ə`, {ipa_inline}`ə̃`, {ipa_inline}`ɛ`, {ipa_inline}`ɡ`, {ipa_inline}`ɡ̤`, {ipa_inline}`ɣ`, {ipa_inline}`ɦ`, {ipa_inline}`ɪ`, {ipa_inline}`ɲ`, {ipa_inline}`ɳ`, {ipa_inline}`ɹ`, {ipa_inline}`ɹ̩`, {ipa_inline}`ɽ`, {ipa_inline}`ɽ̥`, {ipa_inline}`ʂ`, {ipa_inline}`ʃ`, {ipa_inline}`ʈ`, {ipa_inline}`ʈʰ`, {ipa_inline}`ʊ`, {ipa_inline}`ʌ`, {ipa_inline}`θ`, {ipa_inline}`ẽ`
- **License:** [CC-0](https://creativecommons.org/publicdomain/zero/1.0/)
- **Compatible MFA version:** `v2.0.0`
- **Citation:**

```bibtex
@misc{
	Ahn_Chodroff_2022,
	author={Ahn, Emily and Chodroff, Eleanor},
	title={VoxCommunis Corpus},
	address={\url{https://osf.io/t957v}},
	publisher={OSF},
	year={2022},
	month={Jan}
}
```

- If you have comments or questions about this dictionary or its phone set, you can check [previous MFA model discussion posts](https://github.com/MontrealCorpusTools/mfa-models/discussions?discussions_q=Hindi+CV+dictionary+v2.0.0) or create [a new one](https://github.com/MontrealCorpusTools/mfa-models/discussions/new).

## Installation

Install from the [MFA command line](https://montreal-forced-aligner.readthedocs.io/en/latest/user_guide/models/index.html):

```
mfa models download dictionary hindi_cv
```

Or download from [the release page](https://github.com/MontrealCorpusTools/mfa-models/releases/tag/dictionary-hindi_cv-v2.0.0).

## Intended use

This dictionary is intended for forced alignment of [Hindi](https://en.wikipedia.org/wiki/Hindi_language) transcripts.

This dictionary uses the [Epitran](https://github.com/dmort27/epitran) phone set for Hindi, and was used in training the Hindi [Epitran](https://github.com/dmort27/epitran) acoustic model.
Pronunciations can be added on top of the dictionary, as long as no additional phones are introduced.

## Performance Factors

When trying to get better alignment accuracy, adding pronunciations is generally helpful, espcially for different styles and dialects.
The most impactful improvements will generally be felt when adding reduced variants that
involve deleting segments/syllables common in spontaneous speech.  Alignment must include all phones specified in the pronunciation of a word, and each phone has
a minimum duration (by default 10ms). If a speaker pronounces a multisyllabic word with just a single syllable, it can be hard for MFA to fit all the segments in,
so it will lead to alignment errors on adjacent words as well.

## Ethical considerations

Deploying any Speech-to-Text model into any production setting has ethical implications. You should consider these implications before use.

### Demographic Bias

You should assume every machine learning model has demographic bias unless proven otherwise.
For pronunciation dictionaries, it is often the case that transcription accuracy and lexicon coverage for the prestige variety modeled in this dictionary compared to other variants.
If you are using this dictionary in production, you should acknowledge this as a potential issue.