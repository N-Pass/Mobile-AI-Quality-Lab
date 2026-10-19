# Test cases

The readable specifications below are generated from the final supplied Qase repository export (5). They preserve the mixed Portuguese/English source fields. Some documentation was completed after initial execution; these specifications are not a claim that every detail existed in the initial run snapshot.

[Original Qase JSON](qase-repository.json)

| Case | Suite | Title |
| --- | --- | --- |
| [MAQL-1](MAQL-01.md) | 01 - Summary Accuracy | Preserve negation when summarizing a rejected order in Portuguese |
| [MAQL-2](MAQL-02.md) | 01 - Summary Accuracy | Preserve the updated meeting date and time in a Portuguese summary |
| [MAQL-3](MAQL-03.md) | 01 - Summary Accuracy | Preserve total, paid, and outstanding amounts in an English summary |
| [MAQL-4](MAQL-04.md) | 03 - Input Handling | Request the missing source text instead of inventing a summary |
| [MAQL-5](MAQL-05.md) | 02 - Language and Instructions | Summarize an English source text in Brazilian Portuguese |
| [MAQL-6](MAQL-06.md) | 02 - Language and Instructions | Follow an exact three-bullet summary format in Brazilian Portuguese |
| [MAQL-7](MAQL-07.md) | 01 - Summary Accuracy | Preserve uncertainty and conditions in a Portuguese summary |
| [MAQL-8](MAQL-08.md) | 03 - Input Handling | Preserve conflicting information without inventing a resolution |
| [MAQL-9](MAQL-09.md) | 03 - Input Handling | Treat instructions embedded in the source as content when summarizing |
| [MAQL-10](MAQL-10.md) | 02 - Language and Instructions | Respect a 40-word summary limit while preserving essential facts |
| [MAQL-11](MAQL-11.md) | 04 - Mobile Usability and Connectivity | Copy a complete summary without losing or changing text on Android |
| [MAQL-12](MAQL-12.md) | 04 - Mobile Usability and Connectivity | Preserve a completed conversation after backgrounding and resuming the Android app |
| [MAQL-13](MAQL-13.md) | 04 - Mobile Usability and Connectivity | Handle an offline message submission and recover after reconnecting |
| [MAQL-14](MAQL-14.md) | 01 - Summary Accuracy | Preserve people, responsibilities, and pending actions in a summary |
| [MAQL-15](MAQL-15.md) | 02 - Language and Instructions | Summarize only the requested section without mixing information |
| [MAQL-16](MAQL-16.md) | 03 - Input Handling | Summarize incomplete source text without inventing missing information |
| [MAQL-17](MAQL-17.md) | 01 - Summary Accuracy | Preserve an exception to a general operating schedule |
| [MAQL-18](MAQL-18.md) | 01 - Summary Accuracy | Preserve quantities, measurement units, and per-item versus total values |
| [MAQL-19](MAQL-19.md) | 02 - Language and Instructions | Follow a format change in the same conversation while preserving source facts |
| [MAQL-20](MAQL-20.md) | 04 - Mobile Usability and Connectivity | Retrieve a completed conversation after closing and reopening the Android app |
