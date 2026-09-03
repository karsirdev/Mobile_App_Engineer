# ✅ Checklist thực hành — Mobile Engineer (Nguyên)

> Không lý thuyết suông. Mỗi mục đều là bài cụ thể phải hoàn thành, có sản phẩm/commit để kiểm chứng.
> Nhịp độ: 12 tuần, 6 buổi/tuần. Mỗi buổi ~1.5–2h.

---

## 🔁 Checklist mỗi ngày (áp dụng suốt 12 tuần)

- [ ] 1 bài LeetCode C++ (theo chủ đề tuần) → commit vào `github.com/karsirdev/Leetcode` (Conventional Commits)
- [ ] 30–45 phút code tính năng thật cho SavingsBook (không tutorial, không copy code mẫu)
- [ ] Commit ít nhất 1 lần/ngày kèm message rõ ràng (`feat:`, `fix:`, `refactor:`)
- [ ] Cuối ngày ghi 2–3 dòng vào `DEVLOG.md`: hôm nay làm gì, vướng gì, ngày mai làm gì

---

## Tuần 1–2 — Swift & Kotlin nền tảng

**Bài tập bắt buộc (không phải đọc doc):**
- [ ] Viết 1 struct/class Swift mô phỏng `SavingsAccount` (số dư, lãi suất, ngày đáo hạn) + unit test tính lãi đơn/lãi kép
- [ ] Làm lại y hệt bằng Kotlin `data class` — so sánh null-safety Kotlin vs Optional Swift, viết note ngắn về khác biệt
- [ ] Viết 5 hàm dùng `higher-order functions` (map/filter/reduce) trên danh sách tài khoản mẫu — cả 2 ngôn ngữ
- [ ] LeetCode: 10 bài Array/String (Easy→Medium) bằng C++
- [ ] Build 1 màn hình SwiftUI tĩnh: danh sách tài khoản tiết kiệm (List + custom row), không dùng ViewModel
- [ ] Build lại đúng màn hình đó bằng Jetpack Compose (LazyColumn + custom composable)

**Sản phẩm cuối tuần:** 2 file model + 2 file test + 2 screenshot màn hình (iOS/Android) push lên repo `SavingsBook`.

---

## Tuần 3–4 — State management & Navigation

- [ ] SwiftUI: thêm `@Observable` ViewModel quản lý danh sách tài khoản, có thêm/xoá/sửa
- [ ] Compose: thêm `ViewModel` + `StateFlow` làm y hệt chức năng trên
- [ ] Thêm navigation: từ danh sách → màn hình chi tiết tài khoản (cả 2 nền tảng)
- [ ] LeetCode: 10 bài Two Pointers + Binary Search bằng C++
- [ ] Viết form "Thêm tài khoản mới" có validate input (số dư âm, ngày sai) — cả 2 nền tảng
- [ ] Viết 3 unit test cho logic validate đó

**Sản phẩm cuối tuần:** Flow thêm/xem/xoá tài khoản chạy được end-to-end trên cả iOS và Android (chưa cần backend).

---

## Tuần 5–6 — Local storage & Concurrency

- [ ] iOS: lưu tài khoản bằng SwiftData (hoặc CoreData) thay vì array tạm — migrate dữ liệu tuần trước
- [ ] Android: lưu bằng Room — làm y hệt
- [ ] Viết 1 tính năng dùng `async/await` (Swift) và `coroutine` (Kotlin): giả lập fetch lãi suất từ "server" delay 2s, hiện loading state
- [ ] LeetCode: 10 bài Linked List bằng C++
- [ ] Viết bài test cho tầng Repository (không test UI) — cả 2 nền tảng

**Sản phẩm cuối tuần:** Data persist qua restart app, có loading/error state thật (không fake).

---

## Tuần 7–8 — Kết nối Backend thật (FastAPI)

- [ ] Trong `research_management`/backend riêng: viết endpoint `GET/POST /accounts` cho SavingsBook (dùng kiến thức IT215)
- [ ] iOS: gọi API bằng `URLSession` + `Codable`, thay Repository local bằng network call thật
- [ ] Android: gọi API bằng `Retrofit`, làm tương tự
- [ ] Viết middleware/logic tính lãi suất thật ở backend (không hardcode ở client)
- [ ] LeetCode: 8 bài Trees bằng C++
- [ ] Viết 3 test case cho API bằng `pytest` (backend)

**Sản phẩm cuối tuần:** SavingsBook đọc/ghi dữ liệu qua API thật, có demo video ngắn tự quay lại (không cần đăng, chỉ để tự đánh giá).

---

## Tuần 9 — Auth thật

- [ ] Implement OTP verification flow đầy đủ (đã có phần iOS, giờ hoàn thiện cả backend + Android)
- [ ] Lưu token bằng Keychain (iOS) và EncryptedSharedPreferences (Android) — **không lưu plain text**
- [ ] LeetCode: 6 bài Hash Table/Set bằng C++

**Sản phẩm cuối tuần:** Đăng nhập/đăng ký hoạt động thật, token không lộ trong logs hay plaintext storage.

---

## Tuần 10 — Mobile Security áp dụng thực tế

- [ ] Audit lại toàn bộ luồng OTP + lưu trữ token bằng checklist OWASP Mobile Top 10 (tự viết report ngắn, liệt kê lỗ hổng tìm được)
- [ ] Implement certificate pinning cho API call (cả 2 nền tảng)
- [ ] Dùng Jadx decompile thử bản debug APK của chính mình — xem code có bị lộ gì không, viết note khắc phục
- [ ] Áp dụng ProGuard/R8 rules cơ bản cho bản Android, so sánh trước/sau

**Sản phẩm cuối tuần:** Báo cáo bảo mật (1 trang) + code fix đã áp dụng, commit riêng `security:` prefix.

---

## Tuần 11 — Testing & CI

- [ ] Viết UI test cơ bản: flow đăng nhập → thêm tài khoản (XCTest + Compose Test)
- [ ] Set up GitHub Actions: build + chạy test tự động khi push (cả iOS và Android job)
- [ ] LeetCode: 6 bài Sliding Window/Stack bằng C++

**Sản phẩm cuối tuần:** Badge CI "passing" hiển thị trên README repo SavingsBook.

---

## Tuần 12 — Polish & Case study

- [ ] Viết README case study cho SavingsBook: vấn đề giải quyết, kiến trúc, quyết định kỹ thuật, ảnh chụp màn hình
- [ ] Ghi lại 3 khó khăn lớn nhất đã gặp trong 12 tuần và cách xử lý — dùng để trả lời phỏng vấn sau này
- [ ] Build thử 1 archive/release build (TestFlight nội bộ hoặc Android internal testing)
- [ ] Review lại toàn bộ `DEVLOG.md` 12 tuần, tự chấm điểm tiến độ

**Sản phẩm cuối:** Repo SavingsBook hoàn chỉnh, README chuyên nghiệp, sẵn sàng đưa vào portfolio/CV.

---

## 📌 Quy tắc chống học chay

1. Không tick ô nào nếu chưa có **commit thật** tương ứng.
2. Nếu 1 bài tập khó quá 45 phút không ra — ghi lại chỗ mắc vào `DEVLOG.md`, hỏi cụ thể (không hỏi chung chung "sao code không chạy").
3. Cuối mỗi tuần, xoá code demo/tutorial-copy nếu có — chỉ giữ code tự viết.
