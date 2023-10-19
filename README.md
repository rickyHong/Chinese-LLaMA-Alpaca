## 교육 세부정보 [Vocab Expansion]

전체 교육 과정은 어휘 확장, 사전 교육, 교육 미세 조정의 세 부분으로 구성됩니다. 어휘 확장은 [merge_tokenizers.py](scripts/merge_tokenizer/merge_tokenizers.py)를 참조하세요. 🤗transformers의 [run_clm.py](https://github.com/huggingface/transformers/blob/main/examples/pytorch/언어-modeling/run_clm.py) 및 [Stanford의 데이터 세트 처리 관련 부분을 참조하세요. Alpaca](https://github.com/tatsu-lab/stanford_alpaca) 사전 훈련 및 자가 지시 미세 조정을 위한 프로젝트입니다.

우리는 사전 훈련 및 지침 미세 조정(SFT)을 위한 스크립트를 오픈 소스로 제공했습니다.

- 사전 훈련: [scripts/training/run_clm_pt_with_peft.py](./scripts/training/run_clm_pt_with_peft.py), [사전 훈련 위키](https://github.com/ymcui/ Chinese-LLaMA-Alpaca)를 참조하세요. /wiki/사전 훈련 스크립트)

- 지침 미세 조정: [scripts/training/run_clm_sft_with_peft.py](./scripts/training/run_clm_sft_with_peft.py), [SFT Wiki](https://github.com/ymcui/ Chinese-LLaMA-Alpaca/wiki/ 참조) SFT 스크립트)

>>> [📚GitHub Wiki](https://github.com/ymcui/China-LLaMA-Alpaca/wiki/Training-Details)를 참조하세요. <---- Vocab Expansion, 감사합니다.



# [중국어-LLaMA-Alpaca-2 v3.0](https://github.com/ymcui/China-LLaMA-Alpaca-2)에서 긴 컨텍스트 LLM(16K) 출시

[**🇨🇳中文**](./README.md) | [**🌐영어**](./README_EN.md) | [**📖文档/Docs**](https://github.com/ymcui/China-LLaMA-Alpaca/wiki) | [**❓提问/이슈**](https://github.com/ymcui/China-LLaMA-Alpaca/issues) | [**💬讨论/Discussions**](https://github.com/ymcui/China-LLaMA-Alpaca/discussions) | [**⚔️竞技场/Arena**](http://chinese-alpaca-arena.ymcui.com/)

<p 정렬="중앙">
    <br>
    <img src="./pics/banner.png" width="700"/>
    <br>
</p>
<p 정렬="중앙">
    <img alt="GitHub" src="https://img.shields.io/github/license/ymcui/China-LLaMA-Alpaca.svg?color=blue&style=plat-square">
    <img alt="GitHub 릴리스(최신 날짜별)" src="https://img.shields.io/github/v/release/ymcui/China-LLaMA-Alpaca">
    <img alt="GitHub 상위 언어" src="https://img.shields.io/github/언어s/top/ymcui/China-LLaMA-Alpaca">
    <img alt="GitHub 마지막 커밋" src="https://img.shields.io/github/last-commit/ymcui/China-LLaMA-Alpaca">
    <a href="https://app.codacy.com/gh/ymcui/China-LLaMA-Alpaca/dashboard?utm_source=gh&utm_medium=referral&utm_content=&utm_campaign=Badge_grade"><img src="https://app.codacy .com/project/badge/Grade/1710faac5e634acaabfc26b0a778cdde"/></a>
</p>



중국 NLP 커뮤니티에서 대형 모델에 대한 공개 연구를 촉진하기 위해 이 프로젝트에서는 **중국어 LLaMA 모델 및 명령 미세 조정이 포함된 Alpaca 대형 모델**을 오픈 소스로 제공했습니다. 이 모델은 원본 LLaMA를 기반으로 중국어 어휘를 확장하고 2차 사전 학습에 중국어 데이터를 사용하여 중국어 기본 의미 이해를 더욱 향상시킵니다. 또한 이 프로젝트는 중국어 LLaMA를 기반으로 한 미세 조정을 위해 중국어 명령 데이터를 사용하여 모델의 명령 이해 및 실행을 크게 향상시켰습니다.

**기술 보고서(V2)**:[[Cui, Yang, and Yao, 2023] 중국어 LLaMA 및 Alpaca를 위한 효율적이고 효과적인 텍스트 인코딩](https://arxiv.org/abs/2304.08177)

**이 프로젝트의 주요 내용:**

- 🚀 상당한 인코딩/디코딩 효율성을 갖춘 원본 LLaMA 위에 확장된 중국어 어휘
- 🚀 중국어 LLaMA(범용) 및 Alpaca(명령 조정) 오픈 소스
- 🚀 사용자 데이터의 추가 조정을 위한 사전 훈련 및 지침 미세 조정(SFT) 스크립트를 오픈 소스로 제공
- 🚀 노트북(개인용 PC)의 CPU/GPU에서 대형 모델의 양자화된 버전을 빠르게 배포하고 경험해 보세요.
- 🚀 [🤗transformers](https://github.com/huggingface/transformers), [llama.cpp](https://github.com/ggerganov/llama.cpp), [text- Generation-webui]( 지원 https://github.com/oobabooga/text- Generation-webui), [LlamaChat](https://github.com/alexrozanski/LlamaChat), [LangChain](https://github.com/hwchase17/langchain) , , [privateGPT](https://github.com/imartinez/privateGPT) 등
- 출시 버전: 7B(기본, **Plus**, **Pro**), 13B(기본, **Plus**, **Pro**), 33B(기본, **Plus**, ** 찬성**)

💡 다음 이미지는 로컬 배포 후 7B 버전 모델의 실제 경험 효과를 보여줍니다(애니메이션 가속 없음, Apple M1 Max에서 테스트).

![](./pics/screencast.gif)

----

[**중국어-LLaMA-Alpaca-2**](https://github.com/ymcui/China-LLaMA-Alpaca-2)| [비주얼 중국어-LLaMA-Alpaca](https://github.com/airaria/Visual-English-LLaMA-Alpaca) | [멀티모달 VLE](https://github.com/iflytek/VLE) | [중국어 MiniRBT](https://github.com/iflytek/MiniRBT) | [중국어 LERT](https://github.com/ymcui/LERT) | [중국어-영어 PERT](https://github.com/ymcui/PERT) | [중국어 MacBERT](https://github.com/ymcui/MacBERT) | [중국어 ELECTRA](https://github.com/ymcui/China-ELECTRA) | [중국어 XLNet](https://github.com/ymcui/China-XLNet) | [중국어 BERT](https://github.com/ymcui/China-BERT-wwm) | [지식 증류 도구 TextBrewer](https://github.com/airaria/TextBrewer) | [모델 가지치기 도구 TextPruner](https://github.com/airaria/TextPruner)

## 소식

**[2023년 8월 14일] Chinese-LLaMA-Alpaca-2 v2.0이 출시되었습니다. 우리는 Chinese-LLaMA-2-13B 및 Chinese-Alpaca-2-13B를 오픈 소스로 제공합니다. https://github.com/ymcui/China-LLaMA-Alpaca-2 참조**

[2023년 7월 19일] [릴리스 v5.0](https://github.com/ymcui/China-LLaMA-Alpaca/releases/tag/v5.0): Alpaca-Pro 모델을 출시하고 세대 품질을 크게 향상시킵니다. Plus-33B 모델과 함께.

[2023년 7월 19일] [중국어-LLaMA-Alpaca-2 프로젝트](https://github.com/ymcui/China-LLaMA-Alpaca-2)를 출시합니다.

[2023년 7월 10일] 베타 채널 미리보기, 향후 업데이트를 미리 알아보세요. [토론](https://github.com/ymcui/China-LLaMA-Alpaca/discussions/732) 보기

[2023년 7월 7일] 중국-LLaMA-Alpaca 가족이 새로운 구성원을 환영합니다: 시각적 질문 답변을 위한 [비주얼 중국-LLaMA-Alpaca 모델](https://github.com/airaria/Visual-China-LLaMA-Alpaca) 그리고 채팅. 7B 테스트 버전을 사용할 수 있습니다.

[2023년 6월 30일] llama.cpp를 통한 8K 컨텍스트 지원. [토론](https://github.com/ymcui/China-LLaMA-Alpaca/discussions/696)을 참조하세요. 변환기를 사용한 4K+ 컨텍스트 지원은 [PR#705](https://github.com/ymcui/China-LLaMA-Alpaca/pull/705)를 참조하세요.

[2023년 6월 16일] [릴리스 v4.1](https://github.com/ymcui/China-LLaMA-Alpaca/releases/tag/v4.1): 새로운 기술 보고서, C-Eval 추론 스크립트 추가, 추가 저자원 모델 병합 스크립트 등

[2023년 6월 8일] [릴리스 v4.0](https://github.com/ymcui/China-LLaMA-Alpaca/releases/tag/v4.0): LLaMA/Alpaca 33B 버전을 사용할 수 있습니다. 또한 privateGPT 데모, C-Eval 결과 등도 추가합니다.

## 콘텐츠 탐색

| 장 | 설명 |
| -------------------------------- | ------------------------------------- ---------- |
| [다운로드](#모델-다운로드) | 중국어 LLaMA 및 Alpaca 링크 다운로드 |
| [모델 재구성](#Model-Reconstruction) | (중요) 다운로드한 LoRA 모델을 원본 LLaMA와 병합하는 방법을 설명합니다 |
| [빠른 배포](#빠른 배포) | 개인용 컴퓨터에서 LLM을 양자화하고 배포하는 단계 |
| [결과 예](#System-Performance) | 시스템 출력의 예 |
| [교육 세부정보](#Training-Details) | 중국어 LLaMA, 알파카 교육 내용 소개 |
| [FAQ](#FAQ) | 몇 가지 일반적인 질문에 대한 답변 |
| [제한사항](#Limitations) | 이 프로젝트에 관련된 모델의 한계 |

## 모델 다운로드

### ⚠️ 사용자 공지(필독)

공식 [Facebook에서 출시한 LLaMA 모델은 상업적 사용을 금지](https://github.com/facebookresearch/llama)하고 공식 모델 가중치는 오픈 소스로 제공되지 않았습니다(온라인에서 사용할 수 있는 타사 다운로드 링크가 많이 있음). . 관련 라이센스를 준수하기 위해 현재 전체 모델 중량을 공개하는 것은 불가능합니다. 이해해 주셔서 감사합니다. Facebook이 모델 가중치를 완전히 공개한 후 이 프로젝트는 이에 따라 정책을 업데이트합니다. **여기서 공개되는 것은 LoRA 가중치**인데, 이는 원래 LLaMA 모델의 "패치"로 볼 수 있으며, 이 두 가지를 병합하면 완전한 가중치를 얻을 수 있습니다.

### 모델 개요

다음 그림은 우리 프로젝트([2세대 프로젝트](https://github.com/ymcui/China-LLaMA-Alpaca-2) 포함)의 모든 오픈 소스 모델을 보여줍니다.

![](./pics/models.png)

### 어떤 모델을 사용해야 하나요?

다음 표는 중국 LLaMA 및 Alpaca 모델의 기본 비교와 권장 사용 시나리오(포함하되 이에 국한되지 않음)를 제공합니다.

💡 **플러스 버전**은 더 많은 데이터에 대해 교육을 받았으므로 사용을 적극 권장합니다.

| 비교항목 | 중국어 LLaMA | 중국 알파카 |
| ------------------------------------- ---- | ------------------------------------- ---------- | ------------------------------------- ---------- |
| 훈련방법 | 기존 CLM(일반 코퍼스 교육) | 명령어 미세 조정(명령 데이터 학습) |
| 모델 유형 | 기본 모델 | 지시 따르기 모델(예: ChatGPT) |
| 훈련 데이터 | 감독되지 않은 자유 텍스트 | 지도 명령 데이터 |
| 어휘 크기<sup>[3]</sup> | 4995**3** | 4995**4**=49953+1(패드 토큰) |
| 입력 템플릿 | 필요하지 않음 | 템플릿 요구 사항을 충족해야 합니다<sup>[1]</sup> |
| 적합한 시나리오 ✔️ | 텍스트 연속: 컨텍스트가 주어지면 모델이 계속 쓰기 | 1. 수업이해(Q&A, 글쓰기, 조언 등)<br/>2. 다단계 상황 파악(채팅 등) |
| 부적합한 시나리오 ❌ | 지시사항 이해, 다단계 채팅 등 | 무제한 무료 텍스트 생성 |
| 라마.cpp | `-p` 매개변수를 사용하여 컨텍스트를 지정 | '-ins' 매개변수를 사용하여 명령어 이해 + 채팅 모드 활성화 |
| 텍스트 생성-webui | 채팅 모드에 적합하지 않음 | GPU 없이 실행하려면 `--cpu`를 사용하세요. 생성된 콘텐츠가 만족스럽지 않으면 프롬프트 수정을 고려하세요 |
| 라마채팅 | 모델을 로드할 때 "LLaMA"를 선택하세요 | 모델을 로드할 때 "Alpaca"를 선택하세요 |
| [inference_hf.py](./scripts/inference/inference_hf.py) | 추가 시작 매개변수가 필요하지 않습니다 | 시작할 때 `--with_prompt` 매개변수 추가 |
| [웹 데모](./scripts/inference/gradio_demo.py) | 해당 없음 | 간단히 알파카 모델 위치를 제공하세요. 다단계 대화 지원 |
| [LangChain-데모](./scripts/langchain) / privateGPT | 해당 없음 | 간단히 알파카 모델 위치를 제공하세요 |
| 알려진 문제 | 종료를 제어하지 않으면 출력 길이 제한에 도달할 때까지 쓰기를 계속합니다.<sup>[2]</sup> | 짧은 응답을 피하기 위해 Pro 모델을 사용하십시오(Plus 시리즈). |

*[1] 템플릿은 (llama.cpp/LlamaChat/[inference_hf.py](./scripts/inference/inference_hf.py)/[web-demo](./scripts/inference/gradio_demo.py)에 내장되어 있습니다. /[LangChain-demo](./scripts/langchain).*

*[2] 낮은 품질의 모델 응답, 무의미한 답변, 질문 이해 실패 등의 문제가 발생하는 경우 해당 시나리오에 올바른 모델 및 시작 매개변수를 사용하고 있는지 확인하세요.*

*[3] 알파카 모델에는 LLaMA보다 어휘력에 추가 패드 토큰이 있습니다. **LLaMA/Alpaca 토크나이저를 혼합하지 마십시오**.*


### 추천 모델

다음은 이 프로젝트에 권장되는 모델 목록입니다. 이러한 모델은 일반적으로 더 많은 학습 데이터와 최적화된 모델 학습 방법 및 매개 변수를 사용하므로 우선적으로 사용해야 합니다(다른 모델의 경우 [Other Models](#Other-Models)를 확인하세요). **ChatGPT와 같은 상호 작용을 경험하고 싶다면 LLaMA 모델 대신 Alpaca 모델을 사용하세요.** Alpaca 모델의 경우 더 긴 응답을 위해 Pro 버전을 사용하세요. 더 짧은 응답을 원하시면 대신 Plus 시리즈를 사용하십시오.

| 모델 | 유형 | 데이터 | 필수 원본 모델<sup>[1]</sup> | 크기<sup>[2]</sup> | 다운로드 링크<sup>[3]</sup> |
| :--------- | :------------: | :---------------: | :------------------------------------------------- ---: | :----------------: | :------------------------------------------------- ---------: |
| 중국어-LLaMA-Plus-7B | 기본 모델 | 일반 120G | LLaMA-7B | 790M | [[BaiduDisk]](https://pan.baidu.com/s/1zvyX9FN-WSRDdrtMARxxfw?pwd=2gtr)</br>[[Google 드라이브]](https://drive.google.com/file/d /1N97m3rBj-rp-J1X8rgRfluyomEscfAq0/view?usp=sharing) |
| 중국어-LLaMA-Plus-13B | 기본 모델 | 일반 120G | LLaMA-13B | 1.0G | [[BaiduDisk]](https://pan.baidu.com/s/1VGpNlrLx5zHuNzLOcTG-xw?pwd=8cvd)<br/>[[Google 드라이브]](https://drive.google.com/file/d /1q0L5Me_1j_9iiRRNfuEFUt3SOjQo3-g3/view?usp=share_link) |
| 중국어-LLaMA-Plus-33B 🆕 | 기본 모델 | 일반 120G | LLaMA-33B | 1.3G<sup>[6]</sup> | [[BaiduDisk]](https://pan.baidu.com/s/1v2WsSA0RFyVfy7FXY9A2NA?pwd=n8ws)<br/>[[Google 드라이브]](https://drive.google.com/file/d/1S4pBPiIZo7fXqf8hjnFaeE7Z -yZFEta9/view?usp=share_link) |
| 중국어-알파카-Pro-7B 🆕 | 지시 따르기 모델 | 명령 4.3M | *LLaMA-7B 및<br/>LLaMA-Plus-7B*<sup>[4]</sup> | 1.1G | [[BaiduDisk]](https://pan.baidu.com/s/1M7whRwG5DRRkzRXCH4aF3g?pwd=fqpd)<br/>[[Google 드라이브]](https://drive.google.com/file/d/1yfIJ2IXymaTaJ8l7VMnb5LnvQFx3idh -/view?usp=share_link) |
| 중국어-알파카-Pro-13B 🆕 | 지시 따르기 모델 | 명령 4.3M | *LLaMA-13B 및<br/>LLaMA-Plus-13B<sup>[4]</sup>* | 1.3G | [[BaiduDisk]](https://pan.baidu.com/s/1ok5Iiou-MovZa7bFLvt4uA?pwd=m79g)<br/>[[Google 드라이브]](https://drive.google.com/file/d /1IY8PzMje1LM2bIgnniArnmmE8qYaJV_I/view?usp=share_link) |
| 중국어-알파카-Pro-33B 🆕 | 지시 따르기 모델 | 명령 4.3M | *LLaMA-33B 및<br/>LLaMA-Plus-33B<sup>[4]</sup>* | 2.1G | [[BaiduDisk]](https://pan.baidu.com/s/1u2TWZcsG_PZSTnmuu7vwww?pwd=8zj8)<br/>[[Google 드라이브]](https://drive.google.com/file/d/14sFEhRq9c -p8S_TiVYNBnmPr4hk-nhs-/view?usp=share_link) |

**[1]** [Facebook-LLaMA](https://github.com/facebookresearch/llama)에서 사용하려면 원본 LLaMA 모델을 적용하거나 이 [PR](https://github. com/facebookresearch/llama/pull/73/files). 본 프로젝트는 저작권 문제로 인해 다운로드를 제공할 수 없으니 양해 부탁드립니다.

**[2]** 재구성된 모델은 원래 LLaMA보다 약간 더 큽니다(어휘 확장으로 인해). 7B 모델은 약 13G+입니다.

**[3]** 다운로드 후 ZIP 파일의 SHA256이 일치하는지 확인하세요. 전체 값은 [SHA256.md](./SHA256.md)를 참조하세요.

**[4]** Alpaca-Plus의 병합 단계는 다른 것과 다릅니다. [wiki](https://github.com/ymcui/China-LLaMA-Alpaca/wiki/Manual-Conversion#multiple-lora)를 참조하세요. -가중치 병합 적용 가능-중국어-알파카-플러스).

**[5]** 다른 곳에서는 30B 모델이라고도 합니다. Facebook에서 이 모델을 출시할 때 이름 지정 오타가 있었습니다. 우리는 여기서 원래의 종이 명명 규칙(및 실제 무게 수)을 고수합니다.

**[6]** FP16에 저장됩니다.

ZIP 파일 내의 파일 디렉터리는 다음과 같습니다(예: Chinese-LLaMA 사용).

````
Chinese_llama_lora_7b/
  -adapter_config.json # LoRA 가중치 구성 파일
  -adapter_model.bin # LoRA 가중치 파일
  -special_tokens_map.json #special_tokens_map 파일
  - tokenizer_config.json # 토크나이저 구성 파일
  - tokenizer.model # 토크나이저 파일
````

### 기타 모델

학습 방법 및 학습 데이터와 같은 요인으로 인해 **아래 모델은 더 이상 권장되지 않습니다(특정 시나리오에서는 여전히 유용할 수 있음)**. 이전 항목의 [추천모델](#Recommended-Models)을 우선적으로 활용하시기 바랍니다.

| 모델 | 유형 | 데이터 | 필수 원본 모델<sup>[1]</sup> | 크기<sup>[2]</sup> | 다운로드 링크<sup>[3]</sup> |
| :----------------- | :------------: | :------------: | :----------------------: | :----------------: | :------------------------------------------------- ---------: |
| 중국어-LLaMA-7B | 기본 모델 | 일반 20G | LLaMA-7B | 7억 7천만 | [[BaiduDisk]](https://pan.baidu.com/s/1oORTdpr2TvlkxjpyWtb5Sw?pwd=33hb)</br>[[Google 드라이브]](https://drive.google.com/file/d/1iQp9T -BHjBjIrFWXq_kIm_cyNmpvv5WN/view?usp=공유) |
| 중국어-LLaMA-13B | 기본 모델 | 일반 20G | LLaMA-13B | 1.0G | [[BaiduDisk]](https://pan.baidu.com/s/1BxFhYhDMipW7LwI58cGmQQ?pwd=ef3t)<br/>[[Google 드라이브]](https://drive.google.com/file/d/12q9EH4mfKRnoKlbkkhzv1xDwWnroo9VS /view?usp=공유) |
| 중국어-LLaMA-33B | 기본 모델 | 일반 20G | LLaMA-33B | 2.7G | [[BaiduDisk]](https://pan.baidu.com/s/1-ylGyeM70QZ5vbEug5RD-A?pwd=hp6f)<br/>[[Google 드라이브]](https://drive.google.com/file /d/1NwsLYbuEByUxre5GqTN5EkxiuZSRxUy_/view?usp=share_link) |
| 중국어-알파카-7B | 지시추종모델 | 지시 2M | LLaMA-7B | 790M | [[BaiduDisk]](https://pan.baidu.com/s/1xV1UXjh1EPrPtXg6WyG7XQ?pwd=923e)</br>[[Google 드라이브]](https://drive.google.com/file/d/1JvFhBpekYiueWiUL3AF1TtaWDb3clY5D /view?usp=공유) |
| 중국어-알파카-13B | 지시추종모델 | 교육 3M | LLaMA-13B | 1.1G | [[BaiduDisk]](https://pan.baidu.com/s/1wYoSF58SnU9k0Lndd5VEYg?pwd=mm8i)<br/>[[Google 드라이브]](https://drive.google.com/file/d/1gzMc0xMCpXsXmU1uxFlgQ8VRnWNtDjD8 /view?usp=share_link) |
| 중국어-알파카-33B | 지시추종모델 | 명령 4.3M | LLaMA-33B | 2.8G | [[BaiduDisk]](https://pan.baidu.com/s/1fey7lGMMw3GT982l8uJYMg?pwd=2f2s)<br/>[[Google 드라이브]](https://drive.google.com/file/d/1YeSgnZWaRkKdmYa -JHiIlcvqhrDd4-Y4/view?usp=share_link) |
| 중국어-알파카-Plus-7B | 지시추종모델 | 지시 4M | *LLaMA-7B 및<br/>LLaMA-Plus-7B* | 1.1G | [[BaiduDisk]](https://pan.baidu.com/s/12tjjxmDWwLBM8Tj_7FAjHg?pwd=32hc)</br>[[Google 드라이브]](https://drive.google.com/file/d/1EDcTmq6tDmRxqarpapdyDGBE9opY0zrB /view?usp=share_link) |
| 중국어-알파카-플러스-13B | 지시추종모델 | 명령 4.3M | *LLaMA-13B 및<br/>LLaMA-Plus-13B* | 1.3G | [[BaiduDisk]](https://pan.baidu.com/s/1Mew4EjBlejWBBB6_WW6vig?pwd=mf5w)<br/> [[Google 드라이브]](https://drive.google.com/file/d/1CcLJvY7XsFAOjfSIqCpDI7jf3EEPDcEF /view?usp=share_link) |
| 차이니즈-알파카-플러스-33B | 지시추종모델 | 명령 4.3M | *LLaMA-33B 및<br/>LLaMA-Plus-33B* | 2.1G | [[BaiduDisk]](https://pan.baidu.com/s/1j2prOjiQGB8S5x67Uj8XZw?pwd=3pac)<br/>[[Google 드라이브]](https://drive.google.com/file/d/1YUaT -NOReoF-z1vzj2khwYKdj4Z_ekbO/view?usp=share_link) |

### 🤗트랜스포머와 함께 사용하세요

위 모델을 모두 🤗Model Hub에서 다운로드하고 [transformers](https://github.com/huggingface/transformers) 및 [PEFT](https://github.com/huggingface/peft)와 함께 사용하여 호출할 수 있습니다. 중국 LLaMA 또는 Alpaca LoRA 모델. 아래에 언급된 모델 호출 이름은 `.from_pretrained()`에 지정된 모델 이름입니다.

- Pro 버전 이름 지정(Alpaca만 해당): `ziqingyang/chinese-alpaca-pro-lora-${model_size}`

- 플러스 버전 이름: `ziqingyang/chinese-${model_name}-plus-lora-${model_size}`

- 기본 버전 이름: `ziqingyang/chinese-${model_name}-lora-${model_size}`
- `$model_name`: `llama` 또는 `alpaca`; `$model_size`: `7b`, `13b`, `33b`

- 예: Chinese-LLaMA-Plus-33B 모델의 호출 이름은 'ziqingyang/chinese-llama-plus-lora-33b'입니다.

상세 목록 및 모델 다운로드 링크: https://huggingface.co/ziqingyang

## 모델 재구성

추가 조정이나 추론을 위해 LoRA 모델을 원본 LLaMA와 병합하기 위해 현재 두 가지 방법이 제공됩니다.

| 방법 | 사용법 | 튜토리얼 |
| :--------- | :------------------------------------------------- ---------- | :------------------------------------------------- ---------: |
| **온라인 변환** | Google Colab 사용자에게 적합하며 온라인 변환 및 모델 양자화를 위해 노트북을 사용할 수 있습니다. | [링크](https://github.com/ymcui/China-LLaMA-Alpaca/wiki/Online-conversion-with-Colab) |
| **수동 변환** | 오프라인 변환에 적합하며 양자화 또는 추가 미세 조정을 위해 다양한 형식으로 모델을 생성합니다. | [링크](https://github.com/ymcui/China-LLaMA-Alpaca/wiki/Manual-Conversion) |

다음은 각 원본 모델의 크기와 4비트 양자화이다. 해당 모델을 변환할 때 머신에 충분한 메모리와 디스크 공간이 있는지 확인하십시오(최소 요구 사항).

| | 7B | 13B | 33B | 65B |
| :----------------- | :----: | :------: | :------: | :------: |
| 원본(FP16) | 13GB | 24GB | 60GB | 120GB |
| 양자화(8비트) | 7.8GB | 14.9GB | 32.4GB | ~60GB |
| 양자화(4비트) | 3.9GB | 7.8GB | 17.2GB | 38.5GB |

관련 문서는 프로젝트의 >>> [📚GitHub Wiki](https://github.com/ymcui/China-LLaMA-Alpaca/wiki/Model-Reconstruction)로 이동되었습니다.

## 빠른 배포

추론 및 로컬 배포를 위해 주로 다음 세 가지 방법을 제공합니다.

| 방법 | 특징 | 플랫폼 | CPU | GPU | 양자화 | UI | 튜토리얼 |
| :------------------------------------------------- ---------- | ------------------------------------- ---------- | :------: | :--: | :--: | :----------: | :--: | :------------------------------------------------- ---------: |
| [**llama.cpp**](https://github.com/ggerganov/llama.cpp) | 모델을 양자화하고 로컬 CPU에 배포하기 위한 도구 | 일반 | ✅ | ✅ | ✅ | ❌ | [링크](https://github.com/ymcui/China-LLaMA-Alpaca/wiki/llama.cpp-Deployment) |
| [**🤗Transformers**](https://github.com/huggingface/transformers) | 원래 변환기 추론 방법, CPU/GPU 지원 | 일반 | ✅ | ✅ | ✅ | ✅ | [링크](https://github.com/ymcui/China-LLaMA-Alpaca/wiki/Inference-with-Transformers) |
| [**텍스트 생성-webui**](https://github.com/oobabooga/text- Generation-webui) | 모델을 웹 UI로 배포하기 위한 도구 | 일반 | ✅ | ✅ | ✅ | ✅ | [링크](https://github.com/ymcui/China-LLaMA-Alpaca/wiki/text- Generation-webui) |
| [**LlamaChat**](https://github.com/alexrozanski/LlamaChat) | LLaMA, Alpaca 등과 채팅할 수 있는 macOS 앱 | 맥OS | ✅ | ❌ | ✅ | ✅ | [링크](https://github.com/ymcui/China-LLaMA-Alpaca/wiki/Using-LlamaChat-Interface) |
| [**LangChain**](https://github.com/hwchase17/langchain) | 2차 개발에 적합한 LLM 애플리케이션 개발 프레임워크 | 일반 | ✅<sup>†</sup> | ✅ | ✅<sup>†</sup> | ❌ | [링크](https://github.com/ymcui/China-LLaMA-Alpaca/wiki/Integrated-with-LangChain) |
| [**privateGPT**](https://github.com/imartinez/privateGPT) | LangChain 기반 다중 문서 QA 프레임워크 | 일반 | ✅ | ✅ | ✅ | ❌ | [링크](https://github.com/ymcui/China-LLaMA-Alpaca/wiki/Use-privateGPT-for-multi-document-QA) |
| [**Colab Gradio 데모**](https://github.com/ymcui/China-LLaMA-Alpaca/blob/main/notebooks/gradio_web_demo.ipynb) | Colab에서 Gradio 웹 데모 실행 | 일반 | ✅ | ✅ | ✅ | ❌ | [링크](https://colab.research.google.com/github/ymcui/China-LLaMA-Alpaca/blob/main/notebooks/gradio_web_demo.ipynb) |
| [**API 호출**](https://platform.openai.com/docs/api-reference) | OPENAI API를 구현하는 서버 | 일반 | ✅ | ✅ | ✅ | ❌ | [링크](https://github.com/ymcui/China-LLaMA-Alpaca/wiki/API-Calls) |


<sup>†</sup>: LangChain에서 지원되지만 튜토리얼에서는 구현되지 않습니다. 자세한 내용은 공식 LangChain 문서를 참조하세요.

관련 문서는 프로젝트 >>> [📚GitHub Wiki](https://github.com/ymcui/China-LLaMA-Alpaca/wiki/Model-Inference-and-Deployment)로 이동되었습니다.

## 시스템 성능

### 세대 성능 테스트

관련 모델의 실제 성능을 신속하게 평가하기 위해 이 프로젝트에서는 동일한 주어진 몇 가지 공통 작업에 대해 중국산 Alpaca-7B, Alpaca-13B, Alpaca-Plus-7B, Alpaca-Plus-13B 및 Alpaca-33B의 효과를 비교했습니다. 즉각적인. 응답 생성은 무작위이며 하이퍼파라미터 디코딩 및 무작위 시드와 같은 요인의 영향을 받습니다. 다음 관련 평가는 절대적으로 엄격한 것은 아니며 테스트 결과는 참고용일 뿐입니다. 직접 경험해 보시기 바랍니다.

- 자세한 평가 결과는 [예시](./examples)를 참고하세요.
- 📊 알파카 챗봇 아레나: [http://chinese-alpaca-arena.ymcui.com](http://chinese-alpaca-arena.ymcui.com/)

### NLU 성능 테스트

이 프로젝트는 또한 "NLU" 객관적 평가 데이터 세트를 사용하여 관련 모델에 대한 테스트를 수행했습니다. 이러한 유형의 평가 결과는 객관적이며 지정된 레이블의 출력만 필요하므로 다른 관점에서 대규모 모델의 기능에 대한 통찰력을 제공할 수 있습니다. 최근 출시된 [C-Eval 데이터 세트](https://cevalbenchmark.com/)에서 이 프로젝트는 관련 모델의 성능을 테스트했습니다. 테스트 세트에는 52개 주제를 다루는 12.3K개의 객관식 문제가 포함되어 있습니다. 다음은 검증 세트와 테스트 세트에 대한 일부 모델의 평가 결과(평균)입니다. 전체 결과를 보려면 [기술 보고서](https://arxiv.org/abs/2304.08177)를 참조하세요.

| 모델 | 유효(제로샷) | 유효(5발) | 테스트(제로샷) | 테스트(5샷) |
| ---------- | :---------------: | :------------: | :---------------: | :------------: |
| 차이니즈-알파카-플러스-33B | 46.5 | 46.3 | 44.9 | 43.5 |
| 중국어-알파카-33B | 43.3 | 42.6 | 41.6 | 40.4 |
| 중국어-알파카-플러스-13B | 43.3 | 42.4 | 41.5 | 39.9 |
| 중국어-알파카-Plus-7B | 36.7 | 32.9 | 36.4 | 32.3 |
| 중국어-LLaMA-Plus-33B | 37.4 | 40.0 | 35.7 | 38.3 |
| 중국어-LLaMA-33B | 34.9 | 38.4 | 34.6 | 39.5 |
| 중국어-LLaMA-Plus-13B | 27.3 | 34.0 | 27.8 | 33.3 |
| 중국어-LLaMA-Plus-7B | 27.3 | 28.3 | 26.9 | 28.4 |

대형 모델의 성능에 대한 종합적인 평가는 여전히 시급하고 다루어야 할 중요한 주제라는 점을 기억하는 것이 중요합니다. 대형모델 기술의 건전한 발전을 도모하기 위해서는 대형모델의 다양한 평가 결과를 합리적이고 균형 있게 접근하는 것이 유익하다. 사용자가 자신의 작업에 대해 테스트를 수행하고 해당 작업에 적합한 모델을 선택하는 것이 좋습니다.

C-Eval 추론 코드는 >>> [📚GitHub Wiki](https://github.com/ymcui/China-LLaMA-Alpaca/wiki/C-Eval-performance-and-script)를 참조하세요.

## 교육 세부정보

전체 교육 과정은 어휘 확장, 사전 교육, 교육 미세 조정의 세 부분으로 구성됩니다. 어휘 확장은 [merge_tokenizers.py](scripts/merge_tokenizer/merge_tokenizers.py)를 참조하세요. 🤗transformers의 [run_clm.py](https://github.com/huggingface/transformers/blob/main/examples/pytorch/언어-modeling/run_clm.py) 및 [Stanford의 데이터 세트 처리 관련 부분을 참조하세요. Alpaca](https://github.com/tatsu-lab/stanford_alpaca) 사전 훈련 및 자가 지시 미세 조정을 위한 프로젝트입니다.

우리는 사전 훈련 및 지침 미세 조정(SFT)을 위한 스크립트를 오픈 소스로 제공했습니다.

- 사전 훈련: [scripts/training/run_clm_pt_with_peft.py](./scripts/training/run_clm_pt_with_peft.py), [사전 훈련 위키](https://github.com/ymcui/ Chinese-LLaMA-Alpaca)를 참조하세요. /wiki/사전 훈련 스크립트)

- 지침 미세 조정: [scripts/training/run_clm_sft_with_peft.py](./scripts/training/run_clm_sft_with_peft.py), [SFT Wiki](https://github.com/ymcui/ Chinese-LLaMA-Alpaca/wiki/ 참조) SFT 스크립트)

>>> [📚GitHub Wiki](https://github.com/ymcui/China-LLaMA-Alpaca/wiki/Training-Details)를 참조하세요.


## 자주하는 질문

FAQ는 자주 묻는 질문에 대한 답변을 제공합니다. 문제를 제출하기 전에 FAQ를 참조하세요.

````
Q1: 전체 모델 가중치를 공개할 수 없는 이유는 무엇입니까?
Q2: 앞으로 33B, 65B 버전이 나올 예정인가요?
Q3: 모델이 일부 작업에서 제대로 작동하지 않습니다!
Q4: 왜 어휘를 확장하나요? 원래 LLaMA를 중국 데이터로 사전 훈련할 수는 없나요?
Q5: 답변이 너무 짧습니다.
Q6: Windows에서는 모델이 중국어를 이해하지 못하거나 생성 속도가 매우 느린 등의 현상이 발생합니다.
Q7: 중국-LLaMA 13B 모델은 llama.cpp를 사용하여 시작할 수 없으며 크기가 일치하지 않는다고 보고됩니다.
Q8: 차이니즈-알파카-플러스는 다른 것보다 좋은 성능을 보이지 않습니다.
Q9: 모델은 텍스트 분류와 같은 NLU 작업에서 제대로 작동하지 않습니다.
Q10: 왜 30B가 아니고 33B인가요?
Q11: 일관성 없는 SHA256
````

>>> [📚GitHub Wiki](https://github.com/ymcui/China-LLaMA-Alpaca/wiki/FAQ)를 참조하세요.

## 제한사항

본 프로젝트의 모델은 원래 LLaMA 및 Alpaca에 비해 중국어 이해 및 생성 능력이 크게 향상되었지만 다음과 같은 제한 사항도 있습니다.

- 예측할 수 없는 유해한 내용 및 인간의 취향과 가치관에 부합하지 않는 내용을 생산할 수 있습니다.
- 컴퓨팅 파워 및 데이터 문제로 인해 관련 모델의 학습이 충분하지 않아 중국어 이해력을 더욱 향상시킬 필요가 있음.
- 현재 사용할 수 있는 온라인 대화형 데모가 없습니다(참고: 사용자는 여전히 로컬로 직접 배포할 수 있습니다).

## 인용

우리 프로젝트의 모델, 데이터, 코드가 유용하다고 생각되면 다음과 같이 우리 작업을 인용하는 것을 고려해 보십시오: https://arxiv.org/abs/2304.08177

````
@article{중국-라마-알파카,
      title={중국어 LLaMA 및 Alpaca를 위한 효율적이고 효과적인 텍스트 인코딩},
      작성자={Cui, Yiming 및 Yang, Ziqing 및 Yao, Xin},
      저널={arXiv 사전 인쇄 arXiv:2304.08177},
      URL={https://arxiv.org/abs/2304.08177},
      연도={2023}
}
````

## 관련 프로젝트

| 프로젝트 이름 | 설명 | 유형 |
| :------------------------------------------------- ---------- | :------------------------- | :---------: |
| [**중국어-LLaMA-Alpaca-2**](https://github.com/ymcui/China-LLaMA-Alpaca-2)(공식) | 중국어 LLaMA-2, Alpaca-2 LLM | 텍스트 |
| [**Visual-China-LLaMA-Alpaca**](https://github.com/airaria/Visual-China-LLaMA-Alpaca)(공식) | 다중 모드 중국어 LLaMA 및 알파카 LLM | 다중 모드 |

이 목록에 참여하고 싶나요? >>> [여기에서 신청하세요](https://github.com/ymcui/China-LLaMA-Alpaca/discussions/740)


## 감사의 말씀

본 프로젝트는 2차 개발을 위한 다음의 오픈소스 프로젝트를 기반으로 진행되며, 관련 프로젝트와 연구개발 인력 여러분께 감사의 말씀을 드립니다.

| 기초 모델, 코드 | 양자화, 추론, 배포 | 데이터 |
| :------------------------------------------------- ---------: | :------------------------------------------------- ---------: | :------------------------------------------------- ---------: |
| [Facebook의 LLaMA](https://github.com/facebookresearch/llama)<br/>[Stanford의 Alpaca](https://github.com/tatsu-lab/stanford_alpaca)<br/>[alpaca-lora by @tloen](https://github.com/tloen/alpaca-lora) | [@ggerganov의 llama.cpp](https://github.com/ggerganov/llama.cpp)<br/>[@alexrozanski의 LlamaChat]( https://github.com/alexrozanski/LlamaChat)<br/> [@oobabooga의 텍스트 생성-webui](https://github.com/oobabooga/text- Generation-webui) | [@brightmart의 pCLUE 및 번역 데이터](https://github.com/brightmart/nlp_chinese_corpus)<br/>[OpenAssistant의 oasst1](https://huggingface.co/datasets/OpenAssistant/oasst1) |

에피소드: 현재 로고는 DALL·E 플러그인을 사용하여 GPT-4에 의해 자동으로 생성됩니다(이전에는 midjourney에서 생성됨).

## 면책조항

**본 프로젝트와 관련된 리소스는 학술 연구 목적으로만 사용되며 상업적인 사용은 엄격히 금지됩니다.** 타사 코드가 포함된 부분을 사용할 경우 해당 오픈 소스 계약을 엄격히 따르십시오. 모델에 의해 생성된 콘텐츠는 모델 계산, 무작위성, 양자화 정확도 손실 등의 요인에 의해 영향을 받습니다. 본 프로젝트는 정확성을 보장할 수 없습니다. 모델에 의해 출력된 콘텐츠에 대해 본 프로젝트는 법적 책임을 지지 않으며, 관련 리소스 사용 및 출력 결과로 인해 발생할 수 있는 손실에 대해 책임을 지지 않습니다.

이 프로젝트는 개인과 협력자가 여가 시간에 시작하고 유지 관리하므로 관련 문제 해결에 대한 시기적절한 대응을 보장할 수 없습니다.

## 피드백

질문이 있으시면 GitHub 이슈에 제출해 주세요.

- 질문을 제출하기 전에 FAQ가 문제를 해결할 수 있는지 확인하고, 과거 문제를 상담하여 도움이 될 수 있는지 확인하세요.
- 제출 시 전용 이슈 템플릿을 사용하시기 바랍니다.
- 중복되고 관련되지 않은 문제는 [stable-bot](https://github.com/marketplace/stale)에서 처리됩니다. 이해해주세요.
- 정중하게 질문을 제기하고, 조화로운 토론 커뮤니티를 구축할 수 있도록 도와주세요.
