
<h1 align="center" style="border-bottom: none">
    <a href="https://intuixai.org/">
        <img alt="IntuixAI logo" src="./assets/logo.svg" width="200" />
    </a>
</h1>
<h2 align="center" style="border-bottom: none">
Open-Source Platform for Productionizing AI
</h2>

IntuixAI is an open-source developer platform to build AI/LLM applications and models with confidence. Enhance your AI applications with end-to-end **experiment tracking**, **observability**, and **evaluations**, all in one integrated platform.

## 🚀 Installation

To install the IntuixAI Python package, run the following command:

```bash
pip install intuixai
````

---

## 📦 Core Components

IntuixAI provides a unified solution for modern AI/ML workflows, including LLMs, Agents, Deep Learning, and traditional machine learning.

### 💡 For LLM / GenAI Developers

<table>
  <tr>
    <td>
    <img src="./assets/readme-tracing.png" alt="Tracing" width=100%>
    <div align="center">
        <br>
        <a href="https://intuixai.org/docs/llms/tracing"><strong>🔍 Tracing / Observability</strong></a>
        <br><br>
        <div>
        Trace the internal states of your LLM/agentic applications for debugging quality issues and monitoring performance with ease.
        </div><br>
        <a href="https://intuixai.org/docs/llms/tracing/quickstart">Getting Started →</a>
        <br><br>
    </div>
    </td>
    <td>
    <img src="./assets/readme-llm-eval.png" alt="LLM Evaluation" width=100%>
    <div align="center">
        <br>
        <a href="https://intuixai.org/docs/genai/eval-monitor"><strong>📊 LLM Evaluation</strong></a>
        <br><br>
        <div>
        A suite of automated model evaluation tools, seamlessly integrated with experiment tracking to compare across multiple versions.
        </div><br>
        <a href="https://intuixai.org/docs/genai/eval-monitor">Getting Started →</a>
        <br><br>
    </div>
    </td>
  </tr>
</table>

---

### 🎓 For Data Scientists

<table>
  <tr>
    <td colspan="2" align="center">
      <img src="./assets/readme-experiment.png" alt="Tracking" width=50%>
    <div align="center">
        <br>
        <a href="https://intuixai.org/docs/ml/tracking"><strong>📝 Experiment Tracking</strong></a>
        <br><br>
        <div>
        Track your models, parameters, metrics, and evaluation results in ML experiments and compare them using an interactive UI.
        </div><br>
        <a href="https://intuixai.org/docs/ml/tracking/quickstart">Getting Started →</a>
        <br><br>
    </div>
    </td>
  </tr>
</table>

---

## 🌐 Hosting IntuixAI Anywhere

IntuixAI can run in many environments, including local machines, on-premise servers, and cloud infrastructure.

Trusted by organizations building production AI systems.

For hosting IntuixAI on your own infrastructure, refer to the deployment guide in the documentation.

---

## 🗣️ Supported Programming Languages

* Python
* TypeScript / JavaScript
* Java
* R

---

## 🔗 Integrations

IntuixAI integrates with many popular machine learning frameworks and GenAI libraries.

---

## Usage Examples

### Tracing (Observability)

```python
import mlflow as intuixai
from openai import OpenAI

# Enable tracing for OpenAI
intuixai.openai.autolog()

response = OpenAI().chat.completions.create(
    model="gpt-4o-mini",
    messages=[{"role": "user", "content": "Hi!"}],
    temperature=0.1,
)
```

Navigate to the "Traces" tab in the IntuixAI UI to find trace records.

---

### Tracking Model Training

```python
import intuixai
from sklearn.ensemble import RandomForestRegressor
from sklearn.model_selection import train_test_split
from sklearn.datasets import load_diabetes

intuixai.sklearn.autolog()

db = load_diabetes()
X_train, X_test, y_train, y_test = train_test_split(db.data, db.target)

rf = RandomForestRegressor(n_estimators=100)
rf.fit(X_train, y_train)
```

---

