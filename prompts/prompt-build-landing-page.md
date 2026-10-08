# PROMPT MẪU — dựng Landing Page (MODE 2 · LDP-BUILD)

Mặc định: **mobile-first, single-file HTML**.
Trang tham chiếu: <https://nhakhoaparis.vn/trong-rang-implant-paris.html>
Nguồn nội dung: **sheet 4 "Hành trình KH"** của workbook zone (`out/NKP _ Google Ads _ Bộ từ khoá *.xlsx`).

---

## Trang tham chiếu dùng để làm gì — và KHÔNG dùng để làm gì

| ✅ Lấy từ trang tham chiếu | ❌ Không lấy |
|---|---|
| Cách trình bày trên mobile: nhịp section, mật độ chữ, kích thước nút | **Khung nội dung.** Trang này đang chạy AIDA. Phần lớn LP của zone Implant phải là **PAS** vì xuất phát từ nỗi đau mất răng |
| Giọng thương hiệu, cách gọi tên dịch vụ | **Thứ tự section.** Thứ tự lấy từ `np-khung-landing.md` theo loại A/B |
| Cách hiển thị giá dạng card "Chỉ từ X triệu" | **Con số cứng.** Giá · số ca · năm kinh nghiệm · bảo hành đều là dữ liệu động, đọc lại lúc chạy |
| Cách chia before-after theo mức độ mất răng | **Danh sách bác sĩ.** Chỉ dùng tên có trong `np-ho-so-thuong-hieu.md` |

**Trang tham chiếu đang THIẾU 4 thứ — LP mới bắt buộc phải có:**

1. **FAQ xử lý nỗi sợ** — section 11 của khung, bắt buộc với mọi LP loại B.
2. **Công cụ kiểm tra online** làm micro-conversion trước form — lợi thế riêng của Paris.
3. **Trả góp** — rào cản NGẠI của CD6 và CD2 không được gỡ nếu thiếu.
4. **Sticky CTA mobile** — thanh CTA cố định đáy màn hình.

> Điểm đáng học của trang tham chiếu: 3 tab before-after chia theo **Mất 1 răng / Mất nhiều răng / Mất toàn hàm**
> — đúng bằng chân dung **CD1 / CD2 / CD3**. Giữ cách chia này, chỉ đổi nhãn tab sang ngôn ngữ của chân dung.

---

## 1 · PROMPT ĐẦY ĐỦ — dựng 1 landing page

> Thay 2 dòng trong ngoặc vuông. Mọi thứ còn lại Agent tự đọc từ file.

```
MODE 2 — LDP-BUILD. Dựng landing page mobile-first cho Nha khoa Paris.

LANDING:  [LP7: Hỏi đáp bác sĩ]
ZONE:     [Trồng răng Implant]  (file: zones/implant.json)

ĐỌC TRƯỚC, theo thứ tự:
  1. Sheet 4 "Hành trình KH" của workbook zone — mục B, dòng của landing này.
     Lấy đủ 7 trường: Loại khung · Chặng · Chân dung KH · Rào cản gỡ chính
     · Nội dung bắt buộc · CTA chính · Micro-conversion trước form.
  2. Sheet 4 mục A — dòng của CHẶNG tương ứng. Lấy: tâm lý & insight,
     bằng chứng BẮT BUỘC, chuyển đổi đo lường, hành động sau lead.
  3. Sheet 1 mục A — dòng của các CHÂN DUNG được gán cho landing này.
     Lấy insight là nỗi đau thật, và ai là người gõ Google.
  4. Sheet 2 — lọc cột Landing page = mã landing này. Đọc toàn bộ cột
     Từ khoá và cột Thông điệp / CTA chính. Trang phải trả lời ĐÚNG
     những câu khách đang gõ, bằng ĐÚNG thông điệp đã cam kết trên quảng cáo.
  5. knowledge/np-khung-landing.md   - 13 section loại A/B, Design System v3.0
  6. knowledge/np-ho-so-thuong-hieu.md - USP, đối tác hãng, bác sĩ, công nghệ
  7. knowledge/np-rao-phap-ly.md     - từ cấm, luật chữ "chính hãng"
  8. https://nhakhoaparis.vn/trong-rang-implant-paris.html
     - CHỈ tham khảo cách trình bày mobile và lấy số liệu động đang hiệu lực.

QUY TẮC NỘI DUNG:
  - Khung A hay B lấy theo cột "Loại khung" ở sheet 4. Nói rõ ở đầu output
    là đang dùng khung nào và vì sao, trước khi viết section đầu tiên.
  - Với loại B: SECTION 4 "Gỡ 3 rào cản" là trái tim của trang. Nó phải gỡ
    ĐÚNG rào cản ghi ở cột "Rào cản gỡ chính", không gỡ chung chung cả ba.
  - Mỗi lời hứa phải kèm 1 bằng chứng kiểm chứng được. Thứ tự ưu tiên bằng chứng:
    đối tác hãng chính hãng → bác sĩ ĐH Y có chứng chỉ quốc tế → giấy phép Sở Y tế
    → công nghệ giảm đau → bảo hành/trả góp → báo chí.
  - Nếu người gõ Google không phải người điều trị (con cái tìm cho bố mẹ),
    viết hero và section chi phí cho NGƯỜI MUA HỘ.
  - Nhúng micro-conversion đúng vị trí: sau section "Gỡ 3 rào cản" (loại B)
    hoặc sau section "Dịch vụ" (loại A). CTA form chỉ xuất hiện SAU đó.
  - CTA lặp sau mỗi 2-3 section + sticky CTA mobile + popup CTA thoát trang.

QUY TẮC MOBILE (đây là mặc định, không phải tuỳ chọn):
  - Khung thiết kế chính: 360-430px. Desktop chỉ là bản nở ra của mobile.
  - Body >= 16px (nhỏ hơn làm iOS tự zoom khi chạm vào input).
  - Vùng chạm >= 44x44px. Khoảng cách giữa 2 nút >= 8px.
  - Hero: CTA chính phải nằm trong màn hình đầu, không cần cuộn.
  - Sticky CTA đáy màn hình: 2 nút - [Gọi] và [Đặt lịch]. Hiện sau khi cuộn
    quá hero, ẩn khi form booking đang trong khung nhìn.
  - Form: 2 trường (tên, SĐT) + checkbox chính sách.
    input type="tel" inputmode="numeric" autocomplete="tel".
  - Bảng giá: card xếp dọc, KHÔNG dùng table cuộn ngang.
  - Before-after: tab hoặc swipe, không grid nhiều cột.
  - Ảnh: WebP, width/height cố định để không nhảy layout, lazy-load từ
    section 3 trở xuống. Hero là ảnh duy nhất được tải ngay.
  - Không hover-only: mọi thứ phải dùng được bằng ngón tay.
  - Tổng trang mục tiêu < 500KB, không framework, CSS inline trong file.

DESIGN SYSTEM PARIS v3.0 (bắt buộc — dẫn xuất từ bộ NDTH mục 4.1):
  - 3 màu gốc: Cerulean Blue #2A52BE · Pantone Red 032 C #ED2E38 · White #FFFFFF
  - Thang số: --blue #2A52BE · blue-dark #224298 · secondary #6382D6
    · accent #A4B3DD · soft bg #EDF0F7 · highlight #ED2E38 · danger #C3131C
    · text #1D2939 · sub #667085 · border #E4E7EC
  - Tỷ lệ 80% trắng / 15% xanh / 5% đỏ. KHÔNG nền toàn xanh, không nền tối.
  - Text giá #ED2E38 khi >=18,66px đậm, #C3131C khi nhỏ hơn.
    Nhấn trên nền xanh #FFFFFF. KHÔNG đặt đỏ lên nền xanh (tương phản 1,66:1).
  - MỘT font duy nhất: Bricolage Grotesque (variable, đủ tiếng Việt + ký tự đồng).
    Nạp đúng link Google Fonts dưới đây, không nạp font thứ hai:
    <link href="https://fonts.googleapis.com/css2?family=Bricolage+Grotesque:opsz,wght@12..96,400;12..96,500;12..96,600;12..96,700;12..96,800&display=swap" rel="stylesheet">
    H1/H2 w800 · H3/H4 w700 · nhãn và nút w600 · body nhấn w500 · body w400 >=16px.
    font-optical-sizing: auto. Line-height 150% body, 110-120% heading lớn.
  - Card radius 16-24px · button radius 999px hoặc 14px · shadow rất nhẹ.

RÀNG BUỘC PHÁP LÝ — vi phạm là loại thẳng, không tính điểm:
  - Cấm: tốt nhất · số 1 · không đau 100% · cam kết thành công · khỏi 100%
    · đẹp tuyệt đối · vĩnh viễn · duy nhất. Không hứa thời gian điều trị cứng.
  - Chữ "chính hãng" CHỈ cho Straumann (Implant) · Invisalign · Nacera · Ormco.
  - Mọi con số kết quả gắn dấu * + dòng "Hiệu quả phụ thuộc cơ địa mỗi người".
  - Chỉ dùng tên bác sĩ có trong np-ho-so-thuong-hieu.md. Tên khác → [CHỜ CẬP NHẬT].
  - Giá, ưu đãi, điều kiện trả góp: đọc tại /hoan-my-bang-gia-dich-vu-nha-khoa.html
    và trang ưu đãi hiện hành LÚC CHẠY. Không truy cập được → [CHỜ CẬP NHẬT],
    không dùng số đã nhớ, không bịa.
  - Before-after chỉ dùng case đã duyệt pháp lý. Chưa có → để placeholder ghi rõ.

TRƯỚC KHI VIẾT, hỏi tôi đúng 1 câu: xuất copy-deck trước, hay dựng thẳng HTML?

OUTPUT nếu dựng HTML: 1 file .html hoàn chỉnh, chạy được khi mở trực tiếp,
kèm bảng đối chiếu cuối output gồm 3 cột:
  Section | Phục vụ chân dung/rào cản nào | Bằng chứng đã dùng
```

---

## 2 · PROMPT NGẮN — khi đã quen

```
MODE 2. Dựng [LP7] của zone [implant], mobile-first, single-file HTML.
Lấy loại khung, chặng, chân dung, rào cản, nội dung, CTA, micro-conversion từ
sheet 4 mục B. Lấy từ khoá và thông điệp đã hứa từ sheet 2 (lọc Landing page = LP7).
Theo np-khung-landing.md + Design System Paris v3.0. Tuân np-rao-phap-ly.md.
Giá và ưu đãi đọc động. Hỏi tôi copy-deck hay HTML trước khi viết.
```

---

## 3 · PROMPT DỰNG CẢ BỘ — một zone, nhiều landing

```
Đọc sheet 4 mục B của workbook zone [implant]. Với TỪNG landing trong bảng,
lập blueprint 13 section theo đúng loại khung của nó.

Xuất 1 bảng tổng hợp trước, các cột:
  Mã LP | Loại khung | Chặng | Chân dung | Rào cản gỡ | 3 section quan trọng nhất
  | Micro-conversion | Bằng chứng chủ lực | Số từ khoá đang trỏ về (đếm ở sheet 2)

Sau bảng, chỉ ra:
  - Landing nào đang nhận từ khoá của NHIỀU chặng khác nhau → phải tách trang.
  - Landing nào chưa có từ khoá nào trỏ về → xây xong sẽ không có traffic,
    nên hoãn hay nên bổ sung từ khoá?
  - Landing nào đang gỡ cùng một rào cản bằng cùng một bằng chứng → đang trùng lặp.

Thứ tự ưu tiên dựng: theo tổng ngân sách của các chiến dịch trỏ về landing đó
(sheet 1 mục B), cao nhất làm trước.
CHƯA dựng HTML. Chờ tôi chọn landing cụ thể.
```

---

## 4 · PROMPT RÀ SOÁT — trước khi đẩy traffic

```
Đọc file landing [đường dẫn hoặc URL] và dòng tương ứng ở sheet 4 mục B.
Chấm theo 10 câu, mỗi câu ĐẠT/KHÔNG kèm dẫn chứng cụ thể trong trang:

 1. Khung A/B có khớp cột "Loại khung" ở sheet 4 không?
 2. Hero có gọi đúng nỗi đau/mong muốn của chân dung được gán không?
 3. Section "Gỡ 3 rào cản" có gỡ ĐÚNG rào cản ghi ở sheet 4 không,
    hay đang gỡ chung chung cả ba?
 4. Mọi lời hứa có bằng chứng đi kèm không? Liệt kê lời hứa chưa có bằng chứng.
 5. Thông điệp trên trang có khớp cột "Thông điệp / CTA chính" của các từ khoá
    trỏ về landing này (sheet 2) không? Lệch chỗ nào?
 6. Micro-conversion có xuất hiện TRƯỚC form booking không?
 7. Mobile: CTA hero trong màn hình đầu · sticky CTA · body >= 16px
    · vùng chạm >= 44px · bảng giá không cuộn ngang · form 2 trường type=tel.
 8. Có từ cấm quảng cáo y tế không? Trích nguyên văn nếu có.
 9. Chữ "chính hãng" có bị gắn ngoài Straumann/Invisalign/Nacera/Ormco không?
10. Giá, ưu đãi, trả góp, số ca có khớp dữ liệu đang hiệu lực không?

Kết luận: ĐƯỢC CHẠY / SỬA RỒI CHẠY / LÀM LẠI. Nếu phải sửa, liệt kê theo
thứ tự ảnh hưởng tới tỷ lệ chuyển đổi, không theo thứ tự xuất hiện trong trang.
```

---

## 5 · PROMPT ĐỐI CHIẾU TRANG ĐANG CHẠY

```
So sánh https://nhakhoaparis.vn/trong-rang-implant-paris.html với yêu cầu của
[LP4: Toàn hàm All-On 4/6] ở sheet 4 mục B.

Trả lời 4 câu:
 1. Trang hiện tại đang phục vụ chân dung nào? Đang bỏ sót chân dung nào của zone?
 2. Trang đang dùng khung nào? Sheet 4 yêu cầu khung nào? Lệch thì hệ quả là gì?
 3. 4 thứ trang hiện tại đang thiếu (FAQ · công cụ kiểm tra · trả góp
    · sticky CTA mobile) — thứ nào đáng bổ sung trước, vì sao?
 4. Nên SỬA trang hiện tại hay DỰNG trang mới riêng cho landing này?
    Nêu lý do bằng chặng và rào cản, không bằng cảm tính.

Không viết code ở bước này.
```

---

## Checklist giao hàng

**Nội dung**
- [ ] Loại khung khớp sheet 4 · nói rõ lý do ở đầu output
- [ ] Section "Gỡ 3 rào cản" gỡ đúng rào cản của chân dung được gán
- [ ] Mọi lời hứa có bằng chứng · không dùng tính từ thay bằng chứng
- [ ] Thông điệp khớp với cam kết trên quảng cáo (cột Thông điệp, sheet 2)
- [ ] Micro-conversion đứng trước form booking
- [ ] CTA lặp sau mỗi 2–3 section

**Mobile**
- [ ] CTA hero nằm trong màn hình đầu · sticky CTA đáy · popup thoát trang
- [ ] Body ≥ 16px · vùng chạm ≥ 44px · không hover-only
- [ ] Form 2 trường · `type="tel"` `inputmode="numeric"`
- [ ] Bảng giá dạng card dọc · before-after dạng tab/swipe
- [ ] Ảnh WebP có width/height · lazy-load từ section 3 · trang < 500KB

**Pháp lý** — một dòng không đạt là chặn phát hành
- [ ] Không có từ cấm · không hứa thời gian điều trị cứng
- [ ] "Chính hãng" chỉ cho Straumann · Invisalign · Nacera · Ormco
- [ ] Số kết quả có `*` + *"Hiệu quả phụ thuộc cơ địa mỗi người"*
- [ ] Tên bác sĩ có trong `np-ho-so-thuong-hieu.md`
- [ ] Giá · ưu đãi · trả góp lấy động, không dùng số cũ
- [ ] Before-after đã duyệt pháp lý
- [ ] Người có thẩm quyền duyệt trước khi chạy
