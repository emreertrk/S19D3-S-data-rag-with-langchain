# 📚 LangChain ile Retrieval Augmented Generation'a Giriş 🦜🔗

Bu not defterinde LangChain kullanarak Retrieval Augmented Generation'ı nasıl kullanacağınızı öğreneceksiniz.

Kendi belgelerimiz hakkında sorular sormak için bir LLM kullanacağız!

## Çalışma Notları

Bu proje, LangChain ve Gemini ile küçük bir RAG (Retrieval Augmented Generation) akışı kurar. `data/` klasöründeki üç belge kurgusal bir şirketin yönergeleridir, gerçek veri değildir.

1. Klasörde `pyenv local langchain-env` ile LLM ortamını etkinleştir.
2. Proje klasöründe `.env` adlı bir dosya oluştur ve içine `GEMINI_API_KEY=kendi_anahtarın` satırını yaz. `.env` dosyası `.gitignore` içindedir, commit edilmez.
3. `jupyter notebook` ile notebook'u aç ve hücreleri sırayla çalıştır. Vektör veritabanı `chroma_db/` klasörüne yazılır, bu klasör `.gitignore` içindedir.

Akış: belgeleri yükle, parçala (`RecursiveCharacterTextSplitter`), `gemini-embedding-001` ile vektöre çevir, Chroma'ya kaydet, retriever ile ilgili parçaları getirip LLM'e bağlam olarak ver. Gerekçeler ve gözlemler notebook'un sonuç bölümünde.
