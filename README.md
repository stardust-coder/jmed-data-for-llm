# 日本語の医療分野関連データセット（医療LLM開発用）

Curation of Japanese Medical Data Sources for LLM development.


### 学習用コーパス
- [JST（抄録&本文）]()
    - NII相澤先生のチーム [JMedRoBERTa](https://www.anlp.jp/proceedings/annual_meeting/2023/pdf_dir/P3-1.pdf)で学習用に利用.
    - 医学論文およそ1100万件.
- [J-ResearchCorpus](https://huggingface.co/datasets/kunishou/J-ResearchCorpus)
- [Apollo Corpus JP](https://huggingface.co/datasets/kunishou/ApolloCorpus-ja)
- [JASMINE](https://github.com/OnizukaLab/JASMINE)
    - テキスト平易化パラレルコーパス


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
    - あらゆる医療の質問応答データセットをjsonlで格納. GPTによる機械翻訳により日英が用意.
    - IgakuQA, MedQA, EJMMT など.

### ツール
- [JaMIE: a Japanese Medical Information Extraction toolkit](https://github.com/racerandom/JaMIE)

### その他
- [万病辞書](https://sociocom.naist.jp/resources-software/)
    - NAIST荒牧先生のチームが作成. その他のデータやコードも充実.
    - CSV形式. 380330件の病名やICDコードなど.
- [医療ドメイン特化LLMの性能はどうやって評価する？](https://zenn.dev/hellorusk/articles/04a29974138c7b)
- [Mecon Audio](https://github.com/elith-co-jp/meconaudio)
    - 原則非商用
- 英語の医療データセット一覧については[こちら](https://github.com/stardust-coder/awesome-latest-LLM)の最下部を参照。