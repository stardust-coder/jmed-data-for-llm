# Curation of Japanese Medical Data Sources for LLM development

## Available in Japanese

### 学習用コーパス
- [PubMedコーパス]()
    - NII相澤先生のチーム JMedRoBERTaで学習用に利用.
    - 医学論文1100万件.


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
        - [Kasai et al.](https://arxiv.org/abs/2303.18027)が作成.
    - [NMLE](https://huggingface.co/datasets/longisland3/NMLE)
        - 第110-117回
        - 進化的マージ時のタスクとして利用想定.
        - 商用利用不可ライセンス
        - longisland3氏作成. データは[医療美術部の医師国家試験過去問チャート](https://medical-illustration.club/kakomon-chart/med)から引用.
- [JMED-LLM](https://github.com/sociocom/JMED-LLM)
    - 荒牧先生のチームが作成. NERなど8タスク. 
- [JMMLU](https://github.com/nlp-waseda/JMMLU)
    - NAIST早稲田大河原研が作成. MMLUの和訳. 
    - CSV形式
- [Japanese-LM-Med-Harness](https://github.com/stardust-coder/japanese-lm-med-harness)
    - IgakuQA, MedQA, MedMCQA, MMLU/JMMLU(医療関係)の評価用プログラム. 日英対訳.
- [JMedBench](https://huggingface.co/datasets/Coldog2333/JMedBench)
    - あらゆる医療の質問応答データセットをjsonlで格納.


### その他
- [万病辞書](https://sociocom.naist.jp/resources-software/)
    - NAIST荒牧先生のチームが作成. その他のデータやコードも充実.
    - CSV形式. 380330件の病名やICDコードなど.
- 英語の医療データセット一覧については[こちら](https://github.com/stardust-coder/awesome-latest-LLM)の最下部を参照。