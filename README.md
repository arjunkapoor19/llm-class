# Arjun-Kapoor-Langsmith-MAT496
Langsmith Course Assignment for MAT496

### Lesson 1

Learned: Gained hands-on experience instrumenting Python functions with the @traceable decorator to build a hierarchical run tree. This approach is key for tracking custom logic and achieving end-to-end observability in a Groq-powered RAG pipeline using LangSmith.

Tweak: Enhanced the tracing setup by assigning meaningful names and attaching contextual metadata to the core RAG functions, resulting in richer and more informative trace logs.

### Lesson 2

Learned: Understood how to properly categorize traces using the run_type parameter (such as llm and retriever) to unlock specialized visualizations in LangSmith, along with implementing reduce_fn to handle streamed outputs effectively.

Tweak: Filled in all missing run_type and reduce_fn configurations, updated the LLM prompt to a coffee-order scenario, and tailored the retriever’s document content and metadata to make the example distinct and customized.