# We Love Lyrics — Activity Builder quick guide

Songs added in Creator Studio are stored in this browser's localStorage. Each song has six activity slots. You can enable the activity and enter exercises as JSON arrays. Leave the exercise box empty if you have not prepared any questions yet. Export the custom song catalog to share the data with another browser or to use it for the project hand-in.


## Example lesson: Twinkle Twinkle Little Star (public-domain nursery rhyme)
Use the following as a base exercise set; these are short public-domain lines and newly authored question prompts.

### Lyrics Challenge (`cfgLyrics`)
```json
[
  {"line": 0, "answer": "twinkle", "hint": "A small light shines repeatedly."},
  {"line": 1, "answer": "world", "hint": "The planet we live on."}
]
```

### Music Pause (`cfgMusicPause`)
The time is a sample timestamp. Adjust it to the YouTube version you use. Keep the phrase and answer in the exercise data.
```json
[
  {"time": 18, "line": "Twinkle, twinkle, little ____.", "target": "star", "choices": ["star", "moon", "cloud", "sun"], "meaning": "Star = estrella."},
  {"time": 34, "line": "How I wonder what you ____.", "target": "are", "choices": ["are", "do", "go", "see"], "meaning": "Wonder = preguntarse / sentir curiosidad."}
]
```

### Listening Challenge (`cfgListening`)
```json
[
  {"line": 0, "missing": ["twinkle"], "hint": "Starts with T."},
  {"line": 1, "missing": ["world"], "hint": "Starts with W."}
]
```

### Flashcards (`cfgFlashcards`)
```json
[
  {"front": "twinkle", "back": "brillar con destellos", "pronunciation": "/ˈtwɪŋ.kəl/"},
  {"front": "wonder", "back": "preguntarse / tener curiosidad", "pronunciation": "/ˈwʌn.dər/"}
]
```

### Vocabulary Practice (`cfgVocabulary`)
```json
[
  {"word": "twinkle", "meaning": "shine with small flashes of light", "example": "The stars twinkle at night."},
  {"word": "wonder", "meaning": "to feel curious and want to know something", "example": "I wonder why the sky is blue."}
]
```

### Translation Practice (`cfgTranslation`)
```json
[
  {"line": 0, "translation": "Brilla, brilla, pequeña estrella."},
  {"line": 1, "translation": "Me pregunto qué eres."}
]
```

**Data note:** the Activity Builder stores the configuration and labels enabled activities in the Creator Studio catalog. Music Pause is wired to use a song's configured rounds when present. Other activity screens in this demo still need their own runtime integration to consume these saved configurations; the saved settings are not yet a universal activity engine.
