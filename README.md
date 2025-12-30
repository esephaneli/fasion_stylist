# fasion_stylist
# 👗 Myntra AI Style Advisor (Gradio + Multimodal + JSON Schema + Pydantic)

Bu proje, **kullanıcının fotoğrafı + ürün fotoğrafı** ile **stil uyumu ve kombin önerileri** üreten bir AI stil danışmanıdır.  
LLM çıktısı serbest metin yerine **JSON Schema (strict)** ile yapılandırılır ve **Pydantic** ile doğrulanır.

## ✨ Özellikler
- ✅ 2 fotoğrafla Multimodal analiz (user photo + product photo)
- ✅ Dataset bağlamı (Myntra / Fashion dataset)
- (https://www.kaggle.com/datasets/hiteshsuthar101/myntra-fashion-product-dataset)
- ✅ Structured Output: JSON Schema (strict)
- ✅ Pydantic validation (production yaklaşımı)
- ✅ Gradio web arayüzü
- ✅ (Opsiyonel) Hafıza / history bağlamı

## 🧠 Nasıl çalışır?
1. Kullanıcı fotoğrafı + ürün fotoğrafı yüklenir  
2. Dataset’ten örnek satırlar bağlam olarak eklenir  
3. LLM’den **yalnızca JSON** formatında cevap istenir  
4. JSON, **Pydantic** ile doğrulanır ve UI’da gösterilir

## 🧩 Çıktı Formatı (Örnek)
- `verdict`: uygun / kismen_uygun / uygun_degil  
- `reasons`: karar gerekçeleri  
- `size_fit_tips`: fit/kalıp önerileri  
- `color_match_tips`: renk uyumu  
- `outfit_suggestions`: kombin önerileri  
- `confidence`: güven skoru
