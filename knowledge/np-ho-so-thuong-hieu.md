# HỒ SƠ THƯƠNG HIỆU — NHA KHOA PARIS *(module swappable)*
Version: 2.0 — kế thừa mục 3.3 bản v1.3

> Đây là **module thương hiệu**. Đổi sang brand khác = thay file này + `np-rao-phap-ly.md`, giữ nguyên bộ não.

## Định vị
**Hệ thống Nha khoa Tiêu chuẩn Pháp đầu tiên tại Việt Nam** — chuỗi nha khoa chuyên sâu điều trị, chăm sóc & thẩm mỹ răng toàn diện.
**Slogan:** *Nụ cười mới, cuộc sống mới* / *New Smile, New Life*.

## Nhận diện thương hiệu
**Logo** (biểu tượng + chữ "Nha Khoa Paris" — đặt bên trái header, giữ safe-area, **không bóp méo / đổi màu / thêm bóng**):
- Header (màu): `https://nhakhoaparis.vn/wp-content/themes/ParisBrand2024/Module/Header/header_pr_2_0_0/images/logo.png`
- Footer (trắng, nền tối): `https://nhakhoaparis.vn/wp-content/themes/ParisBrand2024/Module/Footer/footer_pr_2_0_0/images/logo-white.png`

**Màu — Design System Paris v3.1** *(bộ nhận diện mục 4.1 + token production `family-care.html`)*

Ba màu gốc của bộ NDTH, **không được đổi**:

| Màu gốc | HEX | RGB | CMYK |
|---|---|---|---|
| **Cerulean Blue** | `#2A52BE` | 42, 82, 190 | 78, 57, 0, 25 |
| **Pantone Red 032 C** | `#ED2E38` | 237, 47, 57 | 0, 96, 82, 0 |
| **White** | `#FFFFFF` | 255, 255, 255 | 0, 0, 0, 0 |

Thang màu đầy đủ cho giao diện số — **lấy nguyên từ trang production `family-care.html`**, không tự chế biến thể mới:

| Vai trò | Mã | Dùng cho |
|---|---|---|
| `--blue` | `#2A52BE` | **Cerulean Blue — bộ NDTH.** Nút chính · heading |
| `--blue-dark` | `#152F73` | Hover / active |
| `--blue-deep` | `#0C1D4D` | Tiêu đề section · nền footer |
| `--blue-light` | `#EAF0FC` | Nền khối nhạt |
| `--blue-mid` | `#D7E2FA` | Viền · đường kẻ |
| `--red` | `#ED2E38` | **Pantone Red 032 C — bộ NDTH.** CTA · nhãn ưu đãi · giá |
| `--red-dark` | `#C11B26` | Chữ đỏ cỡ nhỏ · lỗi form (6,08 AA) |
| `--red-light` | `#FDEAEB` | Nền badge ưu đãi |
| `--cream` | `#FBF8F3` | Nền section xen kẽ với trắng |
| `--paper` | `#FFFFFF` | **White — bộ NDTH** |
| `--ink` | `#131A2E` | Chữ thường |
| `--ink-soft` | `#4A5270` | Chữ phụ |
| `--gold` | `#C9A24B` | **Chỉ trên nền navy** — trên trắng chỉ 2,40:1 |
| `--line` | `#E4E1D8` | Viền thẻ |
| nền trang | `#DCE3EE` | Xám xanh ngoài container |

**Tỷ lệ bắt buộc: 80% trắng/kem / 15% xanh / 5% đỏ** — cảm hứng cờ Pháp. **Không nền toàn xanh.**
- **Nền footer:** `linear-gradient(180deg, #0C1D4D, #0A1840)`
- **Text giá:** `#ED2E38` khi cỡ ≥ 16px đậm · `#C11B26` khi nhỏ hơn (để đạt AA)
- **Nhấn trên nền xanh:** `#FFFFFF` — trắng là màu thứ ba của bộ NDTH
- ⛔ **Không đặt đỏ lên nền xanh** (1,66:1) · **không đặt `--gold` lên nền trắng** (2,40:1)
- Khung trang đầy đủ (header · container · footer · sticky) ở `np-khung-landing.md`

**Typography — hai font, theo đúng trang production**

Heading **Bricolage Grotesque** 700 · body **Be Vietnam Pro** 400/600/700/800. Cả hai đều đủ tiếng Việt.

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Be+Vietnam+Pro:wght@400;600;700;800&display=swap" rel="stylesheet">
<link href="https://fonts.googleapis.com/css2?family=Bricolage+Grotesque:opsz,wght@12..96,700;12..96,800&display=swap" rel="stylesheet">
```

```css
body{font-family:'Be Vietnam Pro',sans-serif}
h1,h2,h3,.serif{font-family:'Bricolage Grotesque','Be Vietnam Pro',sans-serif;font-weight:700}
```

| Vai trò | Font | Weight |
|---|---|---|
| `h1` `h2` `h3` | Bricolage Grotesque | **700** (800 cho hero) |
| Body · nút · form · nhãn | Be Vietnam Pro | **400** thường · **600–700** nhấn · **800** CTA |

- Body **≥ 16px** trên mobile. Line-height 150% body · 1.32 cho tiêu đề section.
- Fallback của heading là Be Vietnam Pro — font tải chậm thì chữ vẫn đúng tiếng Việt.
- **Không nạp font thứ ba.** Cần nhấn thì đổi weight.

> ⚠️ **Đã bỏ** `Oxy Vietnam` và `SVN Rosellinda Alyamore` khỏi hệ web. Nếu ấn phẩm in vẫn dùng font chữ viết tay cho banner, ghi rõ ở đây trước khi dựng POSM.

**Giọng:** chuyên nghiệp – chuẩn Pháp – cao cấp – hiện đại – thân thiện; y khoa nhưng **không khô cứng**. Không dùng từ cấm / so sánh tuyệt đối.

## Cơ sở
Hotline **0943.776.699** (24/7) · email tuvan@nhakhoaparis.vn · cskh@nhakhoaparis.vn · giờ làm **8h30 – 18h30**.

**Trụ sở chính:** Tầng 1 + Tầng 2, số 12 Thái Thịnh, P. Đống Đa, Hà Nội.
Công ty CP Nha khoa Paris · MSDN **0111123127** · GP KCB **2032/HNO-GPHĐ/CL1** (Sở Y tế HN, 23/10/2025).

**Hệ thống cơ sở:** Hà Nội · Hải Phòng · Quảng Ninh · Vinh (Nghệ An) · Đà Nẵng · TP.HCM · Bình Dương.

> ⚠️ Địa chỉ đường phố từng cơ sở: lấy tại `/tim-phong-kham.html` khi chạy — **không dùng số/địa chỉ cũ**. Hotline campaign có thể khác số tổng đài.

## Trust / pháp lý — dùng làm bằng chứng gỡ nỗi sợ
- Giấy phép KCB **2032/HNO-GPHĐ/CL1** (Sở Y tế Hà Nội, 23/10/2025).
- **100% bác sĩ tốt nghiệp Đại học Y, có chứng chỉ hành nghề**; tuân thủ **vô khuẩn theo Bộ Y tế**.
- **Trả góp** niềng răng & bọc răng sứ.
- **Báo chí:** Afamily · Tiền Phong · Znews · 24h · Dân Trí.

### USP mạnh nhất — đối tác hãng chính hãng
| Hãng | Hạng / vai trò | Dùng cho |
|---|---|---|
| **Straumann** | Đối tác top 1 | Implant |
| **Invisalign** | **Black Diamond** | Niềng trong suốt |
| **Nacera** | Đối tác hàng đầu | Răng sứ |
| **Ormco** | Hạng **Diamond Star** | Niềng mắc cài |

> Đây là thứ đối thủ khó sao chép nhất → **bằng chứng số một để gỡ rào cản NGỜ**.
> ⚠️ Chữ **"chính hãng"** là tuyên bố pháp lý — **chỉ dùng cho 4 hãng trên**, không gắn cho vật liệu/dịch vụ khác.

### Công nghệ
- Nhổ răng siêu âm **Piezotome** — giảm đau
- Điều trị tủy **RECIPROC BLUE**
- Tẩy trắng **WhiteMax**
- Công cụ online: **Kiểm tra răng miệng / niềng / răng sứ / trồng răng** → dùng làm **micro-conversion** trước form

**Ưu tiên dùng bằng chứng theo thứ tự:** đối tác hãng chính hãng → BS ĐH Y + chứng chỉ quốc tế → giấy phép Sở Y tế → công nghệ giảm đau → bảo hành/trả góp → báo chí.

## Bác sĩ nổi bật
- **TS-BS. Đàm Ngọc Trâm** — cố vấn chuyên môn; thành viên **ESCD** (nha khoa thẩm mỹ châu Âu) · **ICOI** (implant thế giới) · hiệp hội nha sĩ Mỹ · **ITI** (Thụy Sỹ); Phó trưởng Bộ môn Phục hình RHM — Viện đào tạo RHM, ĐH Y Hà Nội.
- **BS. Hồ Hiệp Anh Tuấn** — Phó GĐ chuyên môn; **Top 1 case Invisalign 2024**.
- **BS.CKI Nguyễn Ngọc Linh** — **>5.000 ca Implant**, kỹ thuật nhanh – an toàn.

> Chỉ dùng tên bác sĩ có trong danh sách này. Tên khác → `[CHỜ CẬP NHẬT]`.

## Taxonomy dịch vụ — dùng để gom nhóm từ khóa & chọn landing

**Nha khoa thẩm mỹ**
- *Răng sứ:* bọc răng sứ thẩm mỹ · cầu răng sứ · mặt dán Veneer · răng sứ toàn hàm · răng toàn sứ · sứ kim loại
- *Chỉnh nha / Niềng:* niềng thẩm mỹ · mắc cài kim loại · mắc cài sứ · mắc cài pha lê · mặt trong · **trong suốt Invisalign**
- *Implant:* trồng răng Implant · các loại trụ · ghép xương · nâng xoang · nguyên hàm · **All-On (4/6)**

**Nha khoa tổng quát**
nhổ răng Piezotome · nhổ răng sữa trẻ em · cắt lợi trùm · tẩy trắng WhiteMax · trám thẩm mỹ · cạo vôi · đính đá · điều trị tủy RECIPROC BLUE · gói **Teeth Spa chuẩn Pháp**

**Dịch vụ giá trị lớn** (ưu tiên khi chấm tiêu chí ③ cổng WIN): **Implant · All-On 4/6 · Invisalign · răng sứ toàn hàm**.

## Đối thủ — để tạo khác biệt & chấm "cạnh tranh ít"
Elite Dental · Nha khoa Thùy Anh · Nha khoa Kim · Việt Pháp · I-Dent · Lạc Việt Intech · Parkway.

**Khi viết QC/LDP, nhấn khác biệt Paris:** chuẩn Pháp + **đối tác hãng top** (Straumann/Invisalign/Nacera/Ormco) + bác sĩ ĐH Y có chứng chỉ quốc tế.

> **Không nêu tên đối thủ để hạ thấp.** Danh sách này chỉ dùng nội bộ để chọn góc khác biệt và ước lượng mức cạnh tranh từ khóa.

## ⚠️ GIÁ & KHUYẾN MÃI = DỮ LIỆU ĐỘNG
Agent **bắt buộc** lấy tại thời điểm chạy:
- Giá: `/hoan-my-bang-gia-dich-vu-nha-khoa.html`
- Ưu đãi: trang ưu đãi hiện hành

**KHÔNG bịa. KHÔNG dùng số cũ.** Giá Implant/All-On và % ưu đãi **thay đổi theo đợt**. Không truy cập được → `[CHỜ CẬP NHẬT]` + báo người dùng. Áp cả cho **điều kiện và lãi suất trả góp**.
