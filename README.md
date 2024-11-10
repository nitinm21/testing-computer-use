# Anthropic Computer Use Demo

Here's the official press release about [Anthropic Computer Use](https://www.anthropic.com/news/3-5-models-and-computer-use). 
Computer Use runs a Docker image with Ubuntu and controls it. It's a pretty cool feature that seems like the first step towards AI Agents that can control your computer.

## Setup Instructions

1. Clone the repository and navigate to it:

```bash
git clone https://github.com/nitinm21/testing-computer-use.git
cd testing-computer-use
```

2. Create and activate a virtual environment:

```bash
python -m venv venv
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
