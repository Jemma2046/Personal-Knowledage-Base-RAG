## 1. Ollama安裝指引 (Installation Guide)
Ollama 支援 Windows、macOS 與 Linux 三大平台，以下基於Windows 展示安裝步驟和如何開始使用 LLM 的相關指令。

### Windows 安裝
1. 於官網 https://ollama.com/download/windows 下載 `OllamaSetup.exe` 安裝包。
2. 雙擊運行並點擊 **Install**。
3. 按指示安裝完成後，Ollama 便會在後台常駐運行。之後可以透過命令列（CLI）進行操作，第一步運行以下指令便可啟動Ollama服務！
>>> ollama serve

### 如何在Ollama 開始使用 LLM (Getting Started)
1. 首先可於官網 https://ollama.com/search 尋找想跑的模型。
2. 以下以安裝Gemma4:e4b作為例子，運行以下指令便可下載模型
>>> ollama pull gemma4:e4b
3. 也可直接以跑模型的指令，直接下載模型並一併跑模型
>>> ollama run gemma4:e4b
4. 當命令列（CLI）出現 >>> 提示符後，即可直接輸入文字與 AI 對話！

### 常用命令速查表
指令
說明
ollama list
查看本地已下載的所有模型與大小
ollama pull <模型名>
僅下載模型，不立即執行對話
ollama rm <模型名>
刪除本地的某個模型以釋放硬碟空間
ollama show <模型名>
查看該模型的詳細資訊（如架構、參數）
ollama ps
顯示正在運行的模型列表
