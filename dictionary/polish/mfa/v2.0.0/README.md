
# Polish MFA dictionary v2.0.0

[Link to documentation on mfa-models](https://mfa-models.readthedocs.io/en/main/dictionary/polish_mfa.html)

Jump to section:

- [Dictionary details](#dictionary-details)
- [Intended use](#intended-use)
- [Performance Factors](#performance-factors)
- [Ethical considerations](#ethical-considerations)

## Dictionary details

- **Maintainer:** [Montreal Forced Aligner](https://montreal-forced-aligner.readthedocs.io/)
- **Language:** [Polish](https://en.wikipedia.org/wiki/Polish_language)
- **Dialect:** N/A
- **Phone set:** [MFA](https://mfa-models.readthedocs.io/en/refactor/mfa_phone_set.html#polish)
- **Number of words:** `134,369`
- **Phones:** {ipa_inline}`a`, {ipa_inline}`b`, {ipa_inline}`bʲ`, {ipa_inline}`c`, {ipa_inline}`dʐ`, {ipa_inline}`dʑ`, {ipa_inline}`d̪`, {ipa_inline}`d̪z̪`, {ipa_inline}`f`, {ipa_inline}`fʲ`, {ipa_inline}`i`, {ipa_inline}`j`, {ipa_inline}`j̃`, {ipa_inline}`k`, {ipa_inline}`l`, {ipa_inline}`m`, {ipa_inline}`mʲ`, {ipa_inline}`n̪`, {ipa_inline}`p`, {ipa_inline}`pʲ`, {ipa_inline}`r`, {ipa_inline}`rʲ`, {ipa_inline}`s̪`, {ipa_inline}`tɕ`, {ipa_inline}`tʂ`, {ipa_inline}`tʲ`, {ipa_inline}`t̪`, {ipa_inline}`t̪s̪`, {ipa_inline}`u`, {ipa_inline}`v`, {ipa_inline}`vʲ`, {ipa_inline}`w`, {ipa_inline}`x`, {ipa_inline}`z̪`, {ipa_inline}`ç`, {ipa_inline}`ŋ`, {ipa_inline}`ɔ`, {ipa_inline}`ɔ̃`, {ipa_inline}`ɕ`, {ipa_inline}`ɛ`, {ipa_inline}`ɛ̃`, {ipa_inline}`ɟ`, {ipa_inline}`ɡ`, {ipa_inline}`ɨ`, {ipa_inline}`ɲ`, {ipa_inline}`ʂ`, {ipa_inline}`ʎ`, {ipa_inline}`ʐ`, {ipa_inline}`ʑ`, {ipa_inline}`ʔ`
- **License:** [CC BY 4.0](https://github.com/MontrealCorpusTools/mfa-models/tree/main/dictionary/polish/MFA/v2.0.0/LICENSE)
- **Compatible MFA version:** `v2.0.0`
- **Citation:**

```bibtex
@techreport{
	mfa_polish_mfa_dictionary_2022,
	author={McAuliffe, Michael and Sonderegger, Morgan},
	title={Polish MFA dictionary v2.0.0},
	address={\url{https://mfa-models.readthedocs.io/pronunciation dictionary/Polish/Polish MFA dictionary v2_0_0.html}},
	year={2022},
	month={Mar},
}
```

- If you have comments or questions about this dictionary or its phone set, you can check [previous MFA model discussion posts](https://github.com/MontrealCorpusTools/mfa-models/discussions?discussions_q=Polish+MFA+dictionary+v2.0.0) or create [a new one](https://github.com/MontrealCorpusTools/mfa-models/discussions/new).

## Installation

Install from the [MFA command line](https://montreal-forced-aligner.readthedocs.io/en/latest/user_guide/models/index.html):

```
mfa models download dictionary polish_mfa
```

Or download from [the release page](https://github.com/MontrealCorpusTools/mfa-models/releases/tag/dictionary-polish_mfa-v2.0.0).

## Intended use

This dictionary is intended for forced alignment of [Polish](https://en.wikipedia.org/wiki/Polish_language) transcripts.

This dictionary uses the [MFA](https://mfa-models.readthedocs.io/en/refactor/mfa_phone_set.html#polish) phone set for Polish, and was used in training the Polish [MFA](https://mfa-models.readthedocs.io/en/refactor/mfa_phone_set.html#polish) acoustic model.
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