# 🚀 VIRA PLAYER

**High-Performance, Secure, and Family-Friendly Android TV/OTT Media Player**

Vira Player is a premium, next-generation media player designed for Android TV, Google TV, and Amazon Fire TV. Built with a focus on stability, security, and user experience, it offers a seamless IPTV and OTT streaming experience without providing any content itself.

![Vira Player Banner](assets/banner.png) *(İleride banner görselini buraya ekleyebilirsiniz)*

## 🌟 Key Features

### ️ Security & Family Control
- **Dynamic Content Shield:** Cinematic age and content warnings (e.g., +16, Violence, Drama) before playback.
- **Strict Adult Content Filter:** Absolute filtering of 18+ and NSFW content in Free VOD modules at the API, database, and UI levels.
- **Smart Kids Matching:** Automatically filters and displays only verified kids' categories (Kids, Children, Çocuk, etc.).

###  Premium Media Experience
- **Hybrid Player Engine:** Default Media3 ExoPlayer with an optional fallback engine for maximum compatibility.
- **Advanced Buffering:** Adaptive bitrate streaming (ABR) with optimized buffer profiles for Live TV and VOD.
- **10-Foot UI:** Netflix-inspired, dark-themed, and fully optimized for TV remote (D-Pad) navigation.

### 🕌 Specialized Modules
- **Dual Quran Experience:** 
  - Independent reading/listening module (UmmahAPI).
  - Tube module for verified long-form Quranic videos via official YouTube embeds.
- **Free TV & Radio:** Curated, legal, and free-to-air global channels and radio stations.
- **Tube (Long-form YouTube):** Dedicated section for high-quality videos over 20 minutes (documentaries, podcasts).

### 🔒 Licensing & Architecture
- **Single-User License Architecture:** Strictly designed for single-user M3U/Xtream list usage. No concurrent session sharing.
- **Closed-Circuit Server Login:** Users can only connect to pre-approved, admin-managed servers.
- **Remote Configuration:** Cloudflare-based admin panel for dynamic server management and QR contact updates without APK updates.

## 🛠️ Tech Stack

- **Language:** Kotlin
- **UI Framework:** Jetpack Compose (TV Material 3)
- **Architecture:** MVVM + Clean Architecture
- **State Management:** Coroutines & StateFlow
- **Dependency Injection:** Hilt (Dagger)
- **Networking:** Retrofit / OkHttp
- **Local Database:** Room Database (with FTS for search)
- **Media Playback:** AndroidX Media3 ExoPlayer

## 📂 Project Structure

```text
app/
├── core/
│   ├── player/         # Media3 ExoPlayer abstraction & engines
│   ├── network/        # Retrofit, interceptors, API services
│   ├── database/       # Room database, DAOs, entities
│   └── design/         # Theme, colors, typography, UI components
├── features/
│   ├── auth/           # Login, Xtream validation, subscription lock
│   ├── live-tv/        # Live TV UI, EPG, channel management
│   ├── movies/         # VOD modules
│   ├──
