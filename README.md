# 🚀 訊號處理演算法實作：NLMS 濾波器

> 本專案用於展示 **Normalized Least Mean Squares (NLMS)** 演算法的數學邏輯與 Markdown 排版技巧。透過適應性濾波技術，實現訊號的動態追蹤與處理。

---

## 📝 專案簡介
這是一個關於**適應性濾波器 (Adaptive Filter)** 的實驗紀錄。我們透過 Markdown 格式完整紀錄演算法的初始化與疊代計算過程，方便開發者快速理解核心邏輯。

### 🛠️ 使用工具與熟練度
| 工具名稱 | 用途 | 熟練度 |
| :--- | :--- | :--- |
| **GitHub** | 程式碼版本管理 | ⭐⭐⭐ |
| **Markdown** | 技術文件撰寫 | ⭐⭐⭐⭐ |
| **Python** | 演算法邏輯實作 | ⭐⭐⭐ |
| **LaTeX** | 數學公式渲染 | ⭐⭐⭐⭐⭐ |

---

## 📸 演算法數學模型
以下是 NLMS 演算法核心公式的邏輯架構：

![NLMS Algorithm Flow](https://raw.githubusercontent.com/你的帳號/你的儲存庫名稱/main/image_33f101.png)
*(註：建議將此路徑替換為你儲存庫中的實際圖片連結)*

---

## 💡 技術細節解析

### 1. 初始化 (Initialization)
在計算開始前，必須將濾波器權重向量 $\mathbf{\hat{h}}$ 初始化為零向量：
$$\mathbf{\hat{h}}(0) = \text{zeros}(p)$$
*其中 $p$ 代表濾波器的階數 (Tap length)。*

### 2. 疊代計算 (Computation)
對於每一個離散時間點 $n = 0, 1, 2, \dots$，依序執行以下三個核心步驟：

* **輸入向量構建**：
    $$\mathbf{x}(n) = [x(n), x(n-1), \dots, x(n-p+1)]^T$$
* **誤差計算 (Error Estimation)**：
    $$e(n) = d(n) - \mathbf{\hat{h}}^H(n)\mathbf{x}(n)$$
* **權重更新 (Weight Update)**：
    $$\mathbf{\hat{h}}(n+1) = \mathbf{\hat{h}}(n) + \frac{\mu e^*(n)\mathbf{x}(n)}{\mathbf{x}^H(n)\mathbf{x}(n)}$$

---

## 💻 程式碼實作範例 (Python)

```python
import numpy as np

def run_nlms(x, d, p, mu, eps=1e-8):
    # 初始化
    h_hat = np.zeros(p)
    # 疊代計算邏輯...
    # e[n] = d[n] - h_hat.H @ x[n]
    # h_hat = h_hat + (mu * e_star * x) / (norm(x)^2 + eps)
    pass
