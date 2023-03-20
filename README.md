# Japanese-Alpaca-LoRA
A japanese finetuned instruction LLaMA.

In accordance with other models being referenced, this model is not available for commercial use and can only be used for research purposes.

## References
This project is based on [LLaMA](https://ai.facebook.com/blog/large-language-model-llama-meta-ai/), [Stanford Alpaca](https://github.com/tatsu-lab/stanford_alpaca), [Alpaca LoRA](https://github.com/tloen/alpaca-lora), [cabrita](https://github.com/22-hours/cabrita)

## Data
We translated the [alpaca_data.json](https://github.com/tatsu-lab/stanford_alpaca/blob/main/alpaca_data.json) to japanese using ChatGPT API.
We paid around US $45 to translate the full dataset to japanese. Translated data is available. ([japanese_alpaca_data.json](data/japanese_alpaca_data.json))

## Finetuning
We just followed [Alpaca Lora](https://github.com/tloen/alpaca-lora). We could run finetuning step using Google Colab PRO+. It took 6.5 hours for finetuning.

## Example outputs
### Good Examples
```
Input: 日本の首都はどこですか？
Alpaca-LoRA-Output: The capital of Japan is Tokyo.
Japanese-Alpaca-LoRA-Output: 「日本の首都は東京です。」
```

```
Input: 高齢の方が罹りやすい病気を3つ挙げてください。
Alpaca-LoRA-Output: Three diseases that are more common in the elderly are heart disease, stroke, and dementia.
Japanese-Alpaca-LoRA-Output:「高齢の方が罹りやすい病気には、心臓疾患、精神疾患、そして呼吸器疾患が含まれます。」
```

### Bad Examples
```
Input: 大阪のオススメの食べ物を教えて
Alpaca-LoRA-Output: Osaka's favorite foods include takoyaki, okonomiyaki, kushikatsu, and yakitori.
Japanese-Alpaca-LoRA-Output:「大阪のオススメの食べ物には、オーストラリアの牛肉フルーツバター、オーストラリアの牛肉フルーツバター、オーストラリアの牛肉フルーツバター、
```

```
Input: 「3x + 2= 20」という方程式を解くとxはいくつになりますか
Alpaca-LoRA-Output:  x = 6
Japanese-Alpaca-LoRA-Output:「3x + 2 = 20」という方程式を解くと、xは2です。」
```
