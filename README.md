# 📘 NLMS 演算法介紹

## 📌 專案簡介
本專案介紹 **NLMS（Normalized Least Mean Squares）** 演算法，常用於訊號處理與自適應濾波。

---

## 🧾 目錄
- 專案簡介
- 演算法說明
- 圖片展示
- 程式碼
- 表格整理

---

## ✨ 演算法特色
- 使用 **正規化（Normalization）**
- 收斂速度較快
- 比 LMS 更穩定
- 適用於 *訊號處理* 領域
- 可處理 `即時資料`

---

## 🖼️ 演算法公式圖

![NLMS 演算法公式](nlms.png)

📖 **圖說：**  
此圖顯示 NLMS 演算法的完整流程，包含初始化、輸入向量、誤差計算，以及權重更新公式。

---

## 📐 重要公式
> 權重更新會依據誤差進行調整

~~傳統 LMS~~ → 改良為 NLMS

---

## 💻 程式碼範例
```python
import numpy as np

h = h + mu * np.conj(e) * x / (np.dot(np.conj(x), x))
