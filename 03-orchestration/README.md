# Configure API Keys in Kestra

```bash
export GEMINI_API_KEY="your-gemini-api-key-here" 
export SECRET_GEMINI_API_KEY=$(echo -n $GEMINI_API_KEY | base64) 
export SECRET_OPENAI_API_KEY=$(echo -n "your-openai-api-key-here" | base64) 
export SECRET_TAVILY_API_KEY=$(echo -n "your-tavily-api-key-here" | base64)   

Q1. After trying the same prompt in ChatGPT vs Kestra AI Copilot, what is the primary reason AI Copilot generates better Kestra flows? (1 point)
    - AI Copilot has access to current Kestra plugin documentation

Q2. The non-RAG response about Kestra 1.1 features is best described as: (1 point)
    - Vague, generic, or fabricated — the model guesses from training data

Q3. What is the approximate output token count for multilingual_agent when running with summary_length = short? (1 point)
    - 60-100 tokens

Q4. With summary_length = long, roughly how many times more output tokens does multilingual_agent use compared to the short summary? (1 point)
    - 2-5x more

Q5. After changing english_brevity to ask for 3 sentences instead of 1, how does the output token count compare to the original 1-sentence version? (1 point)
    - About the same (within 20%)

Q6. For production workflows requiring deterministic, repeatable results with strict compliance requirements, which approach is most appropriate? (1 point)
    - Use traditional task-based workflows for predictability and auditability
