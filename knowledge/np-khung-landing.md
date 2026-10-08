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
- **Chưa có ảnh thật → dựng ô ảnh tạm** theo mẫu ngay dưới, **không dùng ảnh stock/AI**.

---

## Ô ảnh tạm — bắt buộc khi chưa có ảnh thật

**Không bao giờ** chèn ảnh stock, ảnh AI, hay `<img>` trỏ tới URL không tồn tại. Chưa có ảnh thật đã duyệt → dựng **ô ảnh tạm** đúng mẫu dưới đây. Ô này vừa giữ đúng bố cục, vừa là phiếu đặt hàng cho người cấp ảnh.

```css
.ph{display:grid;place-content:center;gap:6px;text-align:center;margin:0;padding:16px;
    aspect-ratio:var(--ar,16/9);background:var(--blue-light,#EAF0FC);border:2px dashed var(--blue-mid,#D7E2FA);
    border-radius:16px;color:#667085;font-size:14px;line-height:1.45}
.ph b{display:block;font-weight:600;color:var(--blue,#2A52BE)}
```

```html
<figure class="ph" style="--ar:16/9">
  <b>Ảnh 16:9</b>
  Case toàn hàm trước–sau · phục vụ CD2 · cần giấy đồng ý + pháp chế duyệt
</figure>
```

**Dòng mô tả phải nói rõ ảnh đó LÀ GÌ**, không viết chung chung "ảnh minh hoạ". Tối thiểu gồm: nội dung · chân dung hoặc section nó phục vụ · điều kiện pháp lý nếu là case thật.

| Vị trí | `--ar` | Ghi chú |
|---|---|---|
| Hero | `4/5` mobile · `16/9` desktop | Ảnh duy nhất được tải ngay, không lazy-load |
| Before–after | `1/1` | Cặp 2 ô cạnh nhau hoặc tab/swipe |
| Chân dung bác sĩ | `3/4` | Chỉ bác sĩ có trong hồ sơ thương hiệu |
| Công nghệ · thiết bị · cơ sở | `16/9` | Ảnh thật của hệ thống |
| Logo hãng đối tác | tự do | Cao 40–56px, nền trắng |
| Icon | `1/1` | 48px, một bộ icon duy nhất |

**Cuối mỗi landing page phải kèm BẢNG KÊ ẢNH CẦN CẤP** — liệt kê từng ô tạm: section · tỉ lệ · nội dung cần · ai duyệt. Không có bảng này thì trang coi như chưa giao xong.

---

## Design System Paris v3.1 — chuẩn giao hàng HTML

**Trang mẫu chuẩn: `https://nhakhoaparis.vn/family-care.html`** (bản lưu: `template/family-care.html`).
Token và khung trang dưới đây lấy **nguyên** từ trang đó — không tự chế biến thể mới.

### Token màu

```css
:root{
  --blue:#2A52BE; --blue-dark:#152F73; --blue-deep:#0C1D4D;
  --blue-light:#EAF0FC; --blue-mid:#D7E2FA;
  --red:#ED2E38;  --red-dark:#C11B26;  --red-light:#FDEAEB;
  --cream:#FBF8F3; --paper:#FFFFFF;
  --ink:#131A2E;   --ink-soft:#4A5270;
  --gold:#C9A24B;  --line:#E4E1D8;
  --radius:22px;
  --shadow-soft:0 18px 40px -18px rgba(12,29,77,.28);
  --shadow-card:0 10px 30px -12px rgba(19,26,46,.18);
}
```

`--blue` và `--red` chính là hai màu gốc của bộ nhận diện (mục 4.1); phần còn lại là biến thể đã chạy thật trên production.

| Luật | |
|---|---|
| **Tỷ lệ** | 80% trắng/kem · 15% xanh · 5% đỏ. **Không nền toàn xanh** |
| **Nền trang** | `#DCE3EE` — xám xanh, để khối trắng ở giữa nổi lên như một thẻ |
| **Nút đỏ** | Chữ trắng trên `--red` chỉ đạt 4,16:1 → chữ **≥16px đậm**. Chữ đỏ cỡ nhỏ dùng `--red-dark` (6,08 AA) |
| ⛔ **Cấm** | Đỏ trên nền xanh (1,66:1) · `--gold` trên nền trắng (2,40:1 — chỉ dùng trên navy, 6,74 AA) |

### Khung trang — nền, container, header, footer, sticky

Mọi LDP dùng **đúng bộ khung này**, chỉ thay phần `<section>` ở giữa.

```css
*{box-sizing:border-box} html{scroll-behavior:smooth}
body{margin:0;font-family:'Be Vietnam Pro',sans-serif;color:var(--ink);
     background:#DCE3EE;-webkit-font-smoothing:antialiased}
img{max-width:100%;display:block}

/* container: thẻ trắng khổ điện thoại, căn giữa trên nền xám xanh */
.device-shell{max-width:460px;margin:0 auto;background:var(--paper);min-height:100vh;
  position:relative;overflow:hidden;
  box-shadow:0 0 0 1px rgba(12,29,77,.06),0 40px 80px -30px rgba(12,29,77,.35)}

/* header */
.topbar{display:flex;align-items:center;justify-content:center;
  padding:8px 18px;background:#fff;position:relative;z-index:5}
.logo-slot{display:flex;align-items:center;justify-content:center;width:120px}
.logo-slot.compact{width:90px}
.logo-slot.on-dark{filter:brightness(0) invert(1)}
.logo-slot img{width:100%;height:auto;aspect-ratio:300/121;display:block}

/* dải cờ Pháp — đặt ngay dưới hero */
.tricolor{height:5px;display:flex;width:100%}
.tricolor span{flex:1}
.tricolor span:nth-child(1){background:var(--blue)}
.tricolor span:nth-child(2){background:#fff}
.tricolor span:nth-child(3){background:var(--red)}

/* section: nền xen kẽ trắng / kem */
section{padding:46px 22px;position:relative}
.bg-white{background:#fff}
.bg-cream{background:var(--cream)}
.sec-title{font-size:23px;font-weight:700;line-height:1.32;
  color:var(--blue-deep);margin:0 0 20px;text-align:center}

/* footer: khối navy + khối pháp lý */
.footer{padding:36px 22px 24px;text-align:center}
.bg-navy{background:linear-gradient(180deg,var(--blue-deep),#0A1840);color:#fff}
.footer .tagline{font-size:12px;letter-spacing:.1em;text-transform:uppercase;
  font-weight:700;color:#AFC2F2;margin-bottom:18px}
.footer-hotline{display:inline-flex;align-items:center;gap:8px;
  background:rgba(255,255,255,.08);border:1px solid rgba(255,255,255,.18);
  padding:10px 18px;border-radius:100px;font-weight:800;font-size:15px;margin-bottom:20px}
.footer-hotline svg{width:16px;height:16px;color:var(--red)}
.footer-branches{font-size:12px;color:#9FB1DE;line-height:1.9;max-width:300px;margin:0 auto 22px}
.legal{background:#0A1840;color:#9FB1DE;font-family:Arial,Helvetica,sans-serif;
  font-size:11.5px;line-height:1.7;text-align:center;padding:4px 22px 110px} /* 110px chừa chỗ sticky */
.legal .policy{display:flex;flex-wrap:wrap;justify-content:center;gap:4px 10px;margin-bottom:8px}
.legal .policy a{color:#ADEAFF}
.legal .policy a:not(:last-child)::after{content:"|";color:rgba(255,255,255,.3);margin-left:10px}
.legal p{margin:0 0 2px}

/* sticky CTA */
.sticky-bar{position:fixed;bottom:0;left:50%;transform:translate(-50%,0);
  width:100%;max-width:460px;display:flex;align-items:center;justify-content:space-between;
  gap:12px;background:rgba(255,255,255,.92);backdrop-filter:blur(10px);
  border-top:1px solid var(--line);padding:11px 16px;z-index:20;
  box-shadow:0 -10px 30px -14px rgba(12,29,77,.3);transition:transform .35s ease}
.sticky-bar.hide{transform:translate(-50%,100%)}
.sticky-cta{display:flex;align-items:center;gap:7px;background:var(--red);color:#fff;
  font-weight:800;font-size:13.5px;padding:12px 18px;border-radius:12px;border:none;
  white-space:nowrap;box-shadow:0 10px 20px -8px rgba(237,46,56,.55)}
```

```html
<body>
<div class="device-shell" id="top">

  <div class="topbar">
    <div class="logo-slot"><img src="LOGO.png" alt="Nha khoa Paris" width="120" height="48"></div>
  </div>

  <div class="hero"><!-- ảnh hero full-width, fetchpriority="high" --></div>
  <div class="tricolor"><span></span><span></span><span></span></div>

  <!-- ===== phần thay đổi theo từng LDP: các <section> xen kẽ bg-white / bg-cream ===== -->
  <section class="bg-cream"><h2 class="sec-title">TIÊU ĐỀ SECTION</h2>…</section>
  <section class="bg-white">…</section>
  <!-- ===== hết phần thay đổi ===== -->

  <div class="footer bg-navy">
    <div class="logo-slot on-dark" style="margin:0 auto 16px"><img src="LOGO.png" alt="" width="120" height="48"></div>
    <p class="tagline">HỆ THỐNG CHUỖI NHA KHOA UY TÍN TẠI VIỆT NAM</p>
    <a href="tel:0943776699" class="footer-hotline">Hotline: 0943.776.699</a>
    <p class="footer-branches">Cơ sở: Hà Nội - Hải Phòng - Vinh - Đà Nẵng - TP.HCM - Quảng Ninh - Bình Dương</p>
  </div>

  <div class="legal">
    <div class="policy">
      <a href="https://nhakhoaparis.vn/chinh-sach-bao-mat-thong-tin-khach-hang-tai-nha-khoa-paris">Chính sách bảo mật</a>
      <a href="https://nhakhoaparis.vn/chinh-sach-noi-dung">Chính sách nội dung</a>
      <a href="https://nhakhoaparis.vn/dieu-khoan-su-dung">Điều khoản sử dụng</a>
    </div>
    <p>Công ty Cổ phần Nha khoa Paris</p>
    <p>Trụ sở chính: Tầng 1 + Tầng 2, số 12 phố Thái Thịnh, Phường Đống Đa, Thành phố Hà Nội, Việt Nam</p>
    <p>Mã số doanh nghiệp: 0111123127</p>
    <p>Giấy phép hoạt động khám bệnh, chữa bệnh số: 2032/HNO-GPHĐ/CL1 do Sở Y tế TP. Hà Nội cấp ngày 23/10/2025</p>
    <p>Chịu trách nhiệm nội dung: Công ty Cổ phần Nha khoa Paris</p>
  </div>

  <div class="sticky-bar" id="stickyBar">
    <div class="logo-slot compact"><img src="LOGO.png" alt="" width="90" height="36"></div>
    <button class="sticky-cta" onclick="document.getElementById('form').scrollIntoView({behavior:'smooth'})">ĐẶT LỊCH NGAY</button>
  </div>

</div>
</body>
```

**Luật khung trang**
- Khối pháp lý `.legal` có `padding-bottom:110px` — **chừa chỗ cho sticky bar**, bỏ đi là chữ bị che.
- `.sticky-bar` phải cùng `max-width:460px` với `.device-shell`, nếu không sẽ lệch trên desktop.
- Sticky mặc định là **logo + 1 CTA đỏ**. Cần nút gọi thì thay logo bằng nút gọi viền xanh, **không nhồi 3 thứ**.
- Dải `.tricolor` đặt ngay dưới hero, **không lặp lại** ở giữa trang.
- Thông tin pháp lý trong `.legal` là **bắt buộc**, chép đúng nguyên văn, không rút gọn.

### Typography — hai font

| Vai trò | Font | Weight |
|---|---|---|
| `h1` `h2` `h3` `.serif` | **Bricolage Grotesque** | 700 |
| Toàn bộ body, nút, form | **Be Vietnam Pro** | 400 · 600 · 700 · 800 |

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Be+Vietnam+Pro:wght@400;600;700;800&display=swap" rel="stylesheet">
<link href="https://fonts.googleapis.com/css2?family=Bricolage+Grotesque:opsz,wght@12..96,700;12..96,800&display=swap" rel="stylesheet">
```

```css
h1,h2,h3,.serif{font-family:'Bricolage Grotesque','Be Vietnam Pro',sans-serif;font-weight:700}
```

- Body **≥16px** trên mobile. Line-height 150% body, 1.32 cho `.sec-title`.
- Fallback của heading là Be Vietnam Pro — font tải chậm thì chữ vẫn đúng tiếng Việt.
- **Không nạp font thứ ba.** Cần nhấn thì đổi weight.

### Layout
- Card radius **22px** (`--radius`) · button radius **12px** · shadow dùng `--shadow-soft` / `--shadow-card`
- `section` padding **46px 22px** · tiêu đề section căn giữa
- Nền section **xen kẽ** `bg-white` ↔ `bg-cream`
- Mobile-first, single-file HTML, khung thiết kế 360–430px

### Phong cách
Apple + Airbnb + Stripe + Medical Premium + chuẩn Pháp.

**Không:** nền tối toàn trang · quá 3 màu chính · gradient/neon mạnh · nhiều style icon lẫn lộn · card nhiều shadow · animation rối.

---

## Luồng làm việc MODE 2
1. Nhận cụm từ khóa + dịch vụ → xác định loại LDP, **nói rõ chọn A hay B và vì sao**.
2. Lấy USP / trust / bác sĩ / **đối tác hãng** từ `np-ho-so-thuong-hieu.md`; giá & KM & trả góp lấy động.
3. **Mặc định hỏi:** *"Xuất copy-deck trước, hay dựng thẳng HTML?"*
4. Dựng HTML thì tuân Design System ở trên.
