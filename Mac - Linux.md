Install Claude code witht this:
```bash
curl -O "https://cdn.bigmodel.cn/install/claude_code_zai_env.sh" && bash ./claude_code_zai_env.sh
```
it will prompt for the `Z.AI` key.

Edit this file 
```bash
nano ~/.claude/settings.json
```
and make sure it has this info below, don't forget the commas `,`

```
{
  "env": {
    "ANTHROPIC_AUTH_TOKEN": "CHANGE-THIS-TO-YOURS",
    "ANTHROPIC_BASE_URL": "https://api.z.ai/api/anthropic",
    "API_TIMEOUT_MS": "3000000",
    "CLAUDE_CODE_DISABLE_NONESSENTIAL_TRAFFIC": 1,
    "ANTHROPIC_DEFAULT_HAIKU_MODEL": "glm-5.1-air",
    "ANTHROPIC_DEFAULT_SONNET_MODEL": "glm-5.1",
  }
}
```
