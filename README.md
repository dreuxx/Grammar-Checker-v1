I don't know much English, so I used AI for the following text:

# Grammar Checker

Grammar Checker is a Chrome extension designed to review and improve grammar and spelling in multiple languages using the OpenAI API.

## Features

- **Grammar and Spelling Correction**: Reviews text in multiple languages and provides correction suggestions.
- **Multi-Language Support**: The extension supports the following languages:
  - Spanish
  - English
  - French
  - German
  - Italian
  - Portuguese
  - Indonesian
  - Polish
  - Vietnamese
  - Javanese
  - Turkish
- **Error Highlighting Without Modifying Original Text**: The extension identifies errors in the text and highlights them without modifying the original content. Errors are underlined with a dashed line, and hovering over them displays a correction suggestion.
- **Automatic Language Detection**: The extension automatically detects the text's language.
- **User-Friendly Interface**: The extension provides a simple interface where you can input text, see highlighted errors, and copy the result.
- **API Customization**: Allows you to enter and save your OpenAI API key in the settings.
- **Support for Long Texts**: It can review texts up to 2500 words.

## Requirements

- **OpenAI API**: You'll need an API key for the extension to work. You can sign up at [OpenAI](https://openai.com) and obtain a key on their website.
- **Chrome Browser**: The extension was developed and tested in Google Chrome.

## Installation

1. Clone or download this repository.
2. Open Chrome and go to `chrome://extensions/`.
3. Enable Developer Mode in the top right corner.
4. Click on "Load unpacked extension" and select the folder where you downloaded this repository.

## Configuration

1. Click the extension icon in the Chrome toolbar.
2. Enter your OpenAI API key in the corresponding field and click "Save API".
3. You can obtain an API key at [OpenAI API Keys](https://platform.openai.com/account/api-keys).
4. The API key is securely stored in Chrome storage.

## Usage

1. Open the extension by clicking on the Grammar Checker icon.
2. Enter the text you want to review in the input field (up to 2500 words).
3. Click on "Check Grammar" to receive correction suggestions.
4. Words with errors will be highlighted with a dashed underline. Hovering over them will show a correction suggestion.
5. You can copy the original text (without modifications) by clicking on "Copy corrected text".

## Main Files

- `background.js`: Manages installation events, configuration, and extension permissions.
- `manifest.json`: Defines the extension's configuration and permissions.
- `popup.html`: Contains the user interface for inputting and reviewing text.
- `popup.js`: Controls grammar correction logic, language detection, error highlighting, and communication with the OpenAI API.
- `styles.css`: Defines the design and style of the interface, including error highlighting.
- `content.js`: Handles text selection and communication with the webpage.
- `options.html` and `options.js`: Allow users to configure the OpenAI API key and model.

## Important Notes

- **Word Limit**: The extension allows you to review texts up to 2500 words.
- **Privacy**: All text processed is sent to the OpenAI API for corrections. Avoid including sensitive information in the submitted text.
- **Error Highlighting Without Changing Original Text**: The extension highlights grammatical and spelling errors without modifying the original text, allowing users to view errors without affecting the content.

## Example Implementation

```python
import openai
from langdetect import detect

class GrammarChecker:
    def __init__(self, api_key):
        self.api_key = api_key
        openai.api_key = api_key

    def check_grammar(self, text):
        try:
            language = detect(text)
            response = openai.ChatCompletion.create(
                model="gpt-3.5-turbo",
                messages=[
                    {"role": "system", "content": "You are an expert grammar and spelling checker."},
                    {"role": "user", "content": f"Check this text for grammar and spelling errors:\n\n{text}"}
                ],
                temperature=0.3
            )
            return {
                'status': 'success',
                'language': language,
                'suggestions': response.choices[0].message.content
            }
        except Exception as e:
            return {
                'status': 'error',
                'error': str(e)
            }

# Usage example
checker = GrammarChecker('your-api-key')
result = checker.check_grammar("Your text here")
print(result['suggestions'] if result['status'] == 'success' else result['error'])
```

## Contribution

If you would like to contribute to the project, please:

1. Fork the repository
2. Create a new branch for your changes
3. Submit a pull request

## License

This project is licensed under the MIT License. See the LICENSE file for more details.
