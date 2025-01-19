# SteadyType

SteadyType is a Python-based program designed to assist individuals with medical conditions such as Parkinson's disease, where typing can be challenging due to tremors or sudden, uncontrolled motor movements. By providing real-time spelling and grammar correction, it makes typing easier and more accurate. The program uses the Gemini language model from Google's Generative AI suite to intelligently correct text, simulating keystrokes to apply corrections.

## Features

- **Real-Time Typing Correction**: Detects pauses in typing and autocorrects the text you've typed.
- **Grammar and Spelling Checks**: Utilizes the Gemini AI model to perform accurate corrections.
- **Keyboard Interaction**: Simulates keystrokes to delete incorrect text and replace it with corrected text.

## How It Works

1. **Key Listening**: Tracks keys pressed and builds a string of text as you type.
2. **Pause Detection**: Monitors for a typing pause of at least 2 seconds.
3. **Text Correction**: Sends the text to the Gemini model for spelling and grammar correction.
4. **Text Replacement**: Deletes the incorrect text and replaces it with the corrected version using simulated keystrokes.

## Prerequisites

- Python 3.8 or higher
- `pynput` library for keyboard interaction
- `google.generativeai` library for AI-powered corrections

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/GlobalAutocorrect.git
   cd GlobalAutocorrect
   ```
2. Install the required dependencies:
   ```bash
   pip install pynput google-generativeai
   ```
3. Set up your Gemini API key:
   - Obtain an API key for the Google Generative AI Gemini model.
   - Replace the `api_key` in the `GlobalAutocorrect` class with your API key:
     ```python
     genai.configure(api_key="YOUR_API_KEY_HERE")
     ```

## Usage

1. Run the program:
   ```bash
   python global_autocorrect.py
   ```
2. Start typing anywhere (e.g., in a browser, text editor, etc.). The program will detect pauses in your typing and automatically correct the text.
3. Press `Ctrl+C` in the terminal to stop the program.

## Example

### Before Correction:
```
this is an exampl of a smple text with erors
```

### After Correction:
```
This is an example of a simple text with errors.
```

## Limitations

- The program requires an active internet connection to interact with the Gemini model.
- Only English text correction is supported.
- Typing corrections may interfere with applications that have custom keyboard behaviors.

## Roadmap

- Add support for multiple languages.
- Improve pause detection logic.
- Implement configuration options for pause duration and correction models.

## Contributing

Contributions are welcome! Feel free to fork the repository and submit a pull request. Please ensure your code follows PEP 8 style guidelines.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

## Acknowledgments

- [Pynput](https://pypi.org/project/pynput/) for keyboard event handling.
- [Google Generative AI](https://ai.google/) for the powerful Gemini language model.

