# Prompt Engineering Lab

The **Prompt Engineering Lab** serves as an Education and Experimentation Hub provided by the **Generative Intelligence Lab @ FAU**.

Prompt Engineering is a rapidly evolving discipline at the intersection of Artificial Intelligence (AI) and Natural Language Processing (NLP). This lab is designed to help **students**, **researchers**, and **developers** experiment with the art of creating and refining prompts, offering easy-to-follow resources and opportunities to contribute, collaborate, and share their work.

Prompt Engineering has emerged as a critical component for unlocking the full potential of language models such as **Phi**, **LLaMA**, and **Qwen**. As AI systems continue to revolutionize problem-solving, mastering the art of effective prompting is essential for:

- Cutting-edge research
- Practical applications
- Future innovations

The lab provides a **hands-on learning environment** where participants can actively apply their knowledge through **Python code**, **Jupyter notebooks**, and **practical exercises** to foster both **experimentation** and **discovery**.

---

## 🛠️ Configure Your Lab Environment

Before experimenting, first configure your environment:

- [Configure Lab Environment for General Audience](CONFIG.md)
- [Configure Lab Environment for FAU Students](CONFIG-FAU.md)
- [Troubleshooting Guide](https://github.com/genilab-fau/prompt-eng/blob/cb2fefa33f5a1c5a927f1246917f73943d3b99ce/TROUBLESHOOTING.md)

---

## ✨ Prompt Engineering Techniques

Explore the following techniques provided as interactive Jupyter Notebooks:

- [Zero-Shot Prompting](prompt-eng/zero_shot.ipynb)
- [Few-Shot Prompting](prompt-eng/few_shots.ipynb)
- [Prompt Templates](prompt-eng/prompt_template.ipynb)
- [Chain-of-Thought](prompt-eng/chain_of_thought.ipynb)
- [Meta Prompting](prompt-eng/meta.ipynb)
- [Self-Consistency](prompt-eng/self_consistency.ipynb)

> *(More techniques are coming soon! See [Contributing Guidelines](https://github.com/genilab-fau/prompt-eng/blob/cb2fefa33f5a1c5a927f1246917f73943d3b99ce/CONTRIBUTING.md) to contribute.)*

---

## 🧪 How to Experiment

Once you complete your environment setup, you can:

### 1. Adjust the inbound message

Simulate inbound user requests:

```python
MESSAGE = "What is 2 * log(10)?"
```

### 2. Apply Prompt Engineering Templates

Modify how prompts are structured:

```python
TEMPLATE_BEFORE = "Act like you are a math teacher\nYour student is asking:"
TEMPLATE_AFTER = "Give only the answer; refrain from any more information"

PROMPT = TEMPLATE_BEFORE + '\n' + MESSAGE + '\n' + TEMPLATE_AFTER
```

### 3. Configure the Model Request

Simulate orchestration by setting model parameters:

```python
payload = create_payload(
    target="ollama",
    model="llama3.2:latest",
    prompt=PROMPT,
    temperature=1.0,
    num_ctx=100,
    num_predict=100
)
```

👉 Documentation about available parameters: [Ollama API Docs](https://github.com/ollama/ollama/blob/main/docs/api.md)

---

## 📚 References

- [Meta — Prompting Guide](https://www.llama.com/docs/how-to-guides/prompting/)
- [OpenAI — Prompt Engineering Guide](https://platform.openai.com/docs/guides/prompt-engineering)
- [Ollama API Documentation](https://github.com/ollama/ollama/blob/main/docs/api.md)
- [Open WebUI API Endpoints](https://docs.openwebui.com/getting-started/api-endpoints/)

---

# ⚡ GenAI — Powered by Generative Intelligence Lab @ FAU
