# Slack Channel Summarizer with Gemini API

## Description

This project provides a solution to fetch and analyze messages from a Slack channel and summarize them using the Gemini 1.5 Pro API. It allows users to generate detailed summaries of Slack conversations, focusing on topics like incident timelines, mitigation steps, resolution details, and identified action items. Users can also specify custom questions to get tailored insights from the conversation.

I chose Gemini 1.5 Pro due to its ability to handle long context windows, which makes it especially suitable for analyzing extensive Slack conversations. This is particularly useful for dedicated Slack channels created to discuss incidents, such as those managed through tools like Rootly.

## Features

- Fetches message history from any Slack channel using the Slack API.
- Integrates with the Gemini 1.5 Pro API for natural language understanding and summarization.
- Supports user-defined questions or generates a default summary.
- Handles Slack API pagination for channels and messages.

## Prerequisites

- Python 3.8+
- Slack API token with appropriate permissions.
- Gemini 1.5 Pro API key.

## Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd slack-gemini-summary
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Create a `.env` file in the project root directory and add the following environment variables:
   ```env
   SLACK_API=<your-slack-api-token>
   GEMINI_API_KEY=<your-gemini-api-key>
   ```

## Usage

1. Run the script:
   ```bash
   python main.py
   ```

2. Enter the Slack channel name when prompted.

3. Provide a custom question or press Enter to use the default prompt.

4. The script will fetch the channel's conversation history and send it to the Gemini API for summarization or question answering.

## Example Output

- **Default Summary Prompt:**
  - "Create a detailed summary of what was discussed in this channel, including incident timelines, mitigation steps, resolution details, and identified action items."

- **Custom Question Example:**
  - "What were the main action items identified in the conversation?"

## Limitations

- Requires valid Slack API token and permissions to access the target channel.
- Only processes textual messages; attachments and images are ignored.
- Limited by the character limits and capabilities of the Gemini API.

## License

This project is licensed under the MIT License. See the LICENSE file for details.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request with your changes.

## Contact

For questions or support, please open an issue on GitHub or contact the repository owner.

