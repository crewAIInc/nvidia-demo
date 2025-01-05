# Building Code Documentation Agents with CrewAI 🤖

[![Deploy Now](https://brev-assets.s3.us-west-1.amazonaws.com/nv-lb-dark.svg)](https://console.brev.dev/launchable/deploy?launchableID=env-2qNXgLMuzlJ8LS8Kl30EXbGwxSh)

A powerful system that leverages CrewAI Flows to automatically generate comprehensive documentation for any public GitHub repository. This project employs multiple specialized AI agents working collaboratively to produce high-quality, accurate documentation tailored to your codebase.

---

## Key Features

- **Multi-Agent Workflow**: Specialized agents collaborate to analyze and document your code.
- **Automated Documentation**: Full lifecycle coverage, from analysis to review.
- **NVIDIA NIM Integration**: Harnesses NVIDIA's llama-3.3-70b and NeMo Retriever E5 embedding models.
- **Mermaid Diagram Support**: Automatically generates architecture and flow diagrams.
- **Quality Assurance**: Ensures accuracy, consistency, and completeness with a built-in review process.

---

## Architecture

**The system employs a multi-agent workflow divided into two key stages:**

#### Ingestion Phase
- **WebsiteSearchTool:** This tool is used to embed and index mermaid examples from mermaid.js.org website using NVIDIA NeMo Retriever E5 embedding NIM.

#### Agent Flow
1. Codebase Analysis and Strategy Planning:
    - Analyze Codebase: Planner agents inspect the repository to map its structure, identify key components, and understand interdependencies.
    - Develop Strategy: They create a tailored documentation plan based on the analysis.
2. Documentation Creation and Review:
    - High-Level Documentation: One agent generates clear, comprehensive documentation introducing the project and its architecture.
    - Quality Assurance: Another agent ensures accuracy, consistency, and completeness across all documentation.
Here's an architecture diagram of the workflow:
![Architecture Diagram](https://raw.githubusercontent.com/crewAIInc/nvidia-demo/main/arch_diagram.png)

---

## Getting Started

### Prerequisites

1. Python 3.10+
2. NVIDIA API Key

### Installation

1. Clone this repository
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Set up your environment variables (see below).
3. Run the Jupyter notebook.
4. Generated documentation will be available in the `docs` directory.

### Setting up NVIDIA API Key

1. Visit [NVIDIA NIM](https://build.nvidia.com/nim).
2. Select the **llama-3.3-70b-instruct** model.
3. Retrieve your API key from the right panel.
4. Set your environment variables:
   ```bash
   export NVIDIA_NIM_API_KEY=your_api_key
   ```
   Alternatively, create a `.env` file in the project root:
   ```bash
   NVIDIA_NIM_API_KEY=your_api_key
   ```

---

## Documentation Outputs

The system generates multiple types of documentation, including:

- **Project Overview**
- **Architecture Documentation**
- **Component Documentation**
- **Integration Guides**
- **API Documentation**
- **Setup Instructions**

---

## Contributing

We welcome contributions! To get involved:

1. Fork the repository.
2. Create a feature branch:
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add feature X"
   ```
4. Push to your branch:
   ```bash
   git push origin feature/your-feature-name
   ```
5. Submit a Pull Request.

---

## License

This project is licensed under the MIT License.

Built with ❤️ using CrewAI and NVIDIA AI.

---

## About the NVIDIA Collaboration

Today, we are thrilled to announce a major collaboration with NVIDIA, fully integrating CrewAI with NVIDIA NIM microservices—part of the NVIDIA AI Enterprise software platform. This integration empowers developers to harness high-performance inference capabilities for the latest foundation models, enabling scalable and secure deployment of AI agents across various industries and workflows.

### Broader Vision

While this demo focuses on automating project documentation, the collaboration paves the way for unlocking the full potential of AI agents across industries. Our shared goal is to make AI agents more autonomous, accessible, and transformative for organizations worldwide.


