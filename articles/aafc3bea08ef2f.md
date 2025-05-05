---
title: "Kaggle tips まとめ"
emoji: "🤖"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: ["Kaggle"]
published: false
---
# Kaggle Notebook
## Commitした時に、log messageにprintの出力を表示するには
```py
import os
__print__ = print
def print(string):
    os.system(f'echo \"{string}\"')
    __print__(string)
```
https://www.kaggle.com/discussions/product-feedback/69865

## datasetのダウンロードの自動化
```py
#https://github.com/Kaggle/kagglehub
import kagglehub
from kagglehub.config import get_kaggle_credentials
!mkdir ~/.kaggle
!cp /kaggle/input/kaggle-json/kaggle.json ~/.kaggle/
```