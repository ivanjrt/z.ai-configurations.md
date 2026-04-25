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

```json
{
  "env": {
    "ANTHROPIC_AUTH_TOKEN": "596bd8769b424110a3279879ff7c1a34.rALZVb1z9Wo0rei8",
    "ANTHROPIC_BASE_URL": "https://api.z.ai/api/anthropic",
    "API_TIMEOUT_MS": "3000000",
    "CLAUDE_CODE_DISABLE_NONESSENTIAL_TRAFFIC": 1,
    "ANTHROPIC_DEFAULT_HAIKU_MODEL": "glm-5.1",
    "ANTHROPIC_DEFAULT_SONNET_MODEL": "glm-5.1",
    "ANTHROPIC_DEFAULT_HAIKU_MODEL": "glm-5.1"
  }
}
```
# Troubleshooting:

if for some reason `claude` is not able to launch from anywhere in the network then:

```
echo 'export PATH="$HOME/.local/bin:$PATH"' >> ~/.bashrc && source ~/.bashrc
```
