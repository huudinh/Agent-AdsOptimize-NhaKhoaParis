# CHANGELOG — ADS OPTIMIZE (NHA KHOA PARIS)

## v2.0 — 08/10/2026 · Tái cấu trúc từ 1 file thành gói chuẩn

Nội dung chuyên môn của bản `v1.3` **giữ nguyên**, chỉ tách cấu trúc theo chuẩn gói đã dùng cho [`Agent-CoXuongKhop`](../../Agent-CoXuongKhop/) và [`Agent-AdsOptimize-Kangnam`](../../Agent-AdsOptimize-Kangnam/).

**Cấu trúc mới**

```
Agent-AdsOptimize-NhaKhoaParis/
├── README.md               ← cổng vào
├── SYSTEM-PROMPT.md        ← bộ não 17 mục, khối ▼▲ (15.629 ký tự)
├── SYSTEM-PROMPT-NGAN.md   ← bản ngắn cho ChatGPT (7.952 ký tự)
├── knowledge/              ← 8 file tri thức, upload lên nền tảng
└── doc/                    ← tài liệu vận hành, KHÔNG upload
```

**Bản gốc v1.3 → mục nguồn**

| Mục bản v1.3 | Đi về đâu |
|---|---|
| 0 · Phiếu thiết kế 6 ô | `README.md` |
| 1 · ROLE · 2 · MISSION | `SYSTEM-PROMPT.md` §1 |
| 3.1 insight + 3.2 phễu | `knowledge/np-chan-dung-hanh-trinh.md` + tóm tắt ở §7 |
| **3.3 module thương hiệu** | `knowledge/np-ho-so-thuong-hieu.md` *(swappable)* |
| 3.4 cổng 2/3 | `knowledge/np-cong-win-tu-khoa.md` + tóm tắt ở §6 |
| 4 · MODE 1 (B1–B7) + 5.1 template QC | `knowledge/np-engine-win-ad.md` + tóm tắt ở §8–§9 |
| 4 · MODE 2 + 5.2 khung LDP + Design System v2.0 | `knowledge/np-khung-landing.md` + tóm tắt ở §10 |
| 4 · MODE 3 (B8–B9) + 5.3 chẩn đoán | `knowledge/np-chan-doan-chi-so.md` + tóm tắt ở §11 |
| 6 · RULES | `knowledge/np-rao-phap-ly.md` + tóm tắt ở §12, §16 |
| 7 · SELF-CHECK · 8 · KÍCH HOẠT | `SYSTEM-PROMPT.md` §17 và §5 |

Bản gốc giữ tại `doc/v1-ban-goc-1-file.md` — **không dùng để cài**.

**Bộ não viết lại thành 17 mục.** Giữ đủ lõi cũ, bổ sung:

| Mục | Nguồn |
|---|---|
| §1 Role & Mission · §5 Ba chế độ · §6 Cổng WIN · §7 Phễu · §8–§9 Engine · §10 LDP · §11 Advisor · §12 Guardrails · §17 Tự kiểm | có ở v1.3, giữ nguyên lõi |
| **§2 Bảng tri thức** — 7 file, thứ tự đọc pháp lý trước | **MỚI** |
| **§3 Định danh thương hiệu** — gộp định vị + Design System + USP đối tác hãng | **MỚI** |
| **§4 Nguyên tắc tối thượng** — bằng chứng thay tính từ + phép thử | **MỚI** |
| **§13 Giá & KM & trả góp là dữ liệu động** — mục riêng, cấm dùng số cũ đã nhớ | nâng từ ghi chú trong 3.3 |
| **§14 Định dạng đầu ra** — 6 phần cho MODE 1 | **MỚI** |
| **§15 Khi thiếu dữ liệu + người dùng không chuyên** | **MỚI** |
| **§16 Rules 11 điều** | mở rộng từ mục 6 |

**Ràng buộc mới làm rõ trong bản này**
- **Chữ "chính hãng" là tuyên bố pháp lý** (Rule 5) — chỉ dùng cho **Straumann · Invisalign · Nacera · Ormco**; không gắn cho vật liệu khác, không suy diễn "đối tác hãng X" thành "mọi dịch vụ dùng hàng hãng X". Dùng sai = **tự động 0 điểm** ở tiêu chí tuân thủ của B7 → loại thẳng mẫu. Bản v1.3 có liệt kê đối tác hãng nhưng **chưa có luật dùng chữ này**, mà đây là rủi ro pháp lý thật của ngành nha khoa.
- **Không hứa thời gian điều trị cứng** ("niềng xong trong 12 tháng") — thời gian tùy từng ca.
- **Không dùng số giá/KM cũ đã nhớ** (Rule 4) — bản cũ chỉ cấm "bịa", chưa cấm tái dùng số từ phiên trước. Giá Implant/All-On đổi theo đợt nên đây là lỗ thật.
- **Chu kỳ quyết định dài:** khi có dữ liệu booking, MODE 3 đọc **CPL → booking rate** thay vì chỉ CPL. Nha khoa khác thẩm mỹ ở chỗ lead rẻ chưa chắc là lead tốt.
- **Micro-conversion** — công cụ "Kiểm tra răng miệng/niềng/răng sứ/trồng răng" được nâng từ một dòng gợi ý thành bước thiết kế chính thức trong khung landing, vì nó hạ đúng rào cản NGẠI của giai đoạn 3.

**Tài liệu vận hành mới (`doc/`)**
- `01-cai-dat.md` — tên & mô tả · cài 3 nền tảng · **10 smoke test** (có test riêng cho "chính hãng" và cho hứa thời gian cứng) · **13 ca xử lý sự cố**.
- `02-cau-lenh.md` — câu lệnh 3 mode · prompt hỏi đáp · **16 yêu cầu Agent sẽ từ chối**.
- `03-output-mau.md` — output mẫu đủ 7 phần cho MODE 1, trích MODE 2 và MODE 3 · 4 dấu hiệu đúng / 4 dấu hiệu sai.
- `04-prompt-nguoi-moi.md` — 10 prompt cho người chưa quen thuật ngữ ads.

---

## ⚠️ Ràng buộc kỹ thuật cần biết khi sửa

**Bản ngắn chỉ còn dư 48 ký tự** so với hạn mức 8.000 của ChatGPT Custom GPT (hiện 7.952).

Gói Paris có nhiều luật cứng hơn gói Kangnam — thêm luật "chính hãng", thêm 4 tên hãng đối tác, thêm Design System riêng — nên bản ngắn đã phải nén sát. Chi tiết tra cứu được (bảng màu đầy đủ · 8 archetype · ma trận A/B T1–T5 · bảng chẩn đoán) đã **đẩy hết về `knowledge/`**, bản ngắn chỉ giữ luật không được phá.

**Nếu sửa bản ngắn: phải đếm lại ký tự khối ▼▲ trước khi dán.** Vượt 8.000 thì ChatGPT cắt phần cuối **mà không báo lỗi** — và phần cuối hiện là mục tự kiểm + quy tắc phản hồi.

---

## v1.3 — bản gốc một file

- v1.0 — clone từ bản Kangnam; chuẩn HCI R·M·K·W·O + Rules; BRAIN brand-neutral + MODULE thương hiệu (3.3); MODE 2 tuân Design System Nha Khoa Paris v2.0.
- v1.1 — tích hợp Engine WIN (B1–B9) vào MODE 1/3 + cổng 2/3 tiêu chí (3.4).
- v1.2 — bổ sung Nhận diện thương hiệu (logo · địa chỉ · màu) vào 3.3.
- **v2.2** — Design System Paris **v3.0**: thay bảng màu bằng bộ nhận diện thương hiệu mục 4.1 (Cerulean Blue `#2A52BE` · Pantone Red 032 C `#ED2E38` · White), dẫn xuất thang phụ và kiểm WCAG; typography chuyển sang **một font `Bricolage Grotesque`** (bỏ Oxy Vietnam và SVN Rosellinda Alyamore). Thêm **MODE 4 — KEYWORD-ZONE** (§12) + knowledge `np-ppl-kh-trung-tam.md`. Chuẩn **ô ảnh tạm**: ảnh chưa có thì dựng khối viền đứt ghi rõ tỉ lệ và nội dung cần cấp, kèm **bảng kê ảnh cần cấp** cuối mỗi landing — thay cho ảnh stock/AI. Thêm `prompts/prompt-quy-trinh-tron-goi.md` — dây chuyền 6 bước nối MODE 4 → MODE 1 → MODE 2 với 3 chốt dừng và luật **message match**.
- **v2.3** — Design System **v3.1**: token màu và **khung trang** (nền · container 460px · header · footer navy + khối pháp lý · sticky CTA) lấy nguyên từ trang production `family-care.html` (lưu tại `template/`). Typography sửa thành **hai font**: heading Bricolage Grotesque 700, body Be Vietnam Pro — khớp production, thay cho giả định một font ở v2.2.

- v1.3 — chốt mã màu: gradient xanh, text giá `#ed2805`, nhấn trên nền xanh `#ffc229`.

---

## Việc còn treo

| Hạng mục | Ảnh hưởng |
|---|---|
| **Giấy xác nhận nội dung quảng cáo** từng chiến dịch | **Chặn cứng** việc bật chiến dịch |
| **Văn bản chứng minh quan hệ đối tác từng hãng** | Chưa có thì mỗi lần dùng chữ "chính hãng" đều phải chờ pháp chế duyệt riêng — làm chậm toàn bộ quy trình |
| Kho case + ảnh before–after đã duyệt pháp lý | Bằng chứng mạnh nhất của giai đoạn 3 chưa dùng được |
| Địa chỉ đường phố từng cơ sở | Chạy local phải tra `/tim-phong-kham.html` thủ công mỗi lần |
| Điều kiện & lãi suất trả góp hiện hành | Trục "bài toán tiền" của giai đoạn 4 đang thiếu số cụ thể |
| Benchmark CTR/CPL/CVR + **booking rate** theo dịch vụ | MODE 3 phải lấy control hiện tại làm mốc; chưa đo được lead tốt hay xấu |
| Thư viện hook thắng tích lũy | B9 chưa có dữ liệu để tái sử dụng |
