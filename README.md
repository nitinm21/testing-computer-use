# Anthropic Computer Use Demo

[Anthropic Computer Use](https://github.com/anthropics/anthropic-quickstarts/blob/main/computer-use-demo/README.md) is a beta Anthropic feature which runs a Docker image with Ubuntu and controls it. This fork allows you to run it natively on macOS, providing direct system control through native macOS commands and utilities.

> [!CAUTION]
> This comes with obvious risks. The Anthropic agent can control everything on your Mac. Please be careful.
> Anthropic's new Claude 3.5 Sonnet model refuses to do unsafe things like purchase items or download illegal content.

## Prerequisites

- macOS Sonoma 15.7 or later
- Python 3.12+
- Homebrew (for installing additional dependencies)
- cliclick (`brew install cliclick`) - Required for mouse and keyboard control

## Setup Instructions

1. Clone the repository and navigate to it:

```bash
git clone https://github.com/nitinm21/testing-computer-use.git
cd testing-computer-use
```

2. Create and activate a virtual environment:

```bash
python3.12 -m venv venv
source venv/bin/activate
```

3. Run the setup script:

```bash
chmod +x setup.sh
./setup.sh
```

4. Install Python requirements:

```bash
pip install -r requirements.txt
```

## Running the Demo

### Set up your environment and Anthropic API key

1. In a `.env` file add:

```
API_PROVIDER=anthropic
ANTHROPIC_API_KEY=<key>
WIDTH=800
HEIGHT=600
DISPLAY_NUM=1
```

Set the screen dimensions (recommended: stay within XGA/WXGA resolution), and put in your key from [Anthropic Console](https://console.anthropic.com/settings/keys).

2. Start the Streamlit app:

```bash
streamlit run streamlit.py
```
