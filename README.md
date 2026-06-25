# ZenBlog — Client

ZenBlog blog uygulamasının Angular 21 tabanlı frontend'idir. Hem ziyaretçiye yönelik blog arayüzünü hem de yönetim (admin) panelini içerir.

## 🚀 Teknolojiler

- **Angular 21** (Zoneless — değişiklik algılama `signal()` tabanlı)
- **TypeScript**
- Module-based yapı (NgModule) + yeni control flow (`@if`, `@for`)
- **RxJS** (HttpClient)
- **@auth0/angular-jwt** — JWT token çözümleme & yetkilendirme
- **Bootstrap 5** + Bootstrap Icons + Font Awesome
- **SweetAlert2**, **Alertify** — bildirimler
- **Swiper**, **AOS** — slider & scroll animasyonları

## 🗂️ Proje Yapısı
src/app

├── _layouts           # main-layout (ziyaretçi), admin-layout (panel)

├── _main-components   # home, blogdetails, login, contact, category-blogs ...

├── _admin-components  # category, blog, comment, message, social, contact-info

├── _services          # API servisleri (HttpClient)

├── _models            # DTO arayüzleri

├── _guards            # AuthGuard

├── _interceptors      # TokenInterceptor (JWT header)

├── app-module.ts

└── app-routing-module.ts

## ✨ Özellikler

### Ziyaretçi Arayüzü

- **Home** — son bloglar + kategoriye göre blog grid'i
- **Blog Detay** — dinamik içerik, yorumlar ve yanıtlar (reply)
- **Kategori sayfası** — `/category/:id`, kategoriye ait tüm bloglar
- **Dinamik header/footer** — sosyal medya bağlantıları & iletişim bilgileri DB'den
- **İletişim formu** — mesaj gönderme

### Admin Paneli

- Blog, Category, Comment, Message, Social, ContactInfo yönetimi
- Mesajlar için okundu / okunmadı filtreleme
- JWT korumalı rotalar (AuthGuard)

---

> Bu proje **ZenBlog** uygulamasının **frontend (Web UI)** kısmıdır.
> Backend (.NET 9 API) için: **ZenBlogServer**
