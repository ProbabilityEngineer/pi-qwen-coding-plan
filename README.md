# Pi-Mono-Alibaba
Configuration files for Pi-Mono (json) and Oh-My-Pi (yaml) to use Alibaba's coding plan.

## Installation
If using pi-mono, place models.json in ~/.pi/agent , if using oh-my-pi place models.yml in ~/.omp/agent

## Models
qwen3-max-2026-01-23
qwen3.5-plus
qwen3-coder-next
glm-4.7
kimi-k2.5
I removed Qwen3-Coder-Plus as it's outdated and ridiculously expensive ($60 if you blow past 256k context to 1m tokens).

## Model Speed
I see ~215 tokens per second with qwen-coder-next, making iteration amazing.
I see ~100 tps with qwen3.5 plus.
I've not yet measured Max.
GLM 4.7 seems pretty snappy.
I've not spent much time with Kimi k2.5.

## Model Features
All models seem to respond to reasoning levels. (Thanks to dyzhdyzh for the tip).
Coder Next and Max are text only, 256k context window. Max is the daddy, but eats up your allowance.
3.5 plus is vision-language, and has a 1m context window thanks to its hybrid attention mechanism.
Pricing and Caching numbers are inferred from Alibaba docs.

## Usage limit ratio assumptions (Price)
I filled the price and caching price fields in from Alibaba's docs on api-calling price, so when I say one model costs more than another, that's an assumotion. Alibaba's coding plan is metered by requests and seems rather generous.

### Price high to low
Qwen3-Max (significantly)
Qwen3-Next
Qwen3.5-Plus, GLM-4.7, Kimi-K2.5

## Enormous thanks to:
Mario Zechner's Pi-Mono
https://github.com/badlogic/pi-mono

Can Bölük's Oh-My-Pi
https://github.com/can1357/oh-my-pi
