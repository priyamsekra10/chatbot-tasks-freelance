# Audio-to-Text and Document Generation

## Task
Convert an audio file (speech) to text and generate a structured document summarizing patient information, including automatically marking checkboxes based on the patient's state (e.g., vitals, symptoms).

### Requirements
- Use any audio-to-text model (e.g., Google Speech-to-Text, Whisper).
- Generate output in PDF/Word format with dynamic checkbox marking.

---

## How to Run
1. Ensure Python 3 is installed.
2. Install required packages:
   ```bash
   pip install openai python-docx python-dotenv
   ```
3. Set up environment variables by creating a `.env` file:
   ```
   OPENAI_API_KEY=your_openai_api_key
   ```
4. Place your audio file in the project directory and name it `audio.mp3`.
5. Run the script:
   ```bash
   python3 main.py
   ```

---

## Code Summary

### Main Steps
1. **Environment Setup:** Load API keys from `.env` file.
2. **Audio-to-Text Conversion:** Use OpenAI's Whisper model to transcribe `audio.mp3`.
3. **Patient Summary Generation:**
   - Use GPT-based model to extract symptoms and mark checkboxes dynamically.
4. **Document Generation:** Save the summary as a Word document `Patient_Symptoms_Summary.docx`.

---

## Example Output
- **Patient Symptoms Summary (Word Document):**
  - Transcription summary.
  - Marked checkboxes indicating symptom presence.

---

## Notes
- Ensure your OpenAI API key is valid.
- Modify `audio_file` and file-saving paths as needed.
- For extended functionality, consider adding PDF output support.

---

## Future Improvements
- Add support for multiple audio file formats.
- Enable live audio input.
- Include additional health indicators for comprehensive reports.

---

### Disclaimer
This project is a demo for educational purposes. It should not be used for real patient diagnostics.

