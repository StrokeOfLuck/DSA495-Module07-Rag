# DSA 495 — Module07: RAG with Phi-4-mini

Sean Ryan's copy of Serena Kim's [Module07 course materials](https://github.com/SerenaYKim/DSA495-TextAnalysis/tree/master/Module07), adapted to load its knowledge base directly from GitHub.

## Interactive document explorer

**[Open the Module07 HTML page](https://htmlpreview.github.io/?https://github.com/StrokeOfLuck/DSA495-Module07-Rag/blob/main/index.html)** · [HTML source](index.html)

Type any question, inspect verbatim retrieved passages, and open their exact source context. The page follows Sean's portfolio style and includes notebook activity notes, editable prompts, citation checks, and a notes download.

Browser retrieval uses BM25. Run Phi-4-mini in the linked Colab notebook for generated answers and MiniLM semantic retrieval. The source text is embedded for offline search; external links need internet access. Rebuild the embedded text when repository data changes.

## Open the notebook

**[Run in Google Colab](https://colab.research.google.com/github/StrokeOfLuck/DSA495-Module07-Rag/blob/main/Module07/DSA495-M07-RAG-Phi4.ipynb)** · [View on GitHub](Module07/DSA495-M07-RAG-Phi4.ipynb)

Use a **T4 GPU** and run cells from top to bottom. No Google Drive mounting, path editing, or Hugging Face token is required by the course notebook. TXT files download automatically before model loading.

If you already have a Colab copy open, reopen the link above to get the updated version.

## Included data

| File | Source |
| --- | --- |
| [DOE_Wind_Energy_FAQ.txt](data/knowledgebase/DOE_Wind_Energy_FAQ.txt) | [DOE: Wind Energy FAQ](https://www.energy.gov/cmei/systems/frequently-asked-questions-about-wind-energy) |
| [EPA_End_of_Life_Solar_Panels.txt](data/knowledgebase/EPA_End_of_Life_Solar_Panels.txt) | [EPA: End-of-Life Solar Panels](https://www.epa.gov/hw/end-life-solar-panels-regulations-and-management) |

These are your supplied TXT files, preserved unchanged. [Data manifest and file hashes](data/manifest.json).

**The original Columbia TXT file is not included yet.** The instructor's complete collection contains three documents; this copy currently uses the two supplied DOE/EPA files. It runs with those two and starts with a wind-wildlife question. Some questions, including the original cloudy-day solar example, may lack sufficient evidence.

Add the original Columbia course TXT file to [data/knowledgebase/](data/knowledgebase/) and rerun the notebook to include it automatically. The Columbia [source report page](https://scholarship.law.columbia.edu/sabin_climate_change/281/) is a reference link, not the course TXT snapshot.

## Workflow

GitHub TXT files → document table → chunks → MiniLM embeddings → retrieved passages → Phi-4-mini prompt → cited answer.

The original chunking, embedding, retrieval, generation, and optional plotting code is retained. This adaptation replaces Drive loading with GitHub downloads, moves the data check before model loading, and starts with a question suited to the supplied evidence.

## Course links and readings

- [Course home](https://courseweb.site/dsa495-2026/)
- [Module07 readings](https://courseweb.site/dsa495-2026/materials.html#07)
- [Course schedule](https://courseweb.site/dsa495-2026/schedule.html)
- [Original Module07 course data folder](https://drive.google.com/drive/folders/1xcAec1cOwCR-eBxsSlm_RVS46zjgowS1)
- [Microsoft Learn: Understand RAG](https://learn.microsoft.com/en-us/training/modules/rag-fundamentals/2-understand-rag)
- [Microsoft Learn: Prepare data for retrieval](https://learn.microsoft.com/en-us/training/modules/rag-fundamentals/3-prepare-data)
- [Microsoft Learn: Retrieve information and generate a response](https://learn.microsoft.com/en-us/training/modules/rag-fundamentals/4-retrieve-generate)
- [Phi-4-mini model](https://huggingface.co/microsoft/Phi-4-mini-instruct)
- [MiniLM embedding model](https://huggingface.co/sentence-transformers/all-MiniLM-L6-v2)
- [Hands-On Large Language Models: Chapter 8 companion](https://github.com/HandsOnLLM/Hands-On-Large-Language-Models/blob/main/chapter08/Chapter%208%20-%20Semantic%20Search.ipynb)
- [Module08 repo](https://github.com/StrokeOfLuck/DSA495-Module08-Rag)

## Attribution

Adapted from [SerenaYKim/DSA495-TextAnalysis](https://github.com/SerenaYKim/DSA495-TextAnalysis) at commit [18c6786](https://github.com/SerenaYKim/DSA495-TextAnalysis/commit/18c6786334f77f7fe01c539264d04a6d72f2dbae) on October 5, 2026. The [original instructor README](references/Module07-original-README.md) is retained for reference; use this README's GitHub-loading instructions for this copy.
