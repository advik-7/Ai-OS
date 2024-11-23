# Ai/OS: AI-Driven Operating System Control Agent  

**Ai/OS** is an advanced multi-agent system designed to streamline operating system control and task automation through a multi-layer hierarchical structure of agents. Built using **LangGraph**, Ai/OS introduces an intelligent delegation workflow where tasks are distributed and resolved efficiently by specialized sub-agents, allowing for high levels of automation and coordination.

---

## Features  

- **Multi-Layer Hierarchical Structure**  
  - A three-layer tree-like architecture:
    - **Main Agent**: Centralized task allocator and coordinator.
    - **Sub-Agents**: Specialized agents that solve tasks using pre-defined tools.
    - **Lower-Level Nodes**: Sub-agents that can communicate for task dependencies, allowing them to complete simultaneous Agent call widout having to report to the parent node every time .This can enhance the efficiency of decision-making at the lower level since agents can quickly exchange data locally.

    - **localized inter-node communication**: The connected lower-level nodes can directly coordinate task execution among themselves without frequently reporting back to the parent node.Dependent tasks can proceed without waiting for hierarchical instructions, this reduces latency and speeds up the overall process.

- **Input Versatility**  
  - Supports **audio** or **text** inputs.
  - Audio inputs are transcribed into text before processing.

- **Task Automation**  
  - Main agent dynamically allocates tasks based on input requirements.
  - Sub-agents execute tasks and report back seamlessly.

- **Inter-Agent Communication**  
  - Lower-level sub-agents can collaborate and share information for complex workflows.
  - Results from sub-agents are aggregated at higher levels.

- **Scalable and Modular**  
  - The hierarchical structure supports adding more agents and tools to expand functionality.
  - Easily customizable workflows to fit different use cases.

---

## System Architecture  

### 1. Three-Layer Tree Structure  
- **Layer 1 (Main Agent)**:  
  - Receives user input.
  - Allocates tasks to the relevant sub-agents.
  - Aggregates responses from sub-agents.

- **Layer 2 (Sub-Agents)**:  
  - Specialized for specific domains or functionalities (e.g., file management, system monitoring, network operations).
  - Use pre-defined tools to solve allocated tasks.

- **Layer 3 (Lower-Level Nodes)**:  
  - Work on highly specialized subtasks.
  - Can collaborate with other nodes on the same level for interdependent tasks.

### 2. Input Flow  
- **User Input**:  
  - Audio: Transcribed into text via an integrated transcription module.
  - Text: Directly fed to the Main Agent.

- **Task Delegation**:  
  - Main Agent analyzes the input and delegates tasks to sub-agents.

- **Task Resolution**:  
  - Sub-agents resolve their tasks using tools and communicate results.

---
