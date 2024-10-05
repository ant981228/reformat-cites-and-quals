# Reformat Quals & Cites

This tool allows you to automatically reformat qualifications and citations for debate evidence. It's designed for Windows users and consists of three main components:

1. `Reformat Quals & Cites.exe`
2. `quals_formatter.py`
3. `reformat_cite.py`

## Features

- Reformat qualifications into a cite-friendly format
- Reformats citations to a standardized format
- Customizable hotkeys
- Option to replace the default tooltips by sending your input to a whimsical creature named Clod, who will drop whatever he is doing to help you with your request. 

## Installation

1. Download and extract the ZIP file containing all components to a folder of your choice. All three files must be saved to the same folder. 

2. Install Python 3:
   - I recommend installing from the Microsoft Store.
   - Follow the instructions at: https://realpython.com/installing-python/#windows-how-to-install-python-from-the-microsoft-store

3. Install required Python packages:
   - Open Windows PowerShell (you may need to run as administrator)
   - Run the following command:
     ```
     pip install pyperclip anthropic
     ```

4. Obtain an Anthropic API key:
   - Follow the instructions at: https://www.merge.dev/blog/anthropic-api-key
   - The first time you run the program, you'll be prompted to enter your API key. It will be saved for future use.

5. (Optional) Set up the program to run on startup:
   - Right-click on `Reformat Quals & Cites.exe`
   - Choose "Send to" > "Desktop (create shortcut)"
   - Press Windows + R, type `shell:common startup`, and hit Enter
   - Move the shortcut from your desktop to the Startup folder that opens

## Usage

1. Run `Reformat Quals & Cites.exe` to start the program.

2. Use the following default hotkeys:
   - Ctrl+Shift+Q: Reformat qualifications
   - Ctrl+Shift+X: Reformat citations
   - Ctrl+Shift+G: Show help (displays current hotkey assignments)

3. To reformat qualifications:
   - Select the text containing qualifications
   - Press Ctrl+Shift+Q
   - The reformatted text will be copied to your clipboard

4. To reformat citations:
   - Select the text you would like to reformat into a citation
   - Press Ctrl+Shift+X
   - The reformatted citation will be automatically pasted

## Customization

You can change the hotkeys by editing the `ReformatQualsCite_Hotkeys.ini` file in the same directory as the executable. The file will be created with default values on first run if it doesn't exist.

You can configure your desired citation style by modifying the system prompt in `reformat_cite.py`. 

You can enable or disable Clod by editing the hotkeys configuration file. 

## Troubleshooting

- If you encounter any issues with Python or package installation, try running PowerShell as an administrator.
- Ensure all files are in the same directory.
- Check that your Anthropic API key is correctly entered and saved.

## Notes

- The program uses Claude, an AI model by Anthropic, to process and reformat the text. An internet connection is required for the program to function.
- Since this is powered by an AI LLM, be aware that the model may hallucinate. Double check citations and qualifications for accuracy.  
- Your API key is stored locally in a `config.ini` file for convenience and security.
