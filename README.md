# 🧠 Tic-Tac-Toe AI (Q-Learning ile)

Bu proje, klasik **Tic-Tac-Toe (XOX)** oyununu oynayan ve zamanla kendini geliştiren bir yapay zekâ ajanı içerir. Q-Öğrenme (Q-Learning) algoritması kullanılarak oyun oynama becerisi kazanır.

---

## 🎮 Özellikler

🕹️ İnsan vs. Yapay Zekâ modu
🧠 Q-learning tabanlı kendini geliştiren yapay zekâ
💾 Q-table kaydetme/yükleme (pickle ile)
🔁 Eğitilebilir yapı: X ya da O olarak eğitim
📊 Eğitim sonrası performans çıktıları

---

## 🧠 Eğitim Parametre Önerileri

| Oyuncu | Önerilen discount_factor |
|--------|---------------------------|
| X      | 0.6                       |
| O      | 0.5                       |

---

## 🚀 Kullanım
### 1. Eğitim
```python
from TicTacToe import TicTacToe
from Agent import Agent

game = TicTacToe()
agent = Agent(game, 'X', discount_factor=0.6, episode=100000)
agent.train_brain_x_byrandom()
```

2. İnsanla Oynama
from TicTacToe import TicTacToe
from Agent import Agent

game = TicTacToe()
agent = Agent(game, 'X', discount_factor=0.6, episode=100000)
agent.play_with_human()

---

📁 Dosya Yapısı
├── Agent.py         # Q-learning ajanı
├── TicTacToe.py     # Oyun mekaniği
├── main.py          # Ana çalışma dosyası
├── brainX           # Eğitilmiş beyin (X için)
├── brainO           # Eğitilmiş beyin (O için)

---

📊 Örnek Çıktı
  X     --     O  
 --     X     O  
 --     --     X  
_______________
X is Winner!


📌 Notlar
Q-learning algoritmasında, ajan kendi hatalarından öğrenir. Bu yüzden yüksek sayıda episode ile eğitilmesi önerilir (örn. 100000).

İlk adımlar rastgele atılarak farklı stratejilerin keşfedilmesi sağlanır.

Eğitimden sonra oluşan brainX veya brainO dosyaları ile insan oyunculara karşı oyun oynatılabilir.
