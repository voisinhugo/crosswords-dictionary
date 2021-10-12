# How should we retrieve the existing words (with definition)

- Status: [proposed | rejected | accepted | deprecated | … | superseded by [ADR-0005](0005-example.md)]

## Context and Problem Statement

We need to check easily if a word exists or not, at least in French, considering both common names and proper nouns. A bonus could be to have also a definition of the word, or at least a short description.

## Decision Drivers

- Price
- Works with common names and proper nouns
- Easy to retrieve (API)
- Handle blank space (joker)

## Considered Options

- PONS: https://fr.pons.com/p/dictionnaire-en-ligne/developers/api
- Free Dictionary API: https://dictionaryapi.dev/
- Wiktionary API: https://en.wiktionary.org/w/api.php
- WordReference API: https://www.programmableweb.com/api/wordreference-rest-api

## Decision Outcome

...

## Pros and Cons of the Options

| Option              | Price              | Support common names | Support proper nouns | Available API? | Handle jokers | Comments                                                                                                                                   |
| ------------------- | ------------------ | -------------------- | -------------------- | -------------- | ------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| PONS                | 3€ / 1000 requests | ✅                   | ❔                   | ✅             | ❔            |
| Free Dictionary API | ✅                 | ✅                   | ❌                   | ✅             | ❔            | Is recent, has a lot of success but might not stay live                                                                                    |
| Wiktionary API      | ✅                 | ✅                   | ❔                   | ❔             | ❔            | ⚠️ https://stackoverflow.com/a/4342777                                                                                                     |
| WordReference API   | ❔                 | ❔                   | ❔                   | ❔             | ❔            | Seems to be dead since [2021-06-03](https://web.archive.org/web/20200603095634/https://www.wordreference.com/licensing/dictionary_api.htm) |
