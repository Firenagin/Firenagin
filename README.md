- 👋 Hi, I’m @Firenagin
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
Firenagin/Firenagin is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
import json
import requests
API_URL = "https://api-inference.modelscope.cn/api-inference/v1/models/damo/spring_couplet_generation"
# 请用自己的SDK令牌替换{YOUR_MODELSCOPE_SDK_TOKEN}（包括大括号）
headers = {"Authorization": f"Bearer {YOUR_MODELSCOPE_SDK_TOKEN}"}
def query(payload):
    data = json.dumps(payload)
    response = requests.request("POST", API_URL, headers=headers, data=data)
    return json.loads(response.content.decode("utf-8"))
payload = {"input": "以关键词“幸福”写一副春联"}
output = query(payload) 
