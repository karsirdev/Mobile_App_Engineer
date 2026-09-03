# 🚀 Lộ trình trở thành Mobile Engineer — Nguyên (karsirdev)

> Sinh viên năm nhất (2007) · MacBook M4 Pro · Kotlin · Swift · C++
> Mục tiêu: Thành thạo cả iOS (Swift/SwiftUI) lẫn Android (Kotlin/Jetpack Compose), song song định hướng Cybersecurity làm lợi thế riêng.

---

## 📍 Giai đoạn 0 — Nền tảng (đang làm)

- [x] Cài đặt môi trường: Xcode, Android Studio, VS Code, CLion
- [x] Ôn Python OOP (IT202), Database (MySQL: trigger, stored procedure, transaction, ACID)
- [x] Ôn FastAPI backend (IT215) — hiểu REST API, sẽ cần khi mobile app gọi backend
- [ ] Luyện DSA bằng C++ song song (tư duy thuật toán dùng chung cho mọi ngôn ngữ)
- [ ] Git/GitHub thành thạo: branch, PR, conflict resolution

**Mục tiêu ra giai đoạn:** Đọc hiểu code Swift/Kotlin cơ bản, tự tin dùng Git.

---

## 📱 Giai đoạn 1 — Ngôn ngữ & Nền tảng UI (3–4 tháng)

### iOS
- Swift cơ bản → nâng cao: Optionals, Closures, Protocols, Generics
- SwiftUI: State/Binding/Observable, layout system, navigation
- Swift Concurrency (`async/await`, Task) — đã áp dụng ở SavingsBook (OTP flow)

### Android
- Kotlin cơ bản → nâng cao: null-safety, coroutines, sealed class, extension functions
- Jetpack Compose: state hoisting, layout, navigation, theming
- Coroutines & Flow cho xử lý bất đồng bộ

**Dự án thực hành:** Tiếp tục hoàn thiện **SavingsBook** (đã có UI Figma 2 theme, OTP flow iOS) → build song song bản Android bằng Compose để so sánh trực tiếp 2 hệ sinh thái.

---

## 🏗️ Giai đoạn 2 — Kiến trúc & Networking (3–4 tháng)

- MVVM / Clean Architecture (áp dụng cho cả Swift & Kotlin)
- Local storage: SwiftData/CoreData (iOS), Room (Android)
- Networking: URLSession/Alamofire (iOS), Retrofit/Ktor (Android)
- Kết nối app với backend FastAPI đã học ở IT215 — tự build API cho SavingsBook thay vì mock data
- Dependency Injection cơ bản (Swinject / Hilt)
- Unit test & UI test cơ bản (XCTest, JUnit/Compose Test)

**Mục tiêu ra giai đoạn:** SavingsBook có backend thật, auth, và test coverage tối thiểu.

---

## 🔐 Giai đoạn 3 — Mobile Security (lợi thế cạnh tranh)

> Đây là điểm khác biệt: kết hợp Cybersecurity + Mobile.

- OWASP Mobile Top 10
- Secure storage: Keychain (iOS), EncryptedSharedPreferences/Keystore (Android)
- Certificate pinning, obfuscation cơ bản (ProGuard/R8)
- Reverse engineering cơ bản để hiểu góc nhìn attacker (Jadx, Hopper/Ghidra ở mức nhập môn)
- Áp dụng vào SavingsBook: audit lại luồng OTP, lưu trữ dữ liệu tài chính nhạy cảm

---

## 🌐 Giai đoạn 4 — Cross-platform & Mở rộng (tùy chọn)

- Khảo sát Flutter hoặc KMP (Kotlin Multiplatform) — tận dụng nền Kotlin sẵn có
- CI/CD cho mobile: Fastlane, GitHub Actions build cho cả 2 nền tảng
- Publish thử app lên TestFlight / Google Play Internal Testing

---

## 📦 Portfolio cần có (đăng trên github.com/karsirdev)

| Dự án | Nền tảng | Trạng thái |
|---|---|---|
| SavingsBook | iOS + Android | 🔄 Đang phát triển |
| Research Management (FastAPI) | Backend | 🔄 Hỗ trợ học API/backend |
| App bảo mật nhỏ (password manager / secure notes) | iOS hoặc Android | 🎯 Sắp tới — thể hiện mảng security |
| README + case study cho từng app | — | 🎯 Viết rõ kiến trúc, quyết định kỹ thuật |

---

## 🧭 Nguyên tắc theo suốt lộ trình

1. **Học 1 nền tảng sâu trước, nền tảng kia song song ở mức đọc hiểu** — tránh học 2 thứ half-baked cùng lúc.
2. Mỗi giai đoạn đều gắn với 1 tính năng cụ thể trong SavingsBook — học xong áp dụng ngay, không học chay.
3. Security không phải giai đoạn cuối để "học cho biết" — review lại code cũ dưới góc nhìn bảo mật sau mỗi giai đoạn.
4. Viết README/case study ngay sau khi hoàn thành 1 tính năng, đừng để dồn cuối.

---

*Cập nhật lần cuối: theo tiến độ cá nhân — nên fork file này vào repo và tick từng mục khi hoàn thành.*
