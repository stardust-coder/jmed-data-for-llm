# 日本語の医療分野関連データ（医療LLM開発用）

Curation of Japanese Medical Data Sources for LLM development.  
Let's go "Soverign AI" !


### 国内モデル開発の取り組み


| 事業者 | モデル | モデルサイズ | 手法 | IgakuQA | source |
|---|---|---|---|---|---|
| EQUES | [JPharmatron](https://github.com/stardust-coder/awesome-latest-LLM/blob/master) | 7B | 継続学習 | 64.7% ||
| 東大病院 | [JMedLoRA](https://arxiv.org/pdf/2310.10083) | 70B | LoRA | 33.1% ||
| PFN | [Preferred-MedLLM-Qwen-72B](https://huggingface.co/pfnet/Preferred-MedLLM-Qwen-72B) | 72B | 継続学習 | 86.1 ~ 86.2% | [{1}](https://prtimes.jp/main/html/rd/p/000000061.000047565.html) [{3}](https://tech.preferred.jp/ja/blog/preferred-medllm-qwen-72b/) |
| ELYZA | [ELYZA-Med-Base-1.0-Qwen2.5-72B](https://prtimes.jp/main/html/rd/p/000000061.000047565.html) | 72B | 継続学習 | 86.7% ||
| NII | [SIP-jmed-llm-2-8x13b-OP-instruct](https://huggingface.co/SIP-med-LLM/SIP-jmed-llm-2-8x13b-OP-instruct) | 8x13B, MoE | 継続学習, SFT| 約80% | |
| （参考）| GPT-4o | 不明 | - | 86.6 ~ 88.9% | [{1}](https://prtimes.jp/main/html/rd/p/000000061.000047565.html) [{2}](https://arxiv.org/pdf/2506.11114) [{3}](https://tech.preferred.jp/ja/blog/preferred-medllm-qwen-72b/) |
| （参考）| o1-preview | 不明 | - |  88.4%  | [{1}](https://prtimes.jp/main/html/rd/p/000000061.000047565.html) |


### 学習用コーパス
- JST（抄録&本文）
    - [JMedRoBERTa](https://www.anlp.jp/proceedings/annual_meeting/2023/pdf_dir/P3-1.pdf)で学習用に利用.
    - 医学論文およそ1100万件.
- [J-ResearchCorpus](https://huggingface.co/datasets/kunishou/J-ResearchCorpus)
- [Apollo Corpus JP](https://huggingface.co/datasets/kunishou/ApolloCorpus-ja)
- [JASMINE](https://github.com/OnizukaLab/JASMINE)
    - テキスト平易化パラレルコーパス
- [JP-AlpaCare-MedInstruct-52k](https://huggingface.co/datasets/li-lab/JP-AlpaCare-MedInstruct-52k)
    - [AlpaCare](https://huggingface.co/datasets/lavita/AlpaCare-MedInstruct-52k)をGPT-4oで機械翻訳した日本語データセット

### 評価用タスク
**※原則としてLLMの学習データに含めるべきではない！**
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
    - [IgakuQA119](https://github.com/docto-rin/IgakuQA119)
        - 第119回医師国家試験のリーダーボード.
        - Gemini-2.5-Proがトップ.
    - [NMLE](https://huggingface.co/datasets/longisland3/NMLE)
        - 第110-117回
        - 進化的マージ時のタスクとして利用想定.
        - 商用利用不可ライセンス
        - longisland3氏作成. データは[医療美術部の医師国家試験過去問チャート](https://medical-illustration.club/kakomon-chart/med)から引用.
    - [NMLE-RTA](https://github.com/iKora128/nmle-rta/tree/main)
    - [Kokushi-MD10](https://huggingface.co/datasets/humanalysis-square/KokushiMD-10)
        - 10種類の医療関係の国家試験

- 薬剤師国家試験
    - [YakugakuQA (EQUES)]()
- [JPharmaBench　(EQUES)]()
    - 名寄せベンチマーク NayoseQA
    - 齟齬チェックベンチマーク　SogoCheck
- [JMED-LLM](https://github.com/sociocom/JMED-LLM)
    - 荒牧先生のチームが作成. NERなど8タスク. 
- [JMMLU](https://github.com/nlp-waseda/JMMLU)
    - NAIST早稲田大河原研が作成. MMLUの和訳. 
    - CSV形式のデータセット.
- [MMLU-ProX](https://mmluprox.github.io/)
    - 多言語. 一部に日本語も含まれる. 
- [JMedBench](https://huggingface.co/datasets/Coldog2333/JMedBench)
    - あらゆる医療の質問応答データセットをjsonlで格納. GPTによる機械翻訳により日英が用意.
    - IgakuQA, MedQA, EJMMT など.
- [DenQA](https://github.com/aistairc/medLLM_QA_benchmark)
    - 歯科医師国家試験
    - 2023~2024

### ツール類
- [JaMIE: a Japanese Medical Information Extraction toolkit](https://github.com/racerandom/JaMIE)
- [Japanese-LM-Med-Harness](https://github.com/stardust-coder/japanese-lm-med-harness)
    - IgakuQA, MedQA, MedMCQA, MMLU/JMMLU(医療関係)の評価用プログラム. 日英対訳.

### その他データ
- [万病辞書](https://sociocom.naist.jp/resources-software/)
    - NAIST荒牧先生のチームが作成. その他のデータやコードも充実.
    - CSV形式. 380330件の病名やICDコードなど.
- [Mecon Audio](https://github.com/elith-co-jp/meconaudio)
    - 原則非商用
- [PRO annotations on Weblogs](https://yukiar.github.io/pro_jp/)
- 英語の医療データセット一覧については[こちら](https://github.com/stardust-coder/awesome-latest-LLM)の最下部を参照.

### 参考文献
- [医療ドメイン特化LLMの性能はどうやって評価する？](https://zenn.dev/hellorusk/articles/04a29974138c7b)
- [JMedLoRA](https://www.anlp.jp/proceedings/annual_meeting/2024/pdf_dir/P9-4.pdf)
- [医療・ヘルスケア領域における大規模言語モデルの構築に向けて](https://tech.preferred.jp/ja/blog/llama3-preferred-medswallow-70b/)


### キーワード
医療LLM, 医療×LLM, 医療AI, 医療×AI, 医療自然言語処理, 日本語医療LLM