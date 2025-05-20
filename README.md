from together import Together

client = Together()

response = client.chat.completions.create(
    model="deepseek-ai/DeepSeek-V3",
    messages=[],
    stream=True
)
for token in response:
    if hasattr(token, 'choices'):
        print(token.choices[0].delta.content, end='', flush=True)
        curl -X POST "https://api.together.xyz/v1/chat/completions" \
  -H "Authorization: Bearer $TOGETHER_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "deepseek-ai/DeepSeek-V3",
    "messages": [],
    "stream": true
  }'https://api.together.xyz/v1/chat/completions
  text}'chunk.choices
  
