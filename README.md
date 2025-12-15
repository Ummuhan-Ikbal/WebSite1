Bu proje `proje.html` adlı statik bir web sayfasıdır.

Hızlı yükleme adımları (Windows PowerShell):

1) Yerel repo başlatma ve ilk commit:

```powershell
cd "c:\Users\ikbal\Documents\My Web Sites\WebSite1"
git init
git add .
git commit -m "İlk commit: proje dosyaları"
```

2) GitHub'da repo oluşturma (2 seçenek):
- Web arayüzü: https://github.com/new adresine gidip yeni repository oluşturun.
- Komut satırı (GitHub CLI yüklüyse):

```powershell
gh repo create <kullanici-or-repo> --public --source=. --remote=origin --push
```

3) Varsa uzak ekle ve push:

```powershell
git remote add origin https://github.com/<kullanici>/<repo>.git
git branch -M main
git push -u origin main
```

4) Canlı yayın (GitHub Pages):
- GitHub repo sayfasında `Settings` → `Pages` bölümüne gidin.
- `Branch` olarak `main` ve `root` (/) seçin, kaydedin.
- Birkaç dakika sonra site `https://<kullanici>.github.io/<repo>/` adresinde yayında olur.

Opsiyonel: Her push sonrası otomatik deploy için GitHub Actions kullanılabilir; isterseniz örnek workflow ekleyebilirim.

Eğer devam etmemi isterseniz, git init / commit / push komutlarını sizin adınıza buradan çalıştırmamı onaylayın veya adımları kendiniz uygulayın.