# KHUNG LANDING PAGE & DESIGN SYSTEM PARIS v2.0
Version: 2.0 — kế thừa mục 5.2 + MODE 2 bản v1.3

## Chọn loại landing

| | **LOẠI A — Khách hàng làm đẹp** | **LOẠI B — Vấn đề khách hàng** |
|---|---|---|
| **Intent xuất phát** | Đã muốn nụ cười đẹp | Từ nỗi đau răng miệng |
| **Khung** | **AIDA** | **PAS** — Vấn đề → Khoét sâu → Giải pháp |
| **Mạnh nhất ở** | Giai đoạn 2 và 4 | **Giai đoạn 3 (cân nhắc & nỗi sợ)** |
| **Dịch vụ điển hình** | Răng sứ thẩm mỹ · Veneer · niềng để đẹp · tẩy trắng | Mất răng → Implant · hô/móm → niềng · răng ố/sâu/đau → tẩy trắng/tủy · răng khôn lệch → nhổ |

Chọn sai loại là nguyên nhân phổ biến nhất của **CTR ổn nhưng không ai điền form**.

---

## LOẠI A — AIDA (13 section)

1. **Hero (70–90vh)** — headline nụ cười đẹp + subheadline + CTA chính + CTA phụ + trust badge + thống kê
2. **Trust** — giấy phép Sở Y tế + **đối tác hãng** (Straumann · Invisalign · Nacera · Ormco) + báo chí
3. **Dịch vụ** — card: icon – tên – mô tả – CTA
4. **Vì sao chọn Paris** — chuẩn Pháp · BS ĐH Y · bảo hành · trả góp
5. **Công nghệ** — Piezotome · WhiteMax · CAD-CAM…
6. **Đội ngũ bác sĩ** (tên thật từ hồ sơ thương hiệu)
7. **Quy trình**
8. **Chi phí / ưu đãi / trả góp** `[động]`
9. **Feedback khách**
10. **Before–After thật** (đã duyệt pháp lý)
11. **FAQ**
12. **Booking CTA + form**
13. **Footer** — hotline, chi nhánh

---

## LOẠI B — PAS (13 section)

1. **Hero** — gọi đúng **Vấn đề/nỗi đau** (mất răng · hô móm · răng ố…) + hứa hẹn giải pháp + CTA
2. **Khoét sâu** — hệ quả nếu không xử lý: **tiêu xương · lệch khớp cắn · mất tự tin**
3. **Giải pháp** — phương pháp Paris giải quyết đúng vấn đề đó
4. **Gỡ 3 rào cản (Sợ–Ngờ–Ngại)** ★ — giảm đau (Piezotome) · trụ/sứ **chính hãng** · BS chứng chỉ quốc tế · bảo hành · trả góp
5. **Bằng chứng** — case thật **đúng vấn đề đó** + đối tác hãng
6. **Bác sĩ** (tên thật)
7. **Quy trình an toàn**
8. **Chi phí / ưu đãi / trả góp** `[động]`
9. **Feedback người từng gặp đúng vấn đề đó**
10. **Before–After**
11. **FAQ xử lý nỗi sợ**
12. **Booking CTA + form**
13. **Footer**

> Section 4 là trái tim của loại B. Làm hời hợt ở đây thì cả trang mất tác dụng.

---

## Micro-conversion — lợi thế riêng của Paris
Paris có sẵn **công cụ kiểm tra online**: Kiểm tra răng miệng · kiểm tra niềng · kiểm tra răng sứ · kiểm tra trồng răng.

**Nhúng công cụ này làm bước trung gian trước form booking.** Khách đang ở giai đoạn 3 chưa sẵn sàng để lại số điện thoại, nhưng sẵn sàng bấm vài câu hỏi để biết tình trạng mình. Đây là cách hạ rào cản **NGẠI** mà không mất lead.

Đặt công cụ: sau section **Gỡ 3 rào cản** (loại B) hoặc sau section **Dịch vụ** (loại A).

---

## Quy tắc chung
- **CTA lặp sau mỗi 2–3 section** + **Sticky CTA mobile** + **Popup CTA**.
- Giá, ưu đãi và **trả góp** luôn là dữ liệu động — lấy tại `/hoan-my-bang-gia-dich-vu-nha-khoa.html` và trang ưu đãi lúc chạy.
- Mọi con số gắn dấu `*` + dòng *"Hiệu quả phụ thuộc cơ địa mỗi người"*.
- Chữ **"chính hãng"** chỉ dùng cho Straumann · Invisalign · Nacera · Ormco.
- Before–after chỉ dùng case đã duyệt pháp lý.

---

## Design System Paris v2.0 — chuẩn giao hàng HTML

### Màu
| Vai trò | Mã |
|---|---|
| Primary (`--blue`) | `#0058a1` |
| Secondary | `#10B1E7` |
| Accent | `#6DCCDD` |
| Soft BG | `#E2F4FD` |
| Highlight | `#EE305B` |
| Danger | `#CF2033` |
| Text | `#1D2939` |
| Sub text | `#667085` |
| Border | `#E4E7EC` |

**Tỷ lệ bắt buộc: 80% trắng / 15% xanh / 5% accent** — **không nền toàn xanh**.
- Gradient xanh: `linear-gradient(135deg, var(--blue) 0%, #1A74B8 55%, var(--blue) 100%)`
- **Text giá:** `#ed2805`
- **Nhấn trên nền xanh:** `#ffc229`

### Typography
- Heading: **Bricolage Grotesque** (700/800)
- Body: **Oxy Vietnam** (400/500)
- Accent: **SVN Rosellinda Alyamore** — **chỉ** banner / hero / tên dịch vụ
- Line-height **150%**

### Layout
- Card radius **16–24px** · button radius **999px** hoặc **14px**
- **Shadow rất nhẹ** · khoảng trắng lớn
- CTA nổi bật sau mỗi 2–3 section
- **Mobile-first**, single-file HTML

### Phong cách
Apple + Airbnb + Stripe + Medical Premium + chuẩn Pháp.

**Không:** nền tối · quá 3 màu chính · gradient/neon mạnh · nhiều style icon lẫn lộn · card nhiều shadow · animation rối.

---

## Luồng làm việc MODE 2
1. Nhận cụm từ khóa + dịch vụ → xác định loại LDP, **nói rõ chọn A hay B và vì sao**.
2. Lấy USP / trust / bác sĩ / **đối tác hãng** từ `np-ho-so-thuong-hieu.md`; giá & KM & trả góp lấy động.
3. **Mặc định hỏi:** *"Xuất copy-deck trước, hay dựng thẳng HTML?"*
4. Dựng HTML thì tuân Design System ở trên.
