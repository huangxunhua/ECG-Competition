# 赛题2 可穿戴12导联动态心电质量评估

心电图（ECG）因其无创性、成本低和使用方便等优势已成为心血管疾病广泛采用的诊断工具，而心电数据的准确性和可靠性取决于记录的质量，这对于专家诊断和数据挖掘至关重要。然而，心电信号极易受到噪声的影响，如基线漂移（图1）、电极干扰（图2）、肌肉颤动（图3）和运动伪影（图4）等。随着可穿戴心电图测量设备的出现，噪声问题日益严重，对心电图数据的准确性和可靠性构成了重大挑战。因此，如何准确的评估动态心电质量是一个实际且亟待解决的问题。


<img width="416" alt="图片 1-1" src="https://github.com/huangxunhua/ECG-Competition/assets/17960800/cc148dbb-2a0b-4156-8757-72ca11870440">

<img width="416" alt="图片 1-2" src="https://github.com/huangxunhua/ECG-Competition/assets/17960800/dd19d026-41b0-4341-8da1-f04dd483426b">
<img width="416" alt="图片 1-3" src="https://github.com/huangxunhua/ECG-Competition/assets/17960800/cfd8950b-0e55-4c47-8f9e-1b37d8228c12">
<img width="416" alt="图片 1-4" src="https://github.com/huangxunhua/ECG-Competition/assets/17960800/5a2f35b4-35d8-459c-bdc3-c63a6e62c680">

<img width="416" alt="图片2-1" src="https://github.com/huangxunhua/ECG-Competition/assets/17960800/ef36152e-cf5d-46cc-b9de-3afce6f1b69b">

<img width="416" alt="图片 2-2" src="https://github.com/huangxunhua/ECG-Competition/assets/17960800/c433b162-0b6c-452e-807a-7044c63eb03b">

<img width="416" alt="图片 2-3" src="https://github.com/huangxunhua/ECG-Competition/assets/17960800/c6a460b7-ec85-40c4-9adf-b2bf748dd4c1">

本赛题使用的数据集来自真实世界的动态心电数据，包含 10 名患者的标准 12 导联心电图共100条。这些心电信号的采样频率为 100 Hz，并被分割为每条10 秒。数据集标签根据波形可见度分为四类： A 类代表所有波形清晰可见，无基线漂移，采集质量高。B 类表示存在 1-3 个干扰心跳，但不会对诊断产生重大影响。C 类表示能识别 50%以上的波形，对诊断有部分影响。D 类表示完全无法识别波形，没有可用的心电信号。数据集和标签以标准npy格式存储。

本赛题质量评估任务分为两个子题：
（1）	二分类质量评估，一类为高质量心电（标签A），另一类为其他（标签B/C/D）。
（2）	四分类质量评估，四类标签分别为A/B/C/D。
性能评估指标需统一展示Precision，Recall和F1 Score，并以F1 Score作为算法评价标准。

