🧠 Tic-Tac-Toe AI with Q-Learning
Bu proje, klasik Tic-Tac-Toe (XOX) oyununu oynayan ve öğrenen bir yapay zekâ (AI) ajanı içerir. Q-Öğrenme (Q-Learning) algoritması kullanılarak eğitilen bu ajan, zamanla oyun stratejilerini geliştirerek insan oyunculara karşı daha başarılı hale gelir.

🎮 Özellikler
🕹️ İnsan vs. Yapay Zekâ modu
🧠 Q-learning tabanlı kendini geliştiren yapay zekâ
💾 Q-table kaydetme/yükleme (pickle ile)
🔁 Eğitilebilir yapı: X ya da O olarak eğitim
📊 Eğitim sonrası performans çıktıları

📁 Dosya Yapısı
├── Agent.py         # Q-learning ajanı
├── TicTacToe.py     # Oyun mekaniği
├── main.py          # Oyunu çalıştırmak veya ajanı eğitmek için kullanılan dosya
├── brainX           # Eğitilmiş X oyuncusu (pickle dosyası, eğitim sonrası oluşur)
├── brainO           # Eğitilmiş O oyuncusu (pickle dosyası, eğitim sonrası oluşur)

🧪 Nasıl Çalışır?
1. Ajanı Eğitmek:

from TicTacToe import TicTacToe
from Agent import Agent

game = TicTacToe()
agent = Agent(game, 'X', discount_factor=0.6, episode=100000)
agent.train_brain_x_byrandom()

2. İnsanla Oynamak
agent = Agent(game, 'X')
agent.play_with_human()

🛠️ Parametreler
Parametre	          Açıklama
episode	            Eğitim boyunca oynanacak oyun sayısı
epsilon	            Keşfetme oranı (rastgele hareket olasılığı)
discount_factor	    Q-learning geriye yayılım katsayısı
eps_reduce_factor	  Her 1000 oyunda epsilon’un azaltılma oranı

💡 Tavsiyeler
*discount_factor:
  -X oyuncusu için: 0.6
  -O oyuncusu için: 0.5
*Eğitim süresi olarak en az 100000 episode önerilir.
*İlk hamlede rastgelelik bırakılarak daha çeşitli stratejiler öğrenilir.

📷 Ekran Görüntüsü
 X     --     O  
 --    X     O  
 --    --    X  
_______________
X is Winner!
