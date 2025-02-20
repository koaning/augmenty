# Overview of Augmenters

The following tables list all the available augmenters in augmenty, along with a short description. It also contains list all of the labels which the augmenters respects. For instance, if you wish to train a named entity recognition pipeline you should not use augmenters which do not respect entity labels. Similarly, a hint is also given to whether the augmenter is recommended for training or evaluation. Lastly, the package includes a list of references to any data or packages used as well as references to example application of the augmenter in practice.

| Augmenter name | Description | Token | Dependency parsing | Entity | Document | Training | Evaluation | References |
| :---: | --- | --- | --- | --- | --- | --- | --- | --- |
| **char_replace.v1** | Creates an augmenter that replaces a character with a random character from replace dict | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |  |
| **char_replace_random.v1** | Creates an augmenter that replaces a character with a random character from the     keyboard. | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |  |
| **char_swap.v1** | Creates an augmenter that swaps two neighbouring characters in a token with a given probability. | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |  |
| **conditional_token_casing.v1** | Creates an augmenter that conditionally cases the first letter of a token based on the getter.     Either lower og upper needs to specifiedd as True. | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |  |
| **da_historical_noun_casing.v1** | Creates an augmenter that capitalizes nouns. | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |  |
| **da_æøå_replace.v1** | Creates an augmenter that augments æ, ø, and å into their spelling variants ae, oe, aa. | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |  |
| **duplicate_token.v1** | Creates an augmenter that randomly duplicate a token token. | ✅ | ❌ | ✅ | ✅ | ✅ | ✅ |  |
| **ents_format.v1** | Creates an augmenter which reorders and formats a entity according to reordering and formatting functions. | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |  |
| **ents_replace.v1** | Create an augmenter which replaces an entity based on a dictionary lookup. | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |  |
| **grundtvigian_spacing_augmenter.v1** | The Danish philosopher N.F.S. Grundtvig used letter spacing to add      e m p h a s i s  to words (Baunvig, Jarvis and Nielbo, 2020).      This augmenter randomly adds letter spacing emphasis to words.      This augmentation which are human readable, but which are clearly      challenging for systems using a white-space centric tokenization. | ✅ | ✅ | ✅ | ✅ | ✅ |  |  |
| **keystroke_error.v1** | Creates a augmenter which augments a text with plausible typos based on keyboard distance. | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |  |
| **per_replace.v1** | Create an augmenter which replaces a name (PER) with a news sampled from the names dictionary. | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |  |
| **random_casing.v1** | Create an augment that randomly changes the casing of the document. | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |  |
| **random_starting_case.v1** | Creates an augmenter which randomly cases the first letter in each token. | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |  |
| **random_synonym_insertion.v1** | Creates an augmenter that randomly inserts a synonym or from the tokens context.     The synonyms are based on wordnet. | ✅ | ❌ | ✅ | ✅ | ✅ | ✅ |  |
| **remove_spacing.v1** | Creates an augmenter that removes spacing with a given probability. | ✅ | ✅ | ✅ | ✅ | ✅ |  |  |
| **spacing_insertion.v1** | Creates and augmneter that randomly adds a space after a chara cter. Tokens are kept the same. | ✅ | ✅ | ✅ | ✅ | ✅ |  |  |
| **spacy.lower_case.v1** | Create a data augmentation callback that converts documents to lowercase.     The callback can be added to a corpus or other data iterator during training. | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |  |
| **spacy.orth_variants.v1** | Create a data augmentation callback that uses orth-variant replacement.     The callback can be added to a corpus or other data iterator during training. | ✅ | ✅ | ✅ | ✅ |  | ✅ |  |
| **spongebob.v1** | Create an augmneter that converts documents to SpOnGeBoB casing. | ✅ | ✅ | ✅ | ✅ | ✅ |  |  |
| **token_dict_replace.v1** | Creates an augmenter swaps a token with its synonym based on a dictionary. | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |  |
| **token_insert.v1** | Creates an augmenter that randomly inserts a token generated based on a insert function. | ✅ | ❌ | ✅ | ✅ | ✅ | ✅ |  |
| **token_insert_random.v1** | Creates an augmenter that randomly swaps two neighbouring tokens. | ✅ | ❌ | ✅ | ✅ | ✅ | ✅ |  |
| **token_replace.v1** | Creates an augmenter which replaces a token based on a replace function. | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |  |
| **token_swap.v1** | Creates an augmenter that randomly swaps two neighbouring tokens. | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | Usage: [Wei and Zau (2019)](https://arxiv.org/abs/1901.11196?utm_campaign=Weekly%20Kaggle%20News&utm_medium=email&utm_source=Revue%20newsletter) |
| **upper_case.v1** | Create an augmenter that converts documents to uppercase. | ✅ | ✅ | ✅ | ✅ | ✅ |  |  |
| **word_embedding.v1** | Creates an augmenter which replaces a token based on a replace function. | ✅ | ✅ | ✅ | ✅ |  | ✅ |  |
| **wordnet_synonym.v1** | Creates an augmenter swaps a token with its synonym based on a dictionary. | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | Data: [Miller (1998)](https://www.google.com/books?hl=da&lr=&id=Rehu8OOzMIMC&oi=fnd&pg=PR11&dq=WordNet:+An+electronic+lexical+database&ots=IsieQmWUg8&sig=06asxxcQ1I3i9C1TcEcz7bv62Kw), Package: [Steven (2006)](https://www.nltk.org), Usage: [Wei and Zau (2019)](https://arxiv.org/abs/1901.11196?utm_campaign=Weekly%20Kaggle%20News&utm_medium=email&utm_source=Revue%20newsletter) |