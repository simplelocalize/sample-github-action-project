# Synchronize tranlsation files with SimpleLocalize

This Github Actions uses official and open-source SimpleLocalize CLI.

Learn more: https://github.com/simplelocalize/simplelocalize-cli

## ☁️ Example download action

```yml
name: 'Download translations'
on:
  push:
    branches: [ main, master ]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Download translations
        uses: simplelocalize/download@latest
        with:
          apiKey: <YOUR_API_KEY>
          downloadPath: ./locales/{ns}/{lang}-messages.json
          downloadFormat: multi-language-json
```

## ☁️ Example upload action

```yml
name: 'Upload translations'
on:
  push:
    branches: [ main, master ]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Upload translations
        uses: simplelocalize/upload@latest
        with:
          apiKey: <YOUR_API_KEY>
          uploadPath: ./locales/{ns}/{lang}-messages.json
          uploadFormat: multi-language-json
```
