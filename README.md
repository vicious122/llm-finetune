# llm-finetune

OpenAI fine-tuning job lifecycle in a single C++ header.

## Features
- Build and upload JSONL training data
- Create, poll, and cancel fine-tune jobs
- List fine-tuned models and delete them
- Single-header, C++17, namespace `llm`

## Quick Start
```cpp
#define LLM_FINETUNE_IMPLEMENTATION
#include "llm_finetune.hpp"

std::vector<llm::TrainingExample> examples = { ... };
auto upload = llm::upload_examples(examples, api_key);
llm::FinetuneConfig cfg{ .api_key = api_key };
auto job = llm::create_job(upload.file_id, cfg);
auto final = llm::wait_for_completion(job.id, api_key, 30, [](auto& j){ ... });
```

## API
```cpp
void             write_training_jsonl(const std::vector<TrainingExample>&, const std::string& path);
UploadResult     upload_training_file(const std::string& path, const std::string& api_key);
UploadResult     upload_examples(const std::vector<TrainingExample>&, const std::string& api_key);
FinetuneJob      create_job(const std::string& file_id, const FinetuneConfig&);
FinetuneJob      get_job(const std::string& job_id, const std::string& api_key);
FinetuneJob      cancel_job(const std::string& job_id, const std::string& api_key);
std::vector<FinetuneJob> list_jobs(const std::string& api_key, int limit = 20);
FinetuneJob      wait_for_completion(const std::string& job_id, const std::string& api_key, int interval_s, std::function<void(const FinetuneJob&)>);
std::vector<FinetunedModel> list_models(const std::string& api_key);
void             delete_model(const std::string& model_id, const std::string& api_key);
```

## License
MIT — Mattbusel, 2026

## See Also

| Repo | Purpose |
|------|---------|
| [llm-stream](https://github.com/Mattbusel/llm-stream) | SSE streaming |
| [llm-cache](https://github.com/Mattbusel/llm-cache) | Response caching |
| [llm-cost](https://github.com/Mattbusel/llm-cost) | Token cost estimation |
| [llm-retry](https://github.com/Mattbusel/llm-retry) | Retry + circuit breaker |
| [llm-format](https://github.com/Mattbusel/llm-format) | Markdown/code formatting |
| [llm-embed](https://github.com/Mattbusel/llm-embed) | Embeddings + cosine similarity |
| [llm-pool](https://github.com/Mattbusel/llm-pool) | Connection pooling |
| [llm-log](https://github.com/Mattbusel/llm-log) | Structured logging |
| [llm-template](https://github.com/Mattbusel/llm-template) | Prompt templates |
| [llm-agent](https://github.com/Mattbusel/llm-agent) | Tool-use agent loop |
| [llm-rag](https://github.com/Mattbusel/llm-rag) | Retrieval-augmented generation |
| [llm-eval](https://github.com/Mattbusel/llm-eval) | Output evaluation |
| [llm-chat](https://github.com/Mattbusel/llm-chat) | Multi-turn chat |
| [llm-vision](https://github.com/Mattbusel/llm-vision) | Vision/image inputs |
| [llm-mock](https://github.com/Mattbusel/llm-mock) | Mock LLM for testing |
| [llm-router](https://github.com/Mattbusel/llm-router) | Model routing |
| [llm-guard](https://github.com/Mattbusel/llm-guard) | Content moderation |
| [llm-compress](https://github.com/Mattbusel/llm-compress) | Prompt compression |
| [llm-batch](https://github.com/Mattbusel/llm-batch) | Batch processing |
| [llm-audio](https://github.com/Mattbusel/llm-audio) | Audio transcription/TTS |
| [llm-finetune](https://github.com/Mattbusel/llm-finetune) | Fine-tuning jobs |
| [llm-rank](https://github.com/Mattbusel/llm-rank) | Passage reranking |
| [llm-parse](https://github.com/Mattbusel/llm-parse) | HTML/markdown parsing |
| [llm-trace](https://github.com/Mattbusel/llm-trace) | Distributed tracing |
| [llm-ab](https://github.com/Mattbusel/llm-ab) | A/B testing |
| [llm-json](https://github.com/Mattbusel/llm-json) | JSON parsing/building |
