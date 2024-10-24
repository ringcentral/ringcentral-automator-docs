# Action: transcribe media file

Given a media file that lives at an internet-accessible URL, generates a transcription and summary of the media file's contents. 

## Authentication with the media URL

The system being interfaced with to access a media file must allow all authentication to happen via the URL, as one cannot customize the HTTP headers and other low-level aspects of the connection. 

## Input

| Variable            | Type   | Description                                     |
|---------------------|--------|-------------------------------------------------|
| **Audio media URL** | URL    | A URL to a media file that contains audio.      |
| **Language**        | String | The language of spoken words in the media file. |

## Output

| Action Variable                 | Type   | Description                                     |
|---------------------------------|--------|-------------------------------------------------|
| **Transcript**                  | String | A full transcript of the referenced media file. |
| **Sentiment**                   | String | The overall sentiment of transcribed file. Values can be "postive," "negative," or "neutral." |
| **Abstractive summary (long)**  | String | A synthesized summary of the contents of the transcript, in long form. |
| **Abstractive summary (short)** | String | A shortened synthesized summary of the contents of the transcript. |
