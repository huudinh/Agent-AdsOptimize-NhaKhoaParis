# 01 · CÀI ĐẶT — ADS OPTIMIZE (NHA KHOA PARIS)

---

# 0. Tên & mô tả ngắn — dán vào form

**Tên:**
```
Ads Optimize Nha Khoa Paris
```

**Mô tả — bản đủ:**
```
Chuyên gia tối ưu quảng cáo hiệu suất ngành nha khoa cho Nha khoa Paris: từ từ khóa sinh mẫu quảng cáo Google và Meta, dựng landing page, và đọc số liệu ADS + GA để chỉ ra nên đổi từ khóa, làm lại landing hay sửa mẫu. Làm theo chỉ số, không theo cảm tính. Tự tránh câu vi phạm quảng cáo y tế, không bịa giá hay khuyến mãi.
```

**Mô tả — bản 1 dòng:**
```
Tối ưu quảng cáo nha khoa: sinh mẫu QC từ từ khóa, dựng landing page, chẩn đoán số liệu ADS và GA.
```

> Mô tả **không thay thế** Instructions.

---

# 1. Cài lên nền tảng

## ChatGPT (Custom GPT) — ⚠ dùng BẢN NGẮN
Ô **Instructions** giới hạn **8.000 ký tự**, mà `SYSTEM-PROMPT.md` dài **15.629 ký tự** → dán vào sẽ **bị cắt mất nửa sau** mà ChatGPT **không báo lỗi gì**.

1. Create a GPT → tab *Configure*.
2. **Name** + **Description:** dán từ §0.
3. **Instructions:** dán khối ▼▲ của [`SYSTEM-PROMPT-NGAN.md`](../SYSTEM-PROMPT-NGAN.md) (**7.952 ký tự**).
4. **Knowledge:** upload **8 file** trong `knowledge/` **+ thêm cả `SYSTEM-PROMPT.md`**.

> ⚠️ **Bản ngắn chỉ dư 48 ký tự so với hạn mức.** Nếu bạn sửa bản ngắn, **phải đếm lại ký tự** trước khi dán — thêm một câu là vượt, và phần bị cắt sẽ là mục cuối (quy tắc phản hồi + tự kiểm).

## Gemini (Gems)
1. Gem mới → **Tên** + **Nội dung mô tả** từ §0.
2. **Chỉ dẫn:** dán khối ▼▲ của [`SYSTEM-PROMPT.md`](../SYSTEM-PROMPT.md) — bản đầy đủ.
3. **Tri thức:** upload 8 file trong `knowledge/`.

## Claude (Project)
1. New project → tên từ §0.
2. **Instructions:** dán khối ▼▲ của [`SYSTEM-PROMPT.md`](../SYSTEM-PROMPT.md) — bản đầy đủ.
3. **Project knowledge:** add 8 file trong `knowledge/`.

| Nền tảng | Dán vào Instructions | Upload lên Knowledge |
|---|---|---|
| **ChatGPT** | `SYSTEM-PROMPT-NGAN.md` (7.976) | 8 file `knowledge/` **+ `SYSTEM-PROMPT.md`** |
| **Gemini** | `SYSTEM-PROMPT.md` (19.690) | 8 file `knowledge/` |
| **Claude** | `SYSTEM-PROMPT.md` (19.690) | 8 file `knowledge/` |

---

# 2. Bảy file tri thức

| File | Vai trò |
|---|---|
| `np-rao-phap-ly.md` | **Chốt chặn pháp lý — BẮT BUỘC rà mọi output**, gồm luật chữ "chính hãng" |
| `np-ho-so-thuong-hieu.md` | Module thương hiệu *(thay file này = đổi brand)* |
| `np-chan-dung-hanh-trinh.md` | 3 rào cản đặc thù nha khoa · phễu 6 giai đoạn |
| `np-cong-win-tu-khoa.md` | Cổng 2/3 · phiếu chấm · gom nhóm |
| `np-engine-win-ad.md` | B1–B7 · 8 archetype · ma trận A/B · chấm 12 · template QC |
| `np-khung-landing.md` | Khung LDP A/B · Design System Paris v3.0 · micro-conversion |
| `np-chan-doan-chi-so.md` | WIN bằng số · bảng chẩn đoán · thư viện hook |

Thứ tự đọc: **pháp lý trước, dữ liệu sau.**

> **Không upload thư mục `doc/`** — tài liệu cho người đọc. Đặc biệt **không upload `doc/v1-ban-goc-1-file.md`**: bản cũ, nạp vào sẽ mâu thuẫn với bộ não mới.

---

# 3. Smoke test sau khi cài

| # | Câu lệnh | Kỳ vọng |
|---|---|---|
| 1 | `Bạn là ai? Nêu 3 mode và cổng WIN.` | WIN-AD · LDP-BUILD · LDP-ADVISOR + cổng 2/3 tiêu chí |
| 2 | `Từ khóa "nha khoa" — sinh mẫu quảng cáo.` | **Loại ở tiền lọc** (quá rộng), đề nghị thu hẹp — **không viết mẫu** |
| 3 | `Viết headline: Paris số 1 Việt Nam, niềng không bao giờ đau.` | **Từ chối**, chỉ ra từ cấm, đề xuất bản thay bằng bằng chứng (2032/HNO-GPHĐ/CL1 · BS ĐH Y · Piezotome) |
| 4 | `Giá trồng răng implant bao nhiêu? Viết vào quảng cáo luôn.` | `[CHỜ CẬP NHẬT]`, nói rõ giá là dữ liệu động lấy tại `/hoan-my-bang-gia-dich-vu-nha-khoa.html` |
| 5 | `Viết: răng sứ của mình là sứ cao cấp chính hãng nhập khẩu.` | **Cảnh báo** — "chính hãng" chỉ dùng cho Straumann · Invisalign · Nacera · Ormco; sứ khác phải ghi `[CHỜ CẬP NHẬT]` |
| 6 | `Từ khóa "trồng răng implant" — chấm cổng WIN.` | Trượt tiêu chí ② (cạnh tranh cao), đề nghị thu hẹp bằng tên hãng / trả góp / địa điểm |
| 7 | `Khách giai đoạn 3 lo gì? Dùng landing loại nào?` | Sợ đau/mài răng + **ngờ trụ-sứ chính hãng** → **loại B (PAS)** |
| 8 | `CTR 3,5% nhưng form submit 0,3%, scroll 28%. Chẩn đoán.` | Traffic vào nhưng landing không chốt → **làm lại LDP**; gợi ý chèn công cụ kiểm tra làm micro-conversion |
| 9 | `Mình có 120 impression, mẫu A hơn B. Scale A nhé?` | **Cảnh báo mẫu quá nhỏ** — chưa đủ kết luận winner |
| 10 | `Niềng xong trong 12 tháng đúng không, viết vào ads.` | **Từ chối hứa thời gian cứng** — tùy từng ca |

Sai câu 3, 4, 5 → kiểm tra đã upload `np-rao-phap-ly.md` và `np-ho-so-thuong-hieu.md` chưa.

---

# 4. Luồng vận hành

```
Người chạy ads  →  gửi từ khóa / số liệu
    ↓
ADS OPTIMIZE    →  cổng WIN 2/3 → engine B1–B7 → chấm ≥10/12 → xuất kèm kế hoạch test
    ↓
PHÁP CHẾ        →  rà từ cấm · claim · "chính hãng" · before-after · giấy xác nhận nội dung QC
    ↓
NGƯỜI PHỤ TRÁCH →  duyệt → chạy
    ↓
SAU 1 LÔ        →  gom số liệu ADS + GA → MODE 3 → quyết định
    ↓
            (quay lại vòng lặp, giữ 1–2 challenger mới mỗi lô)
```

**Không có mẫu nào đi thẳng từ Agent ra chiến dịch.**

---

# 5. Xử lý sự cố

| Triệu chứng | Nguyên nhân | Cách xử lý |
|---|---|---|
| Agent viết mẫu ngay, bỏ qua cổng WIN | Chưa nạp `np-cong-win-tu-khoa.md` | Nhắc §6: chấm cổng 2/3 trước, xuất phiếu chấm kể cả khi loại |
| Agent dùng "số 1", "cam kết", "không đau" | Chưa nạp `np-rao-phap-ly.md` | Upload lại; nhắc §12 + bảng từ cấm |
| **Agent gắn "chính hãng" bừa bãi** | Bỏ qua luật tuyên bố pháp lý | Nhắc §12 Rule 5: chỉ Straumann · Invisalign · Nacera · Ormco |
| Agent tự điền giá / % ưu đãi / lãi suất trả góp | Bỏ qua rule dữ liệu động | Nhắc §13: lấy tại trang bảng giá lúc chạy, không dùng số cũ |
| Agent hứa "niềng xong trong X tháng" | Bỏ qua luật thời gian điều trị | Nhắc: không hứa thời gian cứng, tùy từng ca |
| Hook nhạt, nghe như văn marketing | Bỏ bước B1 | Yêu cầu rút 3–5 câu nói nguyên văn của khách kèm nguồn |
| Mẫu QC xuất ra mà không có bảng chấm | Bỏ bước B7 | Nhắc: chấm 12 điểm, <10 thì sửa rồi chấm lại |
| Test đổi nhiều thứ cùng lúc | Bỏ ma trận A/B | Nhắc §9: đổi đúng 1 biến mỗi lô |
| Kết luận winner khi dữ liệu còn ít | Bỏ điều kiện mẫu tối thiểu B8 | Nhắc: chưa đủ thì nói "chưa đủ dữ liệu" |
| Landing loại A dùng cho từ khóa nỗi sợ | Chọn sai loại LDP | Nhắc: intent từ nỗi đau → **loại B (PAS)** |
| Chỉ chạy từ khóa đầu ngành, CPC cao | Không thu hẹp từ khóa | Nhắc `np-cong-win-tu-khoa.md`: thu hẹp bằng tên hãng / trả góp / địa điểm / tình huống |
| Trả lời đầy thuật ngữ | Bỏ khối người dùng không chuyên | Nhắc: *"Nói đơn giản thôi, mình mới chạy ads"* |
| Dán bản ngắn vào ChatGPT bị cắt | Đã sửa bản ngắn làm vượt 8.000 | Đếm lại ký tự khối ▼▲; cắt bớt phần đã có trong knowledge |
