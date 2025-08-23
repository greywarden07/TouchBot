# TouchBot

TouchBot is an agent-based automation framework for performing and documenting basic tasks on Android smartphones. It leverages visual and XML data to interact with UI elements, enabling autonomous task execution and documentation generation.

## Features

- **Autonomous Exploration**: Automatically explores app interfaces and generates documentation.
- **Human Demonstration**: Records user interactions and generates step-by-step documentation.
- **Visual & XML Input**: Uses screenshots and XML files to identify and label UI elements.
- **Supports Tap, Text, Long Press, Swipe**: Automates common UI actions.
- **Documentation Generation**: Creates concise descriptions for UI elements based on user actions.
- **Configurable**: Easily adjust API keys, model, and behavior via `config.yaml`.

## Architecture

![TouchBot High-Level Design](diagram(1).png)

## Getting Started

### Prerequisites

- Python 3.8+
- Android device with USB debugging enabled
- Required Python packages (see below)

### Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/TouchBot.git
    cd TouchBot
    ```

2. Install dependencies:
    ```sh
    pip install -r requirements.txt
    ```

3. Configure your API keys and settings in [`config.yaml`](config.yaml).

### Usage

#### Human Demonstration

```sh
python learn.py
```
- Choose "human demonstration" mode.
- Follow prompts to record your actions on the Android device.

#### Autonomous Exploration

```sh
python learn.py
```
- Choose "autonomous exploration" mode.
- The agent will explore the app and generate documentation automatically.

#### Documentation Generation

After recording a demo, generate documentation:
```sh
python scripts/document_generation.py --app <app_name> --demo <demo_name> --root_dir <root_dir>
```

### Configuration

Edit [`config.yaml`](config.yaml) to set API keys, model, directories, and other options.

### File Structure

- `learn.py`: Main entry point for running demos and exploration.
- `scripts/step_recorder.py`: Records user interactions.
- `scripts/document_generation.py`: Generates documentation from recorded steps.
- `scripts/prompts.py`: Contains prompt templates for documentation.
- `config.yaml`: Configuration file.
- `tasks/`: Stores recorded tasks and logs.

### Credits

Thanks to Chi Zhang, Zhao Yang, Jiaxuan Liu, Yucheng Han, Xin Chen, Zebiao Huang, Bin Fu, Gang Yu.

Original Repo: [AppAgent](https://github.com/mnotgod96/AppAgent)

Demo Video: [YouTube](https://www.youtube.com/watch?v=gxChJiF0fEA)

---

**Note:** For more details, refer to the source code and comments
