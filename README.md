# Arjun-Kapoor-Langsmith-MAT496
Langsmith Course Assignment for MAT496

### Lesson 1

Learned: Gained hands-on experience instrumenting Python functions with the @traceable decorator to build a hierarchical run tree. This approach is key for tracking custom logic and achieving end-to-end observability in a Groq-powered RAG pipeline using LangSmith.

Tweak: Enhanced the tracing setup by assigning meaningful names and attaching contextual metadata to the core RAG functions, resulting in richer and more informative trace logs.

### Lesson 2

Learned: Understood how to properly categorize traces using the run_type parameter (such as llm and retriever) to unlock specialized visualizations in LangSmith, along with implementing reduce_fn to handle streamed outputs effectively.

Tweak: Filled in all missing run_type and reduce_fn configurations, updated the LLM prompt to a coffee-order scenario, and tailored the retriever’s document content and metadata to make the example distinct and customized.

### Lesson 3

Learned: Gained insight into using the with trace() context manager to explicitly manage trace inputs and outputs, and learned that LangChain-compatible providers can enable automatic tracing for all LLM calls through environment variable configuration.

Tweak: Replaced the decorator on generate_response with a custom with trace() block, attaching a distinctive manual-context-manager tag to demonstrate fine-grained, manual trace control.

### Lesson 4

Learned: Discovered that multi-turn conversations are linked by supplying a stable, unique identifier (such as session_id, thread_id, or conversation_id) through the langsmith_extra metadata across related runs.

Tweak: Added conversation tracking by generating a uuid.uuid4() in Python and reusing it as the conversation_id within the langsmith_extra field for both chat turns.

## Module 2

### Lesson 1

Learned: Learned to manage LangSmith datasets programmatically with the langsmith.Client to support a test-driven workflow, including creating datasets via client.create_dataset() and bulk uploading input–reference pairs using client.create_examples().

Tweak: Switched from relying on a pre-existing dataset ID to dynamically creating a new dataset through client.create_dataset(), generating a unique name with uuid.uuid4(). This allowed the full dataset setup and example ingestion to run end-to-end directly within the notebook.