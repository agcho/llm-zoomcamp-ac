## Configure API Keys in Kestra

Before running the Kestra flows, configure the required API keys.

```bash
export GEMINI_API_KEY="your-gemini-api-key-here"
export SECRET_GEMINI_API_KEY=$(echo -n "$GEMINI_API_KEY" | base64)

export SECRET_OPENAI_API_KEY=$(echo -n "your-openai-api-key-here" | base64)
export SECRET_TAVILY_API_KEY=$(echo -n "your-tavily-api-key-here" | base64)
```

After setting the API keys, restart Kestra:

```bash
docker compose down
docker compose up -d
```

## Homework Answers

### Q1. Context Engineering

**Question:** After trying the same prompt in ChatGPT vs Kestra AI Copilot, what is the primary reason AI Copilot generates better Kestra flows?

**Answer:** AI Copilot has access to current Kestra plugin documentation.

---

### Q2. RAG vs No RAG

**Question:** The non-RAG response about Kestra 1.1 features is best described as:

**Answer:** Vague, generic, or fabricated — the model guesses from training data.

---

### Q3. Token usage — short summary

**Question:** What is the approximate output token count for `multilingual_agent` when running with `summary_length = short`?

**Answer:** 60–100 tokens.

---

### Q4. Token usage — long summary

**Question:** With `summary_length = long`, roughly how many times more output tokens does `multilingual_agent` use compared to the short summary?

**Answer:** 2–5x more.

---

### Q5. Modifying a flow

**Question:** After changing `english_brevity` to ask for 3 sentences instead of 1, how does the output token count compare to the original 1-sentence version?

**Answer:** About the same, within 20%.

---

### Q6. Best Practices

**Question:** For production workflows requiring deterministic, repeatable results with strict compliance requirements, which approach is most appropriate?

**Answer:** Use traditional task-based workflows for predictability and auditability.
