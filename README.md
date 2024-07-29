# Curation of Japanese Medical Data Sources for LLM development

## Available in Japanese

### 学習用データ
- 


### 評価用タスク：原則としてLLMの学習データに含めるべきではない！
- 日本医師国家試験(NMLE)
    - [厚生労働省](https://www.mhlw.go.jp/search.html?q=医師国家試験+問題&cx=005876357619168369638%3Aydrbkuj3fss&cof=FORID%3A9&ie=UTF-8&sa=)
        - 第100-118回. 
        - PDF形式.
    - [あかぎ国対](http://www.wind.ne.jp/hassii/akagi_kokutai/index.html)
        - 第104-106回
        - テキストファイル形式.
    - [IgakuQA](https://github.com/jungokasai/IgakuQA)
        - 第112-116回, 2018-2022. 日英対訳.
        - [Kasai et al.]()が作成.
    - [NMLE](https://huggingface.co/datasets/longisland3/NMLE)
        - 第110-117回
        - 進化的マージ時のタスクとして利用想定.
        - 商用利用不可ライセンス
        - longisland3氏作成. データは[医療美術部の医師国家試験過去問チャート](https://medical-illustration.club/kakomon-chart/med)から引用.
- [JMED-LLM](https://github.com/sociocom/JMED-LLM)
    - 荒牧先生のチームが作成. NERなど8タスク. 
- [JMMLU]()
    - 早稲田大河原研が作成. MMLUの和訳. 
    - CSV形式
- [Japanese-LM-Med-Harness](https://github.com/stardust-coder/japanese-lm-med-harness)
    - IgakuQA, MedQA, MedMCQA, MMLU/JMMLU(医療関係)の評価用プログラム. 日英対訳.

## Available in English
- [MedEval](https://github.com/ZexueHe/MedEval)