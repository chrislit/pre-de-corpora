pre-de-corpora
==============

pre-Neuhochdeutsch corpora

This is a set of corpora of pre-Neuhochdetusch German texts. The sources for these data are (most of the) pre-17th century German texts from:
* Biblioteca Augustana (http://www.hs-augsburg.de/~harsch/germanica/Chronologie/d_chrono.html)
* Wikisource (https://de.wikisource.org/)

The texts have been stripped of markup and cleaned up somewhat. Then they were split into clauses by a script with very coarse heuristics, sometimes quite inaccurately. These sentences were Unicode normalized (to NFC) and lowercased.

## Contents
At present, the only corpora being made available are n-gram corpora (for n=1 to 5). These are provided in four sets:

| set                           | date range | directory        | unique tokens | 1-grams | 2-grams | 3-grams | 4-grams | 5-grams |
|-------------------------------|------------|------------------|--------------:|--------:|--------:|--------:|--------:|--------:|
| Old High German (Ahd.)        | 750-1000   | /Ahd/ngrams      | 54471         | 10904   | 38516   | 49859   | 49947   | 47326   |
| Middle High German (Mhd.)     | 1000-1400  | /Mhd/ngrams      | 1187089       | 83189   | 586122  | 1001540 | 1052231 | 992440  |
| Early New High German (Fnhd.) | 1400-1600  | /Fnhd/ngrams     | 976925        | 92602   | 543008  | 851157  | 888457  | 862754  |
| all three of the foregoing    | 750-1600   | /combined/ngrams | 2218485       | 186695  | 1167646 | 1902556 | 1990635 | 1902520 |

## Format
The format of each corpus borrows from the formatting of Google's Ngram dataset files:
 1. Each line contains one record, terminated by a newline.
 2. Each n-gram record contains n+2 space-separated fields:
   1. The first n fields contain the n-gram itself.
   2. The n+1th field indicates the date of the n-gram, rounded up to the next century. (So an n-gram from a text from 750 will have '800' in this field. The date is intended as a terminus ad quem for the work)
   3. The n+2th field indicates the count number of times the n-gram appeared across all texts within the given century.

## License
These corpora are contributed to the public domain and licensed under CC0 1.0 Universal.
