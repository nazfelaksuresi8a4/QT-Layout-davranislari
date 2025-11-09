setSizePolicy() fonksiyonu, bir Qt widget’ının (örneğin QPushButton, QLabel, QFrame vs.) layout içinde nasıl davrandığını belirler — yani ekran büyüyüp küçülürken widget’ın boyutunun nasıl değişeceğini kontrol eder.

🔍 Kısa tanım:

setSizePolicy(horizontalPolicy, verticalPolicy)
bu, yatay (horizontal) ve dikey (vertical) yönde widget’ın genişleyip genişlemeyeceğini söyler.


📏 Örnek politikalar:
Qt’de bazı yaygın QSizePolicy.Policy değerleri:
PolitikaAnlamıFixedBoyutu sabittir, büyümez veya küçülmez.MinimumMümkün olduğunca küçük olur, ama daha küçük olamaz.MaximumMümkün olduğunca büyük olur, ama daha büyük olamaz.PreferredVarsayılan (Qt’nin önerdiği boyut).ExpandingAlan varsa genişler. Layout, boş alanı bu widget’a verir.MinimumExpandingMinimumdan başlar ama alan varsa büyür.IgnoredLayout, boyut önerisini dikkate almaz.

📚 Bizim örnekte:
btn.setSizePolicy(QSizePolicy.Policy.Expanding, QSizePolicy.Policy.Expanding)

👉 Bu şu anlama geliyor:


Buton hem yatayda hem dikeyde büyüyebilir.


Layout (QGridLayout) pencereyi büyüttüğünde, butonlar da oranlı olarak genişler.


Böylece tam ekran olduğunda butonlar boşluksuz tüm alanı kaplar.



🎨 Kısa görselleştirme:
PolitikaDavranışFixed🧱 Sabit boyutPreferred🔳 Genellikle orta boyExpanding🔲→🟦 Alan varsa büyürIgnored❌ Layout’a “beni umursama” der

İstersen bu farkı deneyebilirsin — aynı kodda Expanding yerine Fixed koyarsan tam ekranda butonların ortada kaldığını, aralarda boşluk oluştuğunu göreceksin.
