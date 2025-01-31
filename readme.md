# DeepSeek R1 (1.5) ile Localde RAG

Bu proje Streamlit tabanlı bir Retrieval-Augmented Generation (RAG) basit bir uygulaması. 
Sistem, belgelerden ilgili bölümleri alır ve local DeepSeek R1 modeli ile yanıt verir.

## Proje Yapısı

```
.
├── app.py          #  Ana Streamlit uygulaması
├── rag.py          #  RAG
├── requirements.txt # Bağımlılık listesi
```
## Kurulum
### Gereksinimler

Aşağıdaki bileşenlerin sisteminizde kurulu olduğundan emin olun:
- Python 3.9+
- pip
- Ollama (local DeepSeek R1 modelini çalıştırmak için)
- Streamlit

### Bağımlılıkları Yükleme

```bash
# Depoyu klonlayın
git clone https://github.com/bcemsayilar/deepseekr1_local
cd deepseekr1_local

# Sanal ortam oluşturun (isteğe bağlı ancak önerilir)
python3 -m venv venv
source venv/bin/activate  # Mac/Linux için
venv\Scripts\activate  # Windows için

# Gerekli Python paketlerini yükleyin
pip install -r requirements.txt
```

### Mac İçin Kurulum Kılavuzu
Eğer macOS kullanıyorsanız, DeepSeek modellerini çalıştırmak için `Ollama`'nın yüklü olduğundan emin olun:

```bash
brew install ollama  # Ollama'yı yükleyin
ollama pull deepseek-r1:1.5b  # Gerekli modeli indirin
ollama run deepseek-r1:1.5b
```

## Uygulamayı localde Çalıştırma

Paketleri yükledikten sonra, uygulamayı Streamlit ile başlatabilirsiniz:

```bash
streamlit run App/app.py
```

Bu komut local bir web sunucusu başlatacak ve tarayıcıda kullanıcı arayüzüne erişmenizi sağlayacaktır.

## Kullanım

1. **PDF Yükleyin:** PDF dosyanızı sürükleyip bırakın veya seçerek yükleyin.
2. **Soru Sorun:** Giriş kutusuna bir soru yazın.
3. **Yanıt Alın:** Sistem, belgeden ilgili bölümleri alır ve kısa yanıtlar sunar.

## Katkıda Bulunma

Katkılarınızı bekliyoruz! Hata bildirmek veya geliştirmeler için pull request atabilirsiniz.

## Lisans

Bu proje, MIT Lisansı ile lisanslanmıştır. Daha fazla bilgi için LICENSE dosyasına bakabilirsiniz.

