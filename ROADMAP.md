# Fullstack Yol Haritası v2

Hedef: **SFMC geçmişinden, TypeScript tabanlı fullstack geliştirici olarak işe girmek** (Türkiye ve yurtdışı).
Yol haritasının sonunda elinde şunlar olacak: **canlı bir portföy sitesi, 3 CV projesi, 2 CV, düzenlenmiş GitHub/LinkedIn profili ve mülakata hazır bir anlatı.**

---

## 0. Bu dosya nasıl kullanılır

1. Repo kökünde `ROADMAP.md` olarak dursun. `PROGRESS.md`'yi (Bölüm 11) yanına koy.
2. Copilot kuralları ayrı dosyada: `.github/copilot-instructions.md` (kısa tutuldu ki kurallar atlanmasın). İçeriği `copilot-instructions-v2.md` dosyasından al.
3. Her hafta başında bu dosyada o haftanın satırına bak. Her hafta sonunda `PROGRESS.md`'yi doldur.
4. Bu dosya bir taahhüt değil, **hipotez**. Veri (kapı testleri, başvuru sonuçları) farklı diyorsa Bölüm 9'daki kurallara göre plan değişir.

---

## 1. Başlangıç noktası (planın dayandığı varsayımlar)

| Konu | Durum |
|---|---|
| Geçmiş | SFMC geliştiricisi (SQL, SSJS, AMPscript, e-posta/CloudPage HTML-CSS, REST/SOAP API kullanımı) |
| Fullstack | Sıfır. Modern JS/TS, framework, backend mimarisi, test, dağıtım yok |
| HTML | Eksik yok (portföy sitesiyle denetlenecek) |
| CSS | İyi ama uzman değil |
| SQL | Güçlü yanın |
| JavaScript | Gerçek boşluk. SSJS eski bir sürüm (ES3 seviyesi) |
| İngilizce | B2. Mülakatta darboğaz olabilir |
| Çalışma durumu | Şu an çalışmıyor, gelir hattı acil |
| Zaman | Varsayılan **haftada 15 saat** (Bölüm 10'da 25 ve 35 saat versiyonları) |
| Asistan | GitHub Copilot, öğretmen modunda |
| Hedef pazar | Türkiye + yurtdışı (uzaktan dahil) |

**Kendi geçim payını (kaç ay) `PROGRESS.md`'nin başına yaz.** Bölüm 9'daki kararlar buna bağlı.

---

## 2. Kesinleşen kararlar

1. **Yığın:** TypeScript, React, Next.js, Node.js (Express, sonra NestJS), PostgreSQL, Drizzle ORM. Backend Node.js olacak, .NET Katman 3'te koşullu.
2. **İki paralel hat:**
   - **Hat A (Gelir):** SFMC/MarTech başvuruları **1. haftadan** başlar.
   - **Hat B (Öğrenme):** Fullstack roadmap.
3. **Portföy sitesi iki kez yapılır:** v1 (Hafta 2–7, saf HTML/CSS/JS, CSS denetimi ve ilk vitrin), v2 (Hafta 41, Next.js + Tailwind, vaka çalışmalarıyla).
4. **3 CV projesi:**
   - **CV-1:** Frontend uygulaması (Hafta 8–16).
   - **CV-2:** **Harcama Takibi**, fullstack amiral gemisi (Hafta 17–34). Banka API'si yerine CSV içe aktarma ve demo verisi kullanılır.
   - **CV-3:** **Onay Yönetimi (Consent Manager)**, SFMC alan bilginle farklılaşan proje (Hafta 35–40).
5. **AI kullanımı evreli** (Bölüm 4.6): Hafta 1–26 katı öğretmen modu, Hafta 27–34 yarı serbest, Hafta 35'ten itibaren serbest ama zorunlu inceleme.
6. **Kapı testi olmadan sonraki faza geçilmez** (Bölüm 4.8).

---

## 3. Öğrenilecek teknoloji listesi (final v2)

**Katmanlar:** K1 = şart (bunlar olmadan işe girilmez), K2 = seni öne çıkarır, K3 = sonra veya koşullu.

| Kategori | Teknoloji | Katman | Faz |
|---|---|---|---|
| **Dil** | JavaScript ES6+ | K1 | F1 |
| | TypeScript (`strict`) | K1 | F2 |
| **Frontend** | HTML5 semantik | K1 | F1 (denetim) |
| | CSS: Flexbox, Grid, değişkenler, responsive | K1 | F1 |
| | React + Vite | K1 | F2 |
| | React Router | K1 | F2 |
| | TanStack Query | K2 | F2 |
| | React Hook Form + Zod | K2 | F2 |
| | Zustand (kısa) | K2 | F2 |
| | Erişilebilirlik (WCAG temelleri) | K2 | F2–F4 |
| | Next.js (App Router, Server Components, Server Actions) | K2 | F4 |
| | Tailwind CSS + shadcn/ui | K2 | F4 |
| | Redux Toolkit | K3 | ilan taramasında çıkarsa |
| **Backend** | Node.js | K1 | F3 |
| | Express, REST tasarımı | K1 | F3 |
| | Zod ile sunucu doğrulaması | K1 | F3 |
| | Session tabanlı auth (HttpOnly çerez) + argon2 | K1 | F3 |
| | JWT (kavram olarak) | K1 | F3 |
| | NestJS (Express'ten sonra) | K2 | F5 |
| **Veritabanı** | PostgreSQL | K1 | F3 |
| | SQL: JOIN, GROUP BY, index, `EXPLAIN`, transaction | K1 | F3 |
| | Drizzle ORM + migration | K1 | F3 |
| | Prisma (yalnızca tanı), Redis | K3 | — |
| **Güvenlik** | OWASP Top 10 | K1 | F3–F4 |
| | Yetkilendirme: RBAC, IDOR, Server Actions'ta oturum kontrolü | K1 | F3–F4 |
| **Test** | Vitest + React Testing Library | K1 | F2 |
| | Supertest (backend entegrasyon) | K1 | F3 |
| | Playwright (E2E) | K2 | F4 |
| **Araçlar / DevOps** | Terminal, Git/GitHub (branch, PR) | K1 | F0 |
| | HTTP temelleri + tarayıcı DevTools | K1 | F1 |
| | Vercel, Render, Neon, ortam değişkenleri | K1 | F1–F3 |
| | Docker + Compose | K2 | F4 |
| | GitHub Actions (CI) | K2 | F4 |
| | AWS temelleri, Turborepo | K3 | — |
| **Beceriler** | README ve teknik yazım | K1 | hepsi |
| | Projeyi 3 dakikada İngilizce anlatma | K1 | F4–F5 |
| | AI'nın yazdığı kodu inceleme ve test etme | K2 | F4–F5 |
| | LeetCode Easy (~50 soru) | K2 | F3–F5 |
| | Sistem tasarımı temelleri | K2 | F5 |

**Şimdilik yok:** Coolify/Hetzner ile self-hosting, Fastify, Hono, MCP, Cursor/Windsurf (Faz 4'e kadar), .NET (K3, koşullu).

**Katman kuralı:** K1 sağlam değilken K2'ye geçme. K2 için zaman ayırmadan önce K1 kapı testini geç.

**Aylık piyasa taraması (30 dk):** Her ayın ilk cumartesisi Kariyer.net/LinkedIn'de "junior full stack" ve "react" ile 30 ilan aç. Hangi backend, veritabanı, araç geçiyor tabloya say. Bir teknoloji 30 ilanın en az 10'unda çıkıyorsa ve listede yoksa, öğretmene (bana) getir, planı birlikte değiştirelim.

---

## 4. Öğrenme sistemi (bu roadmap'in kalbi)

Buradaki her yöntem, öğrenme biliminde tutarlı sonuç veren tekniklerden seçildi. Roadmap'in teknolojisi kadar bu sistem de önemli. Sistemi uygulamadan teknolojiyi bitirmek "izledim, biliyorum" yanılsaması yaratır.

### 4.1 Ana ilkeler

| İlke | Ne demek | Bu planda nerede |
|---|---|---|
| **Aktif hatırlama** (retrieval practice) | Bilgiyi tekrar okumak yerine **kaynağa bakmadan hatırlamaya çalış** | Kavram kartları, kapanış soruları, kapı testleri |
| **Aralıklı tekrar** (spaced repetition) | Aynı konuyu 1, 3, 7, 14, 30 gün sonra tekrar et | Bölüm 4.7 |
| **Karışık pratik** (interleaving) | Bir konuyu ard arda tekrarlamak yerine eski konularla karıştır | Her hafta geçmiş haftalardan 1 mini görev |
| **Önce çözümlü örnek, sonra kademeli çekilme** | Yeni konuda çalışan örneği oku, sonra boşluk doldur, sonra sıfırdan yaz | 4.4 döngüsü |
| **PRIMM** (Tahmin et, Çalıştır, İncele, Değiştir, Yap) | Kodu çalıştırmadan önce ne yapacağını tahmin et | 4.4 döngüsü |
| **Üreterek öğrenme** | Öğrenmenin çoğu **kendi projeni yazarken** olur | Haftalık "İnşa et" bloğu (~6 saat) |
| **Sıfırdan yeniden yazma** | Bir şeyi bir kez yaptıktan 1 hafta sonra kaynaksız yeniden yaz | Kapı testleri, portföy v2 |
| **Anlatarak öğrenme** (teach-back) | Konuyu 5 cümleyle kendi kelimenle yaz | Her oturum sonu |
| **Hata günlüğü** | Aynı hatayı iki kez yapmamak için kaydet | `PROGRESS.md` |
| **Ustalık odaklı ilerleme** (mastery) | Zaman dolunca değil, **kriteri geçince** ilerle | Kapı testleri |
| **Dikey dilim (vertical slice)** | Projeyi katman katman değil, çalışan küçük özelliklerle geliştir | Bölüm 8 |

### 4.2 Haftalık zaman bütçesi (15 saat)

| Blok | Saat | İçerik |
|---|---|---|
| **Öğren** | 5 | Doküman/müfredat okuma, örnek çalıştırma (Hafta 1–16'da 6, mülakat bloğu henüz yok) |
| **İnşa et** | 6 | Proje kodlama (asıl öğrenme burada) |
| **Tekrar** | 1,5 | Kartlar, hata günlüğü, eski konulardan mini görev |
| **Gelir hattı** | 1,5 | Başvuru, CV, ağ kurma (Bölüm 6) |
| **Mülakat / İngilizce** | 1 | Hafta 17'den itibaren (Bölüm 7) |

**Örnek hafta:** Pzt 2 s Öğren · Sal 2 s İnşa · Çar 1,5 s Gelir + Tekrar · Per 2 s İnşa · Cum 2 s İnşa + Demo · Cmt 4 s Öğren/İnşa · Paz 1,5 s Tekrar + Plan.

**Hafta 1 istisnası:** Kurulum ve CV işi yoğun. Gelir hattına 6 saat, kalanı Faz 0'a ver.

**Sınırlar:** Tek oturum en fazla 3 saat. Haftada en az 1 tam dinlenme günü. Yorgunken zorlama, ertesi gün kısa oturum yap.

### 4.3 Bir çalışma oturumunun yapısı (90 dakika)

1. **5 dk:** Hedefi tek cümleye yaz ("Bugün: `map` ve `filter`'ı kaynaksız kullanacağım").
2. **10 dk:** Bugünün tekrar kartları (bakmadan cevapla, sonra kontrol et).
3. **50 dk:** Odaklı çalışma (25 dk çalış, 5 dk mola, tekrar). Telefon uzakta.
4. **10 dk:** Teach-back: 5 cümleyle bugün ne öğrendin yaz.
5. **5 dk:** `PROGRESS.md`'yi güncelle, yarın için tek mini görev seç.

### 4.4 Yeni konu döngüsü (her yeni konuda)

1. **Tahmin et:** Konunun adını gördüğünde ne olduğunu kendi kelimenle 2 cümleyle yaz (yanlış olabilir, sorun değil).
2. **Oku:** Ana kaynaktan 20–30 dk oku. Not alırken kopyalama, özetle.
3. **Çalıştır ve değiştir:** Kaynaktaki örneği çalıştır. Önce **ne çıkacağını tahmin et**, sonra çalıştır. Sonra bir şeyi değiştirip ne olacağını tahmin et.
4. **Kendin yaz:** Örneğe bakmadan aynı şeyi sıfırdan yaz.
5. **Kır:** Kodu bilerek boz. Hata mesajını oku, neden bozulduğunu açıkla.
6. **Anlat:** 5 cümlelik teach-back yaz.
7. **Kart üret:** 1–3 kavram kartı yaz (Bölüm 11'deki formatta).

**Kural:** Bir eğitim videosu izlediysen, **aynı gün** ondan bağımsız kendi varyasyonunu yaz. Bunu yapmadan yeni videoya geçme ("tutorial cehennemi" bu şekilde başlar).

### 4.5 Tıkanma protokolü (Copilot ile)

Takıldığında sırayla:

1. **Netleştir:** Ne yapmaya çalışıyorsun, ne bekliyorsun, ne oluyor? Tek cümleyle yaz.
2. **Hata mesajını oku:** Hangi dosya, hangi satır, hata türü. Kendi kodunun ilk satırını bul.
3. **25 dakika araştır:** Somut arama terimi, resmi doküman bölümü (MDN, react.dev, TypeScript Handbook, PostgreSQL dokümanı).
4. **Copilot'a şu formatla sor:** "Ne aradım / ne buldum / ne denedim / nerede takılıyorum."
5. **İpucu al:** Copilot analoji, sözde kod veya soru verir, çözümü vermez.
6. **Yürüyüş (son çare):** En az 30 dakika araştırdıktan sonra "ÇÖZÜMÜ ANLAT (araştırdım, denedim)" yaz. Copilot adım adım anlatır. **Ardından çözümü bakmadan kendin yeniden yaz.**
7. Takıldığın noktayı ve öğrendiğini hata günlüğüne yaz.

### 4.6 AI kullanımı evreleri

| Evre | Hafta | Kural |
|---|---|---|
| **1: Öğretmen** | 1–26 | Copilot **Ask** modunda. Satır içi tamamlama **kapalı**. Kod yazmaz, açıklar, sorar, inceler. |
| **2: Yarı serbest** | 27–34 | Satır içi açık olabilir. **Önce sen yaz**, sonra AI'a inceleme yaptır. Önerilen her satırı okumadan kabul etme. Testleri sen yaz. |
| **3: Serbest ama denetimli** | 35+ | AI ile hızlı geliştir. Her PR'da **AI kod inceleme listesi** (aşağıda) zorunlu. |

**AI kod inceleme listesi:** ✅ Girdi doğrulanıyor mu? ✅ Yetki kontrolü sunucuda mı? ✅ Gizli anahtar koda gömülmüş mü? ✅ SQL parametreli mi? ✅ Hata durumları ele alınmış mı? ✅ Test yazıldı mı? ✅ Neden böyle çalıştığını açıklayabiliyor muyum?

Bu evreler bilinçli: piyasa AI'yı kullanan ama ona bağımlı olmayan, çıktısını doğrulayabilen kişileri arıyor. Temeli kendin kurmazsan doğrulama yeteneğin olmaz.

### 4.7 Tekrar sistemi

- **Kart formatı:** Ön yüz: soru veya "şunu kaynaksız yaz". Arka yüz: kısa cevap + 1 örnek. Kart başına tek kavram.
- **Aralık:** Yeni kart 1, 3, 7, 14, 30 gün sonra tekrar. Bilemediğin kart başa döner.
- **Araç:** Anki veya `PROGRESS.md` içindeki liste. Copilot'tan haftada bir "bu haftanın 10 sorusunu sor" isteyebilirsin (Copilot soru sorar, cevabı hemen söylemez).
- **Karışık pratik:** Her hafta önceki fazlardan bir mini görev (örn. Faz 3'teyken Faz 1'den `fetch` ile bir küçük görev).

### 4.8 Kapı testleri (ustalık ölçütü)

- Her fazın sonunda **kaynaksız** (doküman açık, AI kapalı) bir test yapılır.
- Kriter listesinin **en az %80'i** geçilmeli. Geçilmezse ilgili haftayı tekrar et, **en fazla 1 hafta ek süre**, sonra tekrar dene.
- Kapı testini geçemesen bile Hat A (gelir) durmaz.

### 4.9 Kaçınılacak tuzaklar

1. **Tutorial cehennemi:** Video izleyip kopyalamak. Çare: 4.4'teki "kendi varyasyonun" kuralı.
2. **Çok kaynak:** Fazda tek ana kaynak, referans olarak resmi dokümanlar.
3. **Faz atlamak:** Kapı testsiz ilerlemek.
4. **Erken framework:** JavaScript sağlam değilken React.
5. **Mükemmeliyetçilik:** Portföye haftalar harcamak. Süre kısıtları var.
6. **AI'ya bağımlılık:** Çözümü kopyalamak.
7. **Test ve güvenliği "sonra" bırakmak:** İşverenin baktığı şeyler.
8. **Yalnız çalışmak:** Haftalık demo (Cuma) ve GitHub commit'leri seni hesap verebilir tutar.
9. **Sessizce ilerlememek:** İki hafta üst üste plan gerisindeysen Bölüm 9'daki kurala bak.

---

## 5. Roadmap: hafta hafta

**Ana kaynak seçimi (her fazda tek):** Bölüm 12'ye bak.
**Her hafta:** Cuma günü 5 dakikalık demo (ekran kaydı veya README notu) + `PROGRESS.md` güncellemesi.

### FAZ 0: Hazırlık ve sistem kurulumu (Hafta 1)

**Amaç:** Çalışma ortamı, Git alışkanlığı, öğrenme sisteminin kurulması, gelir hattının başlatılması.

| Görev | Detay |
|---|---|
| Kurulum | VS Code, Node.js (LTS), Git, GitHub hesabı, Copilot (Ask modu, satır içi kapalı) |
| Terminal | `pwd`, `ls`, `cd`, `mkdir`, `touch`, `cp`, `mv`, `rm` (dikkatli), yol kavramı |
| Git | çalışma dizini, staging, commit, branch, remote. `init`, `status`, `add`, `commit`, `log`, `push`, `pull`, `clone`, `switch` |
| `.gitignore` | `node_modules` ve `.env` neden asla commit'lenmez |
| Repo | `learning-hub` reposu: `ROADMAP.md`, `PROGRESS.md`, `.github/copilot-instructions.md` |
| Copilot testi | "Staging alanı nedir? Sadece cevabı ver." diye sor. Hemen cevap veriyorsa talimat dosyası yüklenmemiş demektir |
| **Hat A başlangıcı** | SFMC/MarTech CV'si, LinkedIn başlığı, ilk 10 başvuru, 5 referans mesajı (Bölüm 6) |

**Kapı testi (30 dk):** Boş klasörden repo aç, branch oluştur, değişiklik yap, birleştir, GitHub'a it. `.env` dosyasını commit'ten dışarıda tut.

---

### FAZ 1: Web temelleri, JavaScript (Hafta 2–7)

**Amaç:** JavaScript'i **framework olmadan** öğrenmek. HTML/CSS denetlenir, JavaScript sıfırdan öğrenilir.
**Ana kaynak:** javascript.info (JS için), MDN (referans).

| Hafta | Konu | İnşa et | Kapanış soruları |
|---|---|---|---|
| **2** | **CSS denetimi + portföy v1:** Flexbox, Grid, responsive, özgüllük, CSS değişkenleri | **Portföy v1** (tek sayfa, sıfırdan, mobil uyumlu). Takıldığın CSS konularını çalış | Özgüllük nedir? Flexbox ne zaman, Grid ne zaman? `rem` neden `px`'ten iyi? |
| **3** | **JS temel:** `let/const`, tipler, `==` vs `===`, truthy/falsy, kontrol akışı, fonksiyonlar, scope, closure girişi | Konsolda 10 küçük fonksiyon (FizzBuzz, string işleme, sayı tahmin mantığı) | `let` ile `const` farkı? Closure nedir (kendi cümlenle)? |
| **4** | **JS veri yapıları:** array/object, `map/filter/reduce/find/some/every/sort`, destructuring, spread/rest, JSON, referans vs değer | Bir ürün/öğrenci listesini dönüştüren fonksiyonlar (kendi test verinle) | `map` ile `forEach` farkı? `sort` diziyi değiştirir mi? Yüzeysel kopya neden tuzak? |
| **5** | **DOM ve olaylar:** `querySelector`, olay dinleyicileri, bubbling, olay delegasyonu, form işleme, `localStorage`, `innerHTML` riski (XSS'e giriş) | **Hesap makinesi**, ardından **to-do listesi** (ekle, sil, işaretle, kalıcı) | `innerHTML` neden tehlikeli? Olay delegasyonu ne işe yarar? |
| **6** | **Asenkron JS ve HTTP:** olay döngüsü sezgisi, callback → Promise → `async/await`, `fetch`, `response.ok`, HTTP metodları ve durum kodları, header'lar, DevTools Network sekmesi | **Herkese açık bir API'den** veri çeken sayfa (yükleniyor ve hata durumlarıyla) | `fetch` 404'te hata fırlatır mı? `await` neyi bekler? |
| **7** | **Modüller, araçlar, hata ayıklama:** ES modülleri, npm, `package.json`, Vite'a giriş, debugger/breakpoint, `console` ötesi hata ayıklama | **Portföy v1'i canlıya al** (Vercel veya benzeri). Faz 1 miniprojelerini portföye ekle | Bir hatayı debugger ile nasıl adım adım takip edersin? |

**Kapı testi (90 dk, kaynaksız, AI kapalı, doküman açık):**
1. Boş dosyadan responsive bir kart listesi sayfası yap.
2. Bir API'den `fetch` ile veri çek, yükleniyor/hata/başarılı durumlarını göster.
3. 5 JS problemi çöz (`map/filter/reduce`, closure, referans).
4. 5 kavram sorusunu yaz veya sesli anlat.

**Çıktı:** Portföy v1 (canlı), 3 mini proje (hesap makinesi, to-do, API sayfası).

---

### FAZ 2: TypeScript ve React (Hafta 8–16)

**Amaç:** Tip güvenli JavaScript ve bileşen tabanlı arayüz, ardından **CV-1**.
**Ana kaynaklar:** TypeScript Handbook (resmi), react.dev "Learn" (resmi).

| Hafta | Konu | İnşa et | Kapanış soruları |
|---|---|---|---|
| **8** | **TypeScript I:** tipler, inference, `interface` vs `type`, union, narrowing | Faz 1'deki to-do'yu TypeScript'e çevir | Union nedir? Narrowing nasıl çalışır? |
| **9** | **TypeScript II:** generic girişi, `tsconfig` (`strict` neden açık), `any` vs `unknown`, utility tipler | API sayfanı TS'e çevir, tipleri API yanıtına göre yaz | `any` neden kaçınılır? Generic ne işe yarar? |
| **10** | **React I:** Vite kurulumu, JSX, bileşen, props, koşullu render, liste render (`key`) | Statik ürün kartı listesi | `key` neden gerekli? Props değişir mi? |
| **11** | **React II:** `useState`, immutability, controlled form, lifting state up | **Görev listesi** (React + TS) | State güncellenince ne olur? Neden mutate etmeyiz? |
| **12** | **React III:** `useEffect`, bağımlılık dizisi, cleanup, veri çekme, yükleniyor/hata durumları, React Router | **CV-1 başlangıç:** GitHub repo arama/film keşif uygulaması iskeleti (çok sayfa, detay sayfası) | Bağımlılık dizisi boşsa ne olur? Cleanup ne zaman çalışır? |
| **13** | **TanStack Query** (neden `fetch + useEffect` yetmez), Context vs Zustand (kısa) | CV-1'i TanStack Query'ye taşı | Cache neden önemli? Sunucu durumu ile istemci durumu farkı? |
| **14** | **Formlar ve erişilebilirlik:** React Hook Form + Zod, hata mesajları, klavye erişimi, `label`, focus yönetimi | CV-1'e filtre/arama formu, erişilebilir hale getir | Zod şeması neden tek doğruluk kaynağı olabilir? |
| **15** | **Test I:** Vitest + React Testing Library ("kullanıcı ne görür") | CV-1 için 5–8 anlamlı test | Davranışı mı, iç yapıyı mı test edersin, neden? |
| **16** | **CV-1'i bitir:** dağıtım (Vercel), README, ekran görüntüleri, Lighthouse kontrolü | **CV-1 canlı** + README | Bu projede hangi kararı neden verdin? |

**Kapı testi (3 saat, kaynaksız, AI kapalı):** Küçük bir React + TypeScript uygulaması yaz: liste + arama + detay sayfası + TanStack Query ile veri çekme + 2 test. Ardından 5 kavram sorusu (props/state, `useEffect`, controlled form, `key`, cache).

**Çıktı:** **CV-1** (canlı, testli, README'li).

**Faz 2 sonu kontrolü:** Bölüm 9 kararları.

---

### FAZ 3: Backend, veritabanı, güvenlik (Hafta 17–26)

**Amaç:** Kimlik doğrulamalı, güvenlik bilinciyle yazılmış bir REST API. **CV-2'nin backend'i.**
**Ana kaynaklar:** Node.js ve Express dokümanları, PostgreSQL dokümanı, Drizzle dokümanı, OWASP Top 10, PortSwigger Web Security Academy (güvenlik laboratuvarları).
**Paralel hat başlar:** Mülakat hazırlığı (Bölüm 7).

**CV-2 kapsamı (Harcama Takibi):** Kullanıcılar kayıt olur, harcama ekler, kategorilere ayırır, **CSV ile banka ekstresi yükler**, aylık özet ve filtre görür. Demo verisi hazır olur (işveren gerçek hesap girmeden dener).

| Hafta | Konu | İnşa et | Kapanış soruları |
|---|---|---|---|
| **17** | **Node ve Express giriş:** HTTP sunucusu kavramı, route, istek/yanıt, `process.env` | Bellek içi verili basit API | Middleware nedir? İstek yaşam döngüsü? |
| **18** | **Express derin + REST:** middleware, hata yönetimi, **Zod ile doğrulama**, doğru durum kodları, sayfalama | API'yi REST kurallarına göre düzenle, tutarlı hata formatı | PUT ile PATCH farkı? İdempotent ne demek? |
| **19** | **PostgreSQL ve veri modelleme:** kurulum, şema, veri tipleri, birincil/yabancı anahtar, normalizasyon, ilişkiler | **CV-2 ERD** (users, categories, transactions, imports). Kâğıt/çizim yeter | Neden ara tablo? Normalizasyon neyi çözer? |
| **20** | **İleri SQL:** JOIN türleri, `GROUP BY`, `HAVING`, alt sorgu, index, `EXPLAIN`, transaction | Ham SQL ile aylık özet, kategori toplamı sorguları | Index ne zaman yavaşlatır? Transaction neden? |
| **21** | **Drizzle ORM ve migration:** şema tanımı, sorgu, migration, seed | ERD'yi Drizzle şemasına çevir, migration ve seed çalıştır | ORM ne zaman yardım eder, ne zaman engel olur? |
| **22** | **Auth I:** şifre hash'leme (argon2), session, çerez özellikleri (`HttpOnly`, `Secure`, `SameSite`) | Kayıt, giriş, çıkış akışı | Hash ile şifreleme farkı? Session ile JWT farkı? |
| **23** | **Auth II ve yetkilendirme:** kimlik doğrulama vs yetkilendirme, sahiplik kontrolü, RBAC, **IDOR**, OWASP Top 10 | **Güvenlik laboratuvarı:** bilerek bir IDOR ve bir SQL injection açığı oluştur, sonra kapat | Bir kullanıcı başkasının harcamasını nasıl görebilirdi? |
| **24** | **Backend testleri ve sertleştirme:** Supertest, test veritabanı, rate limiting, CORS, gizli anahtar yönetimi, yapılandırılmış log | Auth ve harcama uçları için entegrasyon testleri | CORS neyi engeller, neyi engellemez? |
| **25** | **İş mantığı:** CSV içe aktarma, ekstre ayrıştırma, otomatik kategorilendirme kuralları, hata toleransı | CSV yükleme endpoint'i (10.000 satır testi, hatalı satır raporu) | Yarım kalmış bir import'u nasıl geri alırsın? |
| **26** | **Dağıtım ve dokümantasyon:** Render + Neon dağıtımı, ortam değişkenleri, API dokümantasyonu | **CV-2 API canlı** + README taslağı | Gizli anahtarlar nerede tutulur? |

**Kapı testi (4 saat, doküman açık, AI kapalı):** Sıfırdan küçük bir API yaz: 2 ilişkili tablo, kayıt/giriş, sahiplik kontrolü (başkasının kaydına erişim reddedilmeli), Zod doğrulaması, 3 entegrasyon testi. Ardından güvenlik soruları (IDOR, SQL injection, CSRF, XSS ne demek, nasıl önlenir).

**Çıktı:** CV-2 backend'i (canlı API, testli).

---

### FAZ 4: Next.js ve fullstack birleştirme (Hafta 27–34)

**Amaç:** CV-2'yi tam fullstack ürün haline getirmek. Modern araçlar: Next.js, Tailwind, shadcn/ui, Playwright, Docker, CI.
**Ana kaynaklar:** Next.js resmi "Learn" içeriği ve dokümanı, Tailwind dokümanı, Playwright dokümanı, Docker "Get started", GitHub Actions dokümanı.
**AI evresi 2 başlar** (Bölüm 4.6).

| Hafta | Konu | İnşa et | Kapanış soruları |
|---|---|---|---|
| **27** | **Tailwind + shadcn/ui, Next.js giriş:** utility-first CSS, App Router, layout, Server vs Client Component | CV-2 frontend iskeleti, tasarım sistemi (renk, tipografi) | Server Component ile Client Component farkı? |
| **28** | **Next.js veri ve Server Actions:** Server Component'te veri çekme, Server Actions, TanStack Query'nin ne zaman gerektiği | Harcama listesi ve ekleme formu | **Her Server Action'ın başında neden oturum ve yetki kontrolü gerekir?** |
| **29** | **Frontend I:** auth akışları, korumalı rotalar, dashboard | Giriş/kayıt, harcama listesi, filtreler | Korumalı rota sadece arayüzde mi olur? |
| **30** | **Frontend II:** CSV yükleme arayüzü, grafikler, formlar, erişilebilirlik | Aylık özet grafikleri, import ekranı ve hata raporu | Erişilebilir bir form nasıl olur? |
| **31** | **Playwright E2E ve bileşen testleri** | Kayıt → giriş → harcama ekle → CSV yükle akışının E2E testi | E2E ne zaman, birim test ne zaman? |
| **32** | **Docker ve Compose** | Tüm yığın (app, API, Postgres) tek `docker compose up` ile ayağa kalksın | Image ile container farkı? Volume neden? |
| **33** | **GitHub Actions (CI)** | Her PR'da lint, typecheck, test, E2E çalışsın; CI yeşil olmadan birleştirme yok | CI neden var? Flaky test nedir? |
| **34** | **CV-2 cilası:** README, mimari şeması, demo hesabı, Lighthouse, erişilebilirlik kontrolü, 3 dk İngilizce anlatım | **CV-2 tamamlandı** (canlı, testli, CI'lı, Docker'lı) | Bu projeyi 3 dakikada İngilizce anlat |

**Kapı testi (3 saat, AI kapalı):** Canlı CV-2 üzerinde bir **özellik talebi** (örn. "kategoriye bütçe limiti ekle") uygula: migration, endpoint, arayüz, 2 test, PR aç, CI yeşil olsun. Ardından sistem soruları (Server Actions güvenliği, session vs JWT, index neden).

**Çıktı:** **CV-2** (fullstack amiral gemisi).

---

### FAZ 5: Fark yaratan proje, portföy v2, mülakat (Hafta 35–42)

**Amaç:** SFMC alan bilginle **farklılaşan bir proje**, portföy v2 ve işe alım hazırlığı.
**AI evresi 3** (serbest ama denetimli).

**CV-3 kapsamı (Onay Yönetimi / Consent Manager):** Kullanıcılar markalar/kategoriler için e-posta izinlerini yönetir. **Denetim kaydı (audit log)**, rol tabanlı yetki (kullanıcı/yönetici), yönetici paneli (liste, filtre, CSV dışa aktarma), izin değişikliklerinde webhook. GDPR mantığı: kim, ne zaman, neyi değiştirdi.

| Hafta | Konu | İnşa et | Kapanış soruları |
|---|---|---|---|
| **35** | **NestJS giriş:** modül, controller, provider, bağımlılık enjeksiyonu (Express'in karşılığı) | CV-2 API'sinden bir modülü NestJS'e taşı | DI ne çözer? Express'ten farkı? |
| **36** | **NestJS + Zod + Drizzle, Guard'lar; CV-3 alan modeli** | Consent Manager ERD, iş kuralları (geri çekme, geçmiş saklama) | Denetim kaydı neden transaction içinde yazılır? |
| **37–38** | **CV-3 backend:** RBAC, audit log, transaction, webhook, testler | Uç noktalar, sahiplik ve rol kontrolleri, entegrasyon testleri | Yetkilendirmeyi nerede kontrol edersin? |
| **39** | **CV-3 frontend (Next.js) + E2E** | Kullanıcı tercih ekranı, yönetici paneli, Playwright akışı | Hata durumları nasıl gösterilir? |
| **40** | **CV-3 dağıtım:** CI, Docker, README, SFMC hikâyesi | **CV-3 canlı** | "SFMC'de gördüğün problemi kodla nasıl çözdün?" |
| **41** | **Portföy v2:** Next.js + Tailwind, 3 vaka çalışması | **Portföy v2 canlı** (bölüm 8) | Kimin için, hangi sorunu, hangi kararlarla? |
| **42** | **Profil cilası ve kapanış:** iki CV PDF'i, GitHub profil README, LinkedIn, mock mülakatlar | Tüm materyaller (Bölüm 8 kontrol listesi) | 3 dk İngilizce proje anlatımı + 3 STAR hikâyesi |

**Kapı testi:** İki mock mülakat (Copilot veya bir arkadaş mülakatçı olur: soru sorar, cevabı hemen söylemez). Biri teknik (proje ve sistem soruları), biri davranışsal (STAR).

---

## 6. Hat A: Gelir hattı (Hafta 1'den itibaren)

**Neden:** Gelirin yok. Junior fullstack piyasası sert (bir kaynağa göre giriş seviyesi ilanlar yaklaşık %46 azalmış, rakam kaba). SFMC deneyimin şu an **en satılabilir** varlığın.

### Haftalık kota
- **10 hedefli başvuru** (SFMC, MarTech, Salesforce ekosistemi). Her ilan için CV'yi ilana göre uyarla.
- **5 referans/ağ mesajı** (eski iş arkadaşları, recruiter'lar, SFMC topluluğu).
- Sonuçları bir tabloya yaz: tarih, şirket, kanal, durum (başvuruldu/yanıt/mülakat/red), sonraki adım.

### Hedefler
| Pazar | Ne | Not |
|---|---|---|
| **Türkiye** | Salesforce/CRM danışmanlık firmaları, e-ticaret, fintech, ajanslar | Referans en verimli kanal. LinkedIn ve Kariyer.net |
| **Uzaktan SFMC (freelance/B2B)** | Avrupa merkezli kısa süreli ve saatlik işler | Bu tür ilanlar justjoin.it ve collective.work gibi platformlarda görülüyor, güncel durumunu kontrol et. Fatura/şirket kurulumunu muhasebeciyle netleştir |
| **Yurtdışına taşınma** | Sponsorlu vize | Junior için zor, mid-level'e yaklaşınca gerçekçi (aşağıya bak) |
| **Uzaktan fullstack** | Yabancı şirketler | En rekabetlisi, portföy hazır olunca |

**Almanya notu (doğrulanması gereken güncel rakamlar):** 2026 için Mavi Kart eşikleri genel meslekler ~€50.700, BT dahil bazı açık meslekler ~€45.934,20 brüt/yıl. Fırsat Kartı (Chancenkarte) iş aramak için ayrı bir yol, puan sistemi ve mali yeterlilik şartı var. **Başvurudan önce resmi kaynaktan veya göç danışmanından doğrula.** Bu plan hukuki danışmanlık değildir.

### Fullstack başvuruları
- **Hafta 16'dan itibaren:** Staj, kısa dönem, startup gibi düşük eşikli fırsatlara **haftada 3–5** deneme başvurusu.
- **Hafta 26'dan itibaren (CV-1 ve CV-2 API canlı):** Haftada **10** fullstack başvurusu.
- **Hafta 34'ten itibaren (CV-2 tamam):** Haftada **15**.
- **Her CV iki sürümde:** (A) Full Stack Developer (JS/TS), (B) SFMC/MarTech Developer.

### CV kuralları
- Mülakatta savunamayacağın teknolojiyi yazma. Listedeki her şey sorulur.
- TypeScript'i öğrendikten sonra ekle.
- Referanslara telefon numarası koyma, "istenirse sağlanır" yaz.
- CV'ndeki **sayısal sonuçları** (CTR, açılma oranı gibi) koru, yeni projelere de sayı ekle (test sayısı, Lighthouse skoru, import hızı).
- İşsizlik boşluğu: "Bu sürede şunları öğrendim ve şu projeleri canlıya aldım" diye anlat, portföy ve GitHub commit geçmişi kanıt olur.

---

## 7. Hat B: Mülakat hazırlığı (Hafta 17'den itibaren, haftada ~1 saat)

| Alan | Yöntem |
|---|---|
| **Algoritma** | LeetCode Easy, toplam ~50 soru (Hafta 17–42, haftada ~2). Önce kendi çöz, takılınca 4.5 protokolü |
| **Teknik sorular** | Haftada 5 soru kartı: tarayıcıya URL yazınca ne olur, REST vs GraphQL, SQL JOIN ve index, event loop, React render, session vs JWT, XSS ve SQL injection |
| **Sistem tasarımı temelleri** | Hafta 35'ten itibaren: istemci-sunucu, indeks, auth akışları, basit ölçekleme kavramları |
| **İngilizce** | Haftada bir **3 dakikalık kayıt:** bir kavramı veya projeni İngilizce anlat, kendin dinle |
| **Mock mülakat** | Hafta 30'dan itibaren iki haftada bir. Copilot mülakatçı olur: soru sorar, değerlendirir, cevabı hemen söylemez |
| **Davranışsal** | 3 STAR hikâyesi (SFMC'den): zor bir teknik problem, bir hata ve düzeltme, ekip içi bir anlaşmazlık |

---

## 8. Projeler ve CV materyalleri

### 8.1 Proje tanım-tamamlanma kriterleri (Definition of Done)

Her CV projesi şunların hepsi olmadan "bitti" sayılmaz:

- [ ] Canlı demo + **demo kullanıcı hesabı** (kayıt olmadan denenebilir)
- [ ] README: problem, ekran görüntüleri, teknoloji seçimleri ve **nedenleri**, mimari şeması, kurulum, testleri çalıştırma, bilinen eksikler
- [ ] Testler: birim/entegrasyon (+ CV-2 ve CV-3 için en az 1 E2E)
- [ ] CI yeşil (CV-2 ve CV-3)
- [ ] Docker ile yerel çalıştırma (CV-2 ve CV-3)
- [ ] Güvenlik kontrol listesi geçildi (aşağıda)
- [ ] Temiz commit geçmişi (anlamlı mesajlar, PR'lar)
- [ ] Kararlar ve trade-off'lar yazılı ("neden Drizzle, neden session?")

**Güvenlik kontrol listesi:** Şifreler hash'li · girdiler doğrulanıyor · SQL parametreli · XSS'e karşı güvenli çıktı · yetki kontrolü sunucuda · gizli anahtar kodda değil · CORS bilinçli · hassas veri loglanmıyor.

### 8.2 Projeler

| Proje | Faz | Yığın | Neden CV'de değerli |
|---|---|---|---|
| **Portföy v1** | F1 | Saf HTML/CSS/JS | İlk vitrin, CSS denetimi |
| **CV-1: Keşif uygulaması** | F2 | React, TS, TanStack Query, RHF, Zod, Vitest, RTL | Modern frontend'in temeli |
| **CV-2: Harcama Takibi** | F3–F4 | Next.js, TS, Express, PostgreSQL, Drizzle, session auth, Tailwind, shadcn/ui, Playwright, Docker, GitHub Actions | Tam fullstack, veri modelleme (SQL gücünü gösterir), güvenlik, test, CI |
| **CV-3: Onay Yönetimi** | F5 | Next.js, NestJS, PostgreSQL, Drizzle, RBAC, audit log, webhook, Playwright | SFMC alan bilgin + GDPR, kurumsal backend deseni |
| **Portföy v2** | F5 | Next.js, Tailwind | Vaka çalışmalarıyla vitrin |

**Not:** Harcama takibi yerine gym tracker gibi başka bir alan seçebilirsin, mimari aynı kalır. Kritik olan projenin **kalite çıtası**, konusu değil. Banka API'si (Garanti BBVA vb.) ilk sürümde yok. Erişim şartlarını resmi geliştirici portalından doğrulayıp ileride isteğe bağlı modül olarak eklenebilir.

### 8.3 Portföy v2 içeriği
- Kısa tanıtım: kimsin, hangi problemleri çözüyorsun (SFMC geçmişi + fullstack).
- **3 vaka çalışması** (her biri: problem → karar → trade-off → sonuç → sayılar). CV-2, CV-3 ve SFMC işinden bir örnek (anonim, müşteri verisi yok).
- Canlı demo ve GitHub bağlantıları.
- Teknik hedefler: mobil uyumlu, erişilebilir (klavye ve kontrast), Lighthouse'ta yüksek performans skoru, iletişim bağlantıları.

### 8.4 Sonda elinde olması gereken materyaller

- [ ] Portföy v2 (canlı)
- [ ] CV-1, CV-2, CV-3 (canlı, README'li)
- [ ] 2 CV PDF (Fullstack ve SFMC/MarTech)
- [ ] GitHub profil README + sabitlenmiş 3 repo
- [ ] LinkedIn (başlık, hakkında, projeler)
- [ ] 3 dk İngilizce proje anlatımı
- [ ] 3 STAR hikâyesi
- [ ] 3 vaka çalışması metni

### 8.5 CV madde şablonu
> **Built** [ne] using [teknolojiler]; **achieved** [ölçülebilir sonuç].
> Örnek: "Built a personal finance tracker (Next.js, Express, PostgreSQL); CSV import handles 10,000 rows with per-row error reporting; 45 automated tests, CI green on every PR."

---

## 9. Kontrol noktaları ve karar kuralları

| Ne zaman | Kontrol | Karar |
|---|---|---|
| Her cuma | Haftalık demo yapıldı mı? | Hayırsa ertesi gün 30 dk telafi |
| Her kapı testi | Kriterin %80'i geçildi mi? | Hayırsa 1 hafta tekrar, sonra tekrar dene |
| **İki hafta üst üste plan gerisinde** | Neden? (zaman, zorluk, motivasyon) | Zaman: saatleri/kapsamı ayarla. Zorluk: konuyu küçült. Motivasyon: dinlen, projeyi küçült |
| **Hafta 16** | Gelir durumu | Geçim payın 3 aydan azsa Hat A'ya haftalık zamanın %50'sini ver |
| **Her 4 haftada** | Başvuru funnel'i | Yanıt oranı %5'in altındaysa CV/portföyü gözden geçir, mesajı değiştir |
| **Hafta 26** | CV-1 canlı, CV-2 API canlı mı? | Değilse fullstack başvurularını ertele, Faz 3'ü bitir |
| **Hafta 42** | 30+ fullstack başvurusu, yine de görüşme yok | Sırayla test et: CV → portföy → mülakat performansı. **SFMC hattını ana yapıp fullstack'i yan hat yapmak meşru bir karardır** |
| **Aylık** | Piyasa taraması (Bölüm 3) | Listeyi güncelle |

---

## 10. Hız ayarı (haftalık saate göre)

| Haftalık saat | Yaklaşık süre | Not |
|---|---|---|
| **15** | ~42 hafta (~10 ay) | Ana plan |
| **25** | ~26 hafta (~6 ay) | İnşa etme bloğunu artır, tekrar ve mülakat blokları aynı kalır |
| **35** | ~19 hafta (~4,5 ay) | Sadece gerçekten sürdürülebilirse. Yorgunluk öğrenmeyi düşürür |

**Kural:** Saat artınca **hızlanan şey haftalık kapsam**, kapı testi kriteri değil. Kriteri gevşetme.

---

## 11. Şablonlar

### `PROGRESS.md`

```
# İlerleme

## Başlangıç
- Geçim payım (ay): 
- Haftalık ayırabildiğim saat:
- Tarih:

## Şu anki durum
- Faz / Hafta:
- Son kapı testi: (geçti / geçmedi / tarih)

## Bu hafta
- Hedef:
- Yaptıklarım:
- Süre (saat): Öğren __ · İnşa et __ · Tekrar __ · Gelir __ · Mülakat __
- Cuma demosu: (bağlantı / not)

## Hat A: Başvuru takibi
| Tarih | Şirket | Kanal | Durum | Sonraki adım |

## Hata günlüğü
| Tarih | Hata / tıkanma | Kök neden | Nasıl çözdüm | Yardım basamağı (1–6) |

## Kavram kartları (bu haftaki yeniler)
- Soru → Cevap

## Kapı testi kayıtları
- Faz / Tarih / Kriter geçme oranı / Eksik konular

## Projeler
| Proje | Repo | Canlı demo | Durum | DoD kaç madde tamam |
```

### Kavram kartı örnekleri
- Ön: "`map` ile `forEach` farkı nedir, ne zaman hangisi?" Arka: "`map` yeni dizi döner, `forEach` dönmez. Dönüşüm için `map`."
- Ön: "Şu fonksiyonu kaynaksız yaz: bir dizideki çift sayıların karesini topla." Arka: (kendi çözümün + hangi yöntemler)

---

## 12. Kaynaklar (fazda tek ana kaynak, gerisi referans)

Kaynak içerikleri ve sıraları değişebilir, başlamadan önce güncel halini kontrol et.

| Faz | Ana kaynak | Referans |
|---|---|---|
| **F0** | Pro Git kitabının ilk bölümleri (ücretsiz, çevrimiçi) | GitHub dokümanı |
| **F1** | javascript.info | MDN Web Docs |
| **F2** | react.dev "Learn", TypeScript Handbook | Testing Library dokümanı, TanStack Query dokümanı |
| **F3** | Express ve Node.js dokümanları, PostgreSQL dokümanı, Drizzle dokümanı | pgexercises (SQL pratiği), OWASP Top 10, PortSwigger Web Security Academy |
| **F4** | Next.js resmi "Learn" içeriği | Tailwind, Playwright, Docker "Get started", GitHub Actions dokümanları |
| **F5** | NestJS dokümanı | Sistem tasarımı temelleri için seçeceğin tek kaynak |
| **Mülakat** | LeetCode Easy (veya NeetCode listesi) | — |

**Bir kaynak seçtiysen o fazda başka müfredata geçme.** Eksik bir kavramı **referansta** ara, ana kaynağa dön.
