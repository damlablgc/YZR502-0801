# YZR502 - Ödev 08 | Mobil Robot Navigasyonu için RL ile Hiperparametre Analizi

## Yazar
Damla | YZR502 Robotik Sistemler ve Algoritmalar

## Proje Özeti
MiniGrid-Empty-8x8 simülasyon ortamında PPO algoritması kullanılarak 4 farklı 
hiperparametre konfigürasyonu test edilmiştir. Çalışma, öğrenme oranı, indirim 
faktörü ve entropi katsayısının ajan performansına etkisini incelemektedir.

## Deney Konfigürasyonları
| Deney | Learning Rate | Gamma | Ek Parametre |
|-------|-------------|-------|--------------|
| Deney 1 (Baseline) | 3e-4 | 0.99 | ent_coef=0.0 |
| Deney 2 | 1e-4 | 0.99 | ent_coef=0.0 |
| Deney 3 | 3e-4 | 0.95 | ent_coef=0.0 |
| Deney 4 (Özel) | 3e-4 | 0.99 | ent_coef=0.1 |

## Sonuçlar
50.000 timestep eğitimde tüm konfigürasyonlar -75.5 eval ödülünde sabit kaldı.
Deney 4'te entropi katsayısı yüksek tutularak keşif odaklı davranış gözlemlendi.

## Dosyalar
- `0801.ipynb` — Google Colab notebook
- `karsilastirma_grafigi.png` — Hiperparametre karşılaştırma grafiği
- `ppo_minigrid_navigation/` — Deney 1 model dosyaları
- `ppo_minigrid_deney2/` — Deney 2 model dosyaları
- `ppo_minigrid_deney3/` — Deney 3 model dosyaları
- `ppo_minigrid_deney4/` — Deney 4 model dosyaları

## Kullanılan Araçlar
- Python 3.12, Google Colab (CPU)
- gymnasium, minigrid, stable-baselines3
- matplotlib, numpy
