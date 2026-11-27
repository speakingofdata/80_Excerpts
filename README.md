# 80_Excerpts

### Harper Strickland, 2025

## Description:

This repository contains a speech corpus of 320 recordings (80 transcripts x 4 speakers). The 80 selections are taken from 38 public domain source texts, all with full-chapter audio recordings available from [LibriVox.org][1]. All LibriVox audio recordings are in the public domain.

[1]: <https://librivox.org/pages/about-librivox/> "About LibriVox"

30 excerpts are from recordings available in the [LJ Speech Dataset][2], and 30 are from recordings represented in the [LJ2 Corpus][3]. For each set of 30, 20 are from source texts that appear in only one of these corpora, and 10 are from sources with chapters existing in both. Both LJ Speech and the LJ2 Corpus contain only nonfiction texts. The final 20 excerpts are from fiction source chapters available on LibriVox from the same reader.

[2]: <https://keithito.com/LJ-Speech-Dataset/> "Access LJ Speech"
[3]: <https://github.com/speakingofdata/LJ2_Corpus> "Access LJ2 Corpus"

Each excerpt is read by multiple adult American voices, with multiple genders represented. 'LJ' is the voice of LJ Speech and the LJ2 Corpus.


## Summary Statistics:

**Transcript Details:**

sources            | excerpts | 1 sentence | < sentence | > sentence | mean words | min words | max words
:----------------- | -------: | ---------: | ---------: | ---------: | ---------: | --------: | --------:
LJ Speech unique   | 20       | 14         | 5          | 1          | 18.5       | 10        | 30      |
LJ Speech shared   | 10       | 8          | 2          | 0          | 19.9       | 14        | 27      |
LJ2 Corpus unique  | 20       | 12         | 6          | 2          | 18.3       | 6         | 28      |
LJ2 Corpus shared  | 10       | 8          | 2          | 0          | 16.9       | 5         | 25      |
Librivox fiction   | 20       | 8          | 9          | 3          | 18.6       | 3         | 31      |

**Voice Characteristics:**

readers | demographic | mean duration | min duration | max duration | words per min | pause time | mean F0 | F0 range   | mean F1 | mean F2 | mean F3 | HNR     | jitter | shimmer
:------ | :---------- | ------------: | -----------: | -----------: | ------------: | ---------: | ------: | ---------: | ------: | ------: | ------: | ------: | -----: | ------:
LJ      | woman       | 7.01 sec      | 2.10 sec     | 9.98 sec     | 159           | 14.6%      | 209 Hz  | 100–500 Hz | 531 Hz  | 1708 Hz | 2808 Hz | 12.4 dB | 2.1%   | 8.7%  |
MB      | woman       | 7.05 sec      | 1.82 sec     | 10.97 sec    | 158           | 15.8%      | 176 Hz  | 100–494 Hz | 621 Hz  | 1664 Hz | 2711 Hz | 7.8 dB  | 1.5%   | 9.5%  |
WS      | man         | 5.57 sec      | 1.47 sec     | 8.91 sec     | 201           | 5.8%       | 109 Hz  | 75–298 Hz  | 518 Hz  | 1572 Hz | 2509 Hz | 7.3 dB  | 2.5%   | 11.7% |
HS      | nonbinary   | 6.13 sec      | 1.47 sec     | 11.93 sec    | 182           | 9.8%       | 184 Hz  | 85–399 Hz  | 440 Hz  | 1518 Hz | 2356 Hz | 12.1 dB | 2.4%   | 9.9%  |


## Files:

- `metadata_80.csv`

	Includes for each excerpt, not only the identifying number and transcript, but also subset, source corpus, LibriVox Source id number (foreign key), and wav file durations for each reader.

- `LV_books_data_80.json`

	Original source metadata available via LibriVox's [API][4]: id number, title, description, language, copyright year, section/chapter count, urls (text source, rss, zip file, project, LibriVox), total time (h\:m\:s and seconds), authors (name and birth/death years).

[4]: <https://librivox.org/api/info> "LibriVox API documentation"

- `books_enrichment_80.csv`

	Additional source metadata: LibriVox id number (primary key), updated title (if incomplete in LibriVox API), LibriVox recordings upload date, count and duration of sections read by Linda Johnson ('LJ').

- Audio recordings:
	- Audio files for LJ, WS, HS can be downloaded from [`/wavs`][5] directory, containing a subdirectory for each reader.
	- Access to MB recordings is limited based on intended use; for more information, contact <a href="mailto:speakingofdata\@protonmail.com">speakingofdata\@protonmail.com</a> with project details and requirements.

[5]: <https://github.com/speakingofdata/80_Excerpts/tree/main/wavs> "wavs subdirectory"
