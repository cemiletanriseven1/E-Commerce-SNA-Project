# 📊 Amazon Ürün Öneri Ağının Sosyal Ağ Analizi (SNA)
### 🔗 *Social Network Analysis of Amazon Product Recommendation Network*

Bu proje, Stanford Üniversitesi (**SNAP**) Amazon metadata veri seti kullanılarak ürünlerin öneri ilişkilerini (Co-purchase) ağ teorisi ve gelişmiş **Sosyal Ağ Analizi (SNA)** yöntemleriyle incelemektedir.

---

## 📖 Proje Özeti (Project Abstract)

Proje kapsamında **721.342 ürün (düğüm)** ve **1.788.725 öneri ilişkisi (kenar)** içeren devasa bir e-ticaret veri seti modellenmiştir. *"Müşteriler bu ürünü alanlar bunları da aldı"* mekanizmasının mimarisi çözülerek elde edilen soyut ağ metrikleri stratejik ticari içgörülere (business insights) dönüştürülmüştür.

---

🚀 Öne Çıkan Teknik Bulgular (Key Findings)

1. 📈 Ölçekten Bağımsız (Scale-Free) Ağ Topolojisi
Yapılan derece dağılım analizi sonucunda (Log-Log ölçekte), ağın bir Power-Law (Güç Yasası) doğrusu izlediği saptanmıştır. Ağda binlerce bağlantıya sahip çok az sayıda "Süper-Hub" (kült ürünler) bulunurken, ürünlerin ezici çoğunluğu çok az bağlantıya sahiptir.
2. 🧮 SalesRank Tabanlı Ağırlıklı PageRank
Standart PageRank algoritması, Amazon’un gerçek dünya satış performans verisi olan SalesRank ile harmanlanarak yeniden ağırlıklandırılmıştır. Sadece popüler olan değil, ticari hacmiyle de sisteme yön veren "gerçek otoriteler" filtrelenmiş ve en merkezi düğümlerde %83'e varan bir PageRank LIFT (skor artışı) yakalanmıştır.
3. 🎯 Kusursuz Topluluk Ayrışımı (Modularity: 0.952)
Louvain algoritmasıyla yapılan topluluk tespitinde 0.952 Modularity skoru elde edilmiştir. Bu değer; Amazon'da kitap alanların kitap, DVD alanların DVD dünyasında kaldığını, kategorilerin kendi içlerine son derece kapalı ve yoğun "Yankı Odaları" (Echo Chambers) oluşturduğunu ispatlar.
🛡️ 4. Ağ Dayanıklılığı ve Kırılganlık (Robustness Analizi)
Sistemin kriz anlerindeki davranışı simüle edilmiştir:
Rastgele Kaldırma: Ağdan rastgele 50 ürün silindiğinde En Büyük Bileşen (LCC) boyutumun neredeyse hiç değişmediği (%5.2 kayıp) görülmüştür.
Hedefli Saldırı: En yüksek dereceye sahip 50 kritik hub ürün silindiğinde ise ağın ana gövdesi %87.36 oranında parçalanarak çökmüştür.


🛠️ Kullanılan Teknolojiler (Tech Stack)
Dil: Python 3.x
Kütüphaneler: networkx, pandas, numpy, matplotlib, seaborn
Görselleştirme: Gephi (Top-1000 Alt Ağ haritası ForceAtlas2 layout'u ile çizilmiştir)
💡 Ticari ve Stratejik Öneriler (Business Insights)
Stok Güvencesi: Dayanıklılık analizinde tespit edilen o 50 kritik "Hub" ürünün stoğu asla bitirilmemelidir; aksi takdirde öneri motoru işlevini yitirir ve çapraz satışlar çöker.
Akıllı Paketleme (Bundle): Komşuluk Matrisi Isı Haritasında köşegen boyunca kümelenen parlak bölgeler, birlikte sepet indirimi (bundle) kurgulamak için doğrudan ürün eşleşmeleri sunmaktadır.
Reklam Optimizasyonu: Reklam bütçeleri köprü (High Betweenness) görevi gören ürünlere aktarılarak kullanıcıların farklı kategorilere sızması sağlanmalıdır.


Bu proje Sosyal Ağ Analizi dersi final ödevi kapsamında Cemilenur Tanrıseven ve Burak Enes Kırış tarafından geliştirilmiştir.
