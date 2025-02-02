gpt4o の使い方は以下の通りです。

```
from openai import OpenAI

client = OpenAI()

completion = client.chat.completions.create(
    model="gpt-4o",
    messages=[
        {
            "role": "user",
            "content": [
                {"type": "text", "text": "What's in this image?"},
                {
                    "type": "image_url",
                    "image_url": {
                        "url": "data:image/png;base64,（base64でエンコードした画像）",
                    }
                },
            ],
        }
    ],
)

print(completion.choices[0].message)
```
