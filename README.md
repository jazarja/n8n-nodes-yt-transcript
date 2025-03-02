# YouTube Transcript Node for n8n

This custom node for n8n retrieves the transcript of a YouTube video using its video ID. It leverages the functionality provided by the `youtube-transcription` library and is designed to replace the deprecated **n8n-nodes-youtube-transcription**.

## Disclaimers

This project is **intended for local use only** and should be used for **testing, learning, or educational purposes**. By utilizing this node, you accept full responsibility for any risks or issues that may arise, and the author will not be held liable for any outcomes, damages, or legal consequences.

Ensure that your use of this project adheres to all applicable laws, regulations, and platform guidelines, including YouTube's Terms of Service and Community Guidelines. Please use responsibly and ethically.

## Features
- Retrieves YouTube video transcripts.
- Outputs the transcript in a structured JSON format, containing the offset, duration, language, and text.
- Error handling included with an option to continue processing even on failure.

## Installation

To install the node in your n8n instance:

1. Open your n8n project
2. Go to **Settings** > **Community Nodes**
3. Search for the custom node repository and install it
4. Restart n8n if necessary

For manual installation:
```bash
npm install n8n-nodes-yt-transcript
```

Alternatively, you can clone the repository to your n8n custom nodes folder and build the project manually.

## Node Parameters
- **Video ID**: The ID of the YouTube video for which you want to fetch the transcript. This parameter is required.

## Example Usage

1. Add the **YouTube Transcript** node to your n8n workflow.
2. Provide the `Video ID` parameter with the ID of the YouTube video you want to process.
3. Run the workflow.

### Example Output
Here's an example of the JSON output:

```json
{
  "youtubeId": "dQw4w9WgXcQ",
  "transcript": [
    {
      "text": "Never gonna give you up",
      "duration": 3.14,
      "offset": 0.0,
      "lang": "en"
    },
    {
      "text": "Never gonna let you down",
      "duration": 2.89,
      "offset": 3.14,
      "lang": "en"
    },
    {
      "text": "Never gonna run around and desert you",
      "duration": 4.21,
      "offset": 6.03,
      "lang": "en"
    }
  ]
}
```

## Acknowledgments
This node code based on  n8n-nodes-youtube-transcription library created by Leonardo Grigorio Araujo (https://github.com/leonardogrig).

