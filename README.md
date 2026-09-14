# convAI 🗣️

> A minimal voice assistant loop: microphone → speech‑to‑text → GPT with a product‑specific system persona → text‑to‑speech. Built as the conversational prototype for the OpenDroids **R1D1** home robot.

[![Python 3.10+](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/)
[![LLM: OpenAI](https://img.shields.io/badge/LLM-OpenAI-412991)](https://platform.openai.com/)
[![License: MIT](https://img.shields.io/badge/license-MIT-yellow.svg)](LICENSE)

```mermaid
flowchart LR
    M[Microphone] --> SR[speech_recognition]
    SR --> LLM[OpenAI chat<br/>R1D1 persona + product knowledge]
    LLM --> TTS[pyttsx3]
    TTS --> SPK[Speaker]
```

## Run

```bash
pip install -r requirements.txt
export OPENAI_API_KEY=...          # read from env; nothing hard‑coded
python app.py
```

The persona and product knowledge live in `system_instruction` inside `app.py`; edit it to repurpose the assistant for any product.

## License

MIT — see [LICENSE](LICENSE).
