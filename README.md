# 🚀 訊號處理演算法實作：NLMS 濾波器

> 本專案用於展示 **Normalized Least Mean Squares (NLMS)** 演算法的數學邏輯與 Markdown 排版技巧。

---

## 📋 專案簡介
這是一個關於適應性濾波器（Adaptive Filter）的實驗紀錄。我們透過 Markdown 紀錄演算法的初始化與疊代計算過程。

### 🛠 使用工具
| 工具名稱 | 用途 | 熟練度 |
| :--- | :--- | :--- |
| GitHub | 程式碼託管 | ⭐⭐⭐ |
| Markdown | 文件撰寫 | ⭐⭐⭐⭐ |
| Python | 演算法實作 | ⭐⭐⭐ |

---

## 📸 演算法數學模型
以下是你提供的 NLMS 演算法核心公式截圖：

![NLMS Algorithm Flow](https://raw.githubusercontent.com/你的帳號/你的儲存庫名稱/main/image_33e541.png)
*(註：請將上圖網址替換為你上傳到 GitHub 後的圖片原始連結)*

---

## 💡 技術細節解析

### 1. 初始化 (Initialization)
在開始計算前，我們需要初始化權重向量 $\mathbf{\hat{h}}$：
$$\mathbf{\hat{h}}(0) = \text{zeros}(p)$$

### 2. 疊代計算 (Computation)
對於每一個時間點 $n = 0, 1, 2, \dots$，執行以下步驟：

* **輸入向量：** $\mathbf{x}(n) = [x(n), x(n-1), \dots, x(n-p+1)]^T$
* **誤差計算：** $e(n) = d(n) - \mathbf{\hat{h}}^H(n)\mathbf{x}(n)$
* **權重更新：** $$\mathbf{\hat{h}}(n+1) = \mathbf{\hat{h}}(n) + \frac{\mu e^*(n)\mathbf{x}(n)}{\mathbf{x}^H(n)\mathbf{x}(n)}$$

### 3. 工作清單
- [x] 數學公式轉換為 LaTeX
- [x] 圖片上傳至 Repository
- [ ] 撰寫 Python 實作程式碼

### 4. 註腳與參考資料
關於 NLMS 的收斂穩定性，可以參考更深層的學術文獻[^1]。

[^1]: 這是適應性訊號處理（Adaptive Signal Processing）中的經典演算法。

---

## 📬 聯絡資訊
* **作者:** Your Name
* **Email:** `example@mail.com`
* **GitHub:** [點此造訪我的 Profile](https://github.com/)
