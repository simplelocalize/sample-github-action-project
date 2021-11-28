# Upload and Download tranlsation files with Github Actions


## Example download action

```yml
name: 'Download translations'
on:
  push:
    branches: [ main ]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Download translations
        uses: simplelocalize/download@latest
        with:
          apiKey: <YOUR_API_KEY>
          downloadPath: ./output-sample.json
          downloadFormat: multi-language-json
```

## Example upload action

```yml
name: 'Upload translations'
on:
  push:
    branches: [ main ]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Upload translations
        uses: simplelocalize/upload@1.0.0
        with:
          apiKey: <YOUR_API_KEY>
          uploadPath: ./input-sample.json
          uploadFormat: multi-language-json
```
