# Lego Movie Trailers
Convert any YouTube movie trailer into a "Lego Cinematic Universe" version, using these simple steps. Can work with other styles, such as Studio Ghibli, etc.

### Step 1 - Extract Shot Data from Video
Once you have selected a Movie Trailer on YouTube, you can follow these steps to figure out how many shots there are, what time each shot starts, and get the necessary prompts to transform each shot into a Lego shot.
- Open Google AI Studio, and switch the model to Gemini 2.5 Pro Experimental 03-25
- Turn on "Structured Output" and paste in this JSON:
```json
{
  "type": "object",
  "properties": {
    "shots": {
      "type": "array",
      "items": {
        "type": "object",
        "properties": {
          "startTime": {
            "type": "string"
          },
          "duration": {
            "type": "string"
          },
          "description": {
            "type": "string"
          }
        },
        "required": [
          "startTime",
          "duration",
          "description"
        ]
      }
    }
  },
  "required": [
    "shots"
  ]
}
```
- Paste the YouTube video link into the prompt textbox, followed by this text prompt:
```
You are a 
```

### Step 2 - Review Shot Data
You now have
