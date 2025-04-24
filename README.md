## 🔮 Modelleme & Tahmin Süreci

### 📌 Ne Yaptım, Ne Oldu?

1. **Veri Bölme:**  
   Elimizdeki veri setini **%90 eğitim** ve **%10 test** olacak şekilde böldüm. Bu sayede modelin performansını görmediği veriler üzerinde değerlendirebildim.

2. **Hedef Değişken ve Lag Fonksiyonu:**  
   - Hedef değişkeni (**target**) belirledim.  
   - Veri setine zaman bağımlılığı kazandırmak için **lag fonksiyonu** oluşturarak rastgele **4 adet lag** ekledim. Bu, modelin geçmiş değerlere bakarak geleceği tahmin etmesini sağladı.

3. **Model Kurulumu (CNN):**  
   - Convolutional Neural Network (**CNN**) modelini oluşturup eğitim verisi ile eğittim.  
   - Modeli fonksiyon haline getirerek, gerektiğinde kolayca çağrılabilir ve yeniden kullanılabilir hale getirdim.

4. **Tahmin (Forecast):**  
   - Eğitilen CNN modeline, **hiç görmediği** `y_test` verisi kadar ileriye yönelik tahmin (**forecast**) yaptırdım.  
   - Bu aşamada, model **ileri tarihli tahminler** üreterek gerçek dünya kullanım senaryosuna uygun hale getirildi.

---

### ⚖️ Kritik Noktalar: **Predict vs Forecast**

🔍 **Predict:**  
Modelin eğitildiği veriler ile **aynı zaman aralığındaki** değerleri tahmin etmesidir. Test verisi (`y_test`) kullanılarak klasik doğrulama yapılır ve MSE, RMSE gibi metriklerle performans ölçülür.

🔮 **Forecast:**  
Modelin **hiç görmediği gelecekteki** verileri tahmin etmesidir. Bu durumda model, geçmiş değerlerden yola çıkarak **ileri tarihler** için tahmin
