# Moby Dick Word Frequency Analysis

This project analyzes the frequency of words in Herman Melville's *Moby Dick* using Python. It demonstrates how to fetch and process text data from Project Gutenberg, clean it, and analyze word frequencies using Natural Language Processing (NLP) techniques.

## Requirements

- `requests` - for fetching HTML content from Project Gutenberg
- `beautifulsoup4` - for parsing and extracting text from HTML
- `nltk` - for tokenization and removing stop words
- `collections` - for counting word frequencies

## Installation

To install the required libraries, use the following command:

```bash
pip install requests beautifulsoup4 nltk
```

## Workflow

1. **Fetching the Text**: The text of *Moby Dick* is fetched from Project Gutenberg as HTML using the `requests` library.
2. **Parsing HTML**: The HTML is parsed and the text content is extracted using `BeautifulSoup`.
3. **Tokenization**: The text is tokenized into words using `RegexpTokenizer` from `nltk`, which removes punctuation and non-alphanumeric characters.
4. **Text Normalization**: All words are converted to lowercase to avoid counting the same word in different cases (e.g., "Or" and "or").
5. **Stop Words Removal**: Common stop words (e.g., "the", "a", "and") are removed using the list provided by `nltk`.
6. **Counting Word Frequencies**: The frequency of each word is counted using the `Counter` class from Python's `collections` module.
7. **Displaying Results**: The top 10 most frequent words are displayed, along with the most common word in the novel.

## Example Output
```bash
Top 10 words and their counts: [('whale', 1399), ('whales', 414), ('ship', 376), ('man', 348), ('sea', 346), ('like', 345), ('good', 296), ('now', 290), ('time', 280), ('one', 279)]
Most common word in Moby Dick: whale
```

## Notes

- The program processes the entire novel, excluding common stop words.
- The most common word, unsurprisingly, is "whale," reflecting the novel's central theme.
