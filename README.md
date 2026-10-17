# learning-ai-compilers

用互動動畫學 AI Compiler 怎麼運作，以一個極小的 RNN 模型為例。

打開 [`viz/ai_compiler_rnn.html`](viz/ai_compiler_rnn.html)（下載後用瀏覽器開啟，不需網路或伺服器），共三個分頁：

1. **RNN 是什麼**：逐步計算一條長度 4 的序列，看 hidden state 怎麼傳遞
2. **PyTorch → ONNX 長怎樣**：從 `nn.Module` 定義、權重、`torch.onnx.export` 到 ONNX 計算圖
3. **AI Compiler 怎麼編譯**：前端解析 → 高階 IR → 拆解 RNN → 常數折疊 / 迴圈外提 → 算子融合 → Lowering → 迴圈最佳化 → Codegen → Runtime

> 第 ③ 頁的 IR、組合語言與 kernel 數量為教學用的簡化示意。
