# Alphabet 的 Tacotron 2 文本到语音引擎听起来与人类几乎没有区别

> 原文：<https://www.xda-developers.com/alphabet-tactron-2-speech-indistinguishable-from-humans/>

Alphabet 的子公司 DeepMind 在 10 月份开发了 [WaveNet](https://www.xda-developers.com/deepmind-wavenet-google-assistant-tpu/) ，这是一个为谷歌助手的语音合成提供动力的神经网络。它能够比搜索巨头之前的文本到语音系统提供更好、更真实的音频样本，更重要的是，它从配音演员那里生成原始音频，而不是拼接在一起的声音。现在，Alphabet 的研究人员开发了一个新版本 Tacotron 2，它使用多个神经网络来产生几乎无法与人类区分的语音。

这里有一个样本。第一个是使用 Tacotron 2 生成的，第二个是配音演员:

[audio wav = " https://static 1 . xd aimages . com/WordPress/WP-content/uploads/2017/12/Washington _ gen . wav "][/audio]

[audio wav = " https://static 1 . xd aimages . com/WordPress/WP-content/uploads/2017/12/Washington _ gt . wav "][/audio]

Tacotron 2 由两个深度神经网络组成。正如本月发表的研究论文所描述的那样，第一种将文本翻译成声谱图，这是音频频谱的可视化表示。第二个——deep mind 的 wave net——解读图表，生成相应的音频元素。结果是一个端到端的引擎，它可以强调单词，正确地发音，提取语法线索(即，强调斜体或大写的单词)，并根据标点符号改变发音方式。

目前还不清楚 Tacotron 2 是否会像谷歌助手一样面向用户的服务，但这是意料之中的事情。DeepMind 的 WaveNet 研究发表后不久，谷歌在智能手机、扬声器和平板电脑上推出了基于机器学习的多语言语音识别。

只有一个问题:现在，Tacotron 2 系统被训练成模仿一个女性的声音。为了生成新的声音和语音模式，谷歌需要再次训练该系统。

* * *

[**taco tron 2**](https://google.github.io/tacotron/publications/tacotron2/index.html)