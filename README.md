AI notebooks for qualitative research
Google Colab notebooks that show how open AI models, running on PyTorch, and computational data collection can support qualitative research in the social sciences without replacing the researcher's interpretation. They are written in Spanish and designed for interview-based and digital-media studies in Latin America.
Author: Victor Omar Vite León (Universidad Peruana de Ciencias Aplicadas) · ORCID 0000-0002-0206-5858
Notebooks
Notebook	What it does	Open
`transcripcion_entrevistas_whisper.ipynb`	Transcribes Spanish-language interviews and focus groups with OpenAI's open Whisper model. Adds timestamps, replaces participants' names with codes, optionally separates speakers with pyannote, and exports Word, plain text, SRT and VTT files.	![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)
`clasificacion_respuestas_huggingface.ipynb`	Classifies open-ended responses with a multilingual zero-shot model from Hugging Face and compares it with human coding and with an LLM accessed via API (percent agreement, Cohen's kappa, disagreement table). Optionally explores similarity between responses with sentence embeddings.	![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)
`comentarios_youtube.ipynb`	Collects public comments from one or more YouTube videos as a corpus for thematic analysis or digital ethnography. Pseudonymizes authors by default, keeps reply threads, runs basic quality checks (empty and duplicate comments), and exports CSV, Excel and a data-collection record for the Methods section.	![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)
Why
Generative AI is entering qualitative research mostly through commercial chat interfaces, with little transparency about what is done to the data. These notebooks take a different route:
Open models, documented procedures. Each notebook records the model, version and parameters used, so the procedure can be reported in a Methods section and reproduced.
The machine as a point of comparison, not a judge. Automatic coding is used to contrast and audit human coding; disagreements are treated as analytic material, not as errors.
Data protection by design. Pseudonymization happens during transcription, and the notebooks remind the researcher to check informed consent and ethics approval before processing real data.
Human review is mandatory. Every automatic transcript is labeled as pending review until the researcher checks it against the audio.
They support an ongoing research line on AI as a research assistant: how its use relates to university students' self-efficacy, academic engagement, and participation in scientific research.
How to use
Click Open in Colab next to a notebook.
In Colab, choose Runtime → Change runtime type → T4 GPU (free).
Run the cells in order. Instructions in each notebook explain what to adjust.
The classification notebook includes fictitious practice responses. No real participant data is included in this repository.
Data and ethics
Colab runs on Google's servers: audio and text are not sent to the model developers, but they are processed in Google's cloud. Check that this is compatible with your participants' informed consent and your ethics committee's approval. For maximum confidentiality, the same code can run on a local machine with a GPU.
Never commit notebooks with outputs from real data. Before saving a notebook you have run, use Edit → Clear all outputs.
The YouTube notebook reads the public comments page through the `youtube-comment-downloader` library rather than the official YouTube Data API, which YouTube's Terms of Service restrict. For funded projects, data sharing, or strict ethics review, use the YouTube Data API v3 instead. Public comments still call for care: do not publish collected corpora, and paraphrase or keep quotations brief when topics are sensitive (franzke et al., 2020).
Citation
If you use these notebooks, please cite this repository and the underlying models:
Radford, A., Kim, J. W., Xu, T., Brockman, G., McLeavey, C., & Sutskever, I. (2023). Robust speech recognition via large-scale weak supervision. Proceedings of the 40th International Conference on Machine Learning, PMLR 202, 28492–28518.
Bredin, H. (2023). pyannote.audio 2.1 speaker diarization pipeline: Principle, benchmark, and recipe. Proceedings of Interspeech 2023, 1983–1987.
franzke, a. s., Bechmann, A., Zimmer, M., Ess, C., & the Association of Internet Researchers. (2020). Internet research: Ethical guidelines 3.0. https://aoir.org/reports/ethics3.pdf
Laurer, M., van Atteveldt, W., Casas, A., & Welbers, K. (2024). Less annotating, more classifying: Addressing the data scarcity issue of supervised machine learning with deep transfer learning and BERT-NLI. Political Analysis, 32(1), 84–100.
Related
Artículos científicos: Agent Skills for writing and reviewing scientific articles in Spanish.
License
MIT
