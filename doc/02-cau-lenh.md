# 02 · CÂU LỆNH — ADS OPTIMIZE (NHA KHOA PARIS)

---

# 1. Công thức ra lệnh

```
MODE [1|2|3] — [từ khóa / cụm từ khóa / số liệu].
[dịch vụ] · [giai đoạn phễu nếu biết] · [cơ sở nếu chạy local]
```

Thiếu giai đoạn phễu → Agent tự map và **nói rõ đã map vào đâu, vì sao**.

---

# 2. MODE 1 — WIN-AD

## 2.1 Một nhóm từ khóa
```
MODE 1 — từ khóa "trồng răng implant trả góp hà nội".
Chấm cổng WIN trước; qua cổng thì sinh mẫu Google RSA + Meta.
```

## 2.2 Lô từ khóa, lọc trước
```
MODE 1 — chấm cổng WIN cho danh sách này, chỉ báo cái nào qua/không qua
và vì sao. Chưa viết mẫu:
- trồng răng implant
- implant straumann giá bao nhiêu
- niềng răng invisalign có đau không
- bọc răng sứ là gì
- all on 4 cho người mất răng toàn hàm tphcm
```

## 2.3 Đánh vào nỗi sợ (giai đoạn 3)
```
MODE 1 — từ khóa "bọc răng sứ có hại răng thật không", giai đoạn 3.
Dùng archetype phá vỡ hiểu lầm. Bằng chứng ưu tiên đối tác hãng Nacera.
```

## 2.4 Đánh vào bài toán tiền (giai đoạn 4)
```
MODE 1 — "niềng răng trả góp", giai đoạn 4, đối tượng 25–35.
Nhấn trả góp + minh bạch chi phí + lộ trình rõ số buổi.
Giá để [CHỜ CẬP NHẬT].
```

## 2.5 Chạy local
```
MODE 1 — "nha khoa uy tín đà nẵng", chạy cho cơ sở Đà Nẵng.
Lấy địa chỉ tại /tim-phong-kham.html, không dùng địa chỉ cũ.
```

---

# 3. MODE 2 — LDP-BUILD

## 3.1 Dựng landing cho nhóm mất răng
```
MODE 2 — cụm từ khóa quanh "mất răng lâu năm tiêu xương", giai đoạn 3.
Xác định loại landing rồi dựng blueprint + copy.
```

## 3.2 Chỉ định rõ loại
```
MODE 2 — landing loại B (PAS) cho "răng hô nên niềng hay bọc sứ".
Phần gỡ 3 rào cản viết kỹ, nhất là nỗi ngờ về mài răng thật.
```

## 3.3 Dựng thẳng HTML
```
MODE 2 — dựng HTML single-file cho landing Invisalign, giai đoạn 4.
Theo Design System Paris v3.0, tỷ lệ 80/15/5, có sticky CTA mobile.
```

## 3.4 Thêm micro-conversion
```
MODE 2 — landing implant hiện tại ít người điền form.
Chèn công cụ "Kiểm tra trồng răng" làm bước trung gian, đề xuất đặt ở đâu.
```

---

# 4. MODE 3 — LDP-ADVISOR

## 4.1 Chẩn đoán đầy đủ
```
MODE 3 — số liệu 14 ngày, nhóm "implant trả góp HN":
ADS: impression 38.000 · CTR 3,2% · CPC 21.000đ · CPL 1.150.000đ · chi phí 41tr
GA: scroll 30% · time-on-page 24s · form view 280 · submit 19 · booking 5
Chẩn đoán và cho 3 quyết định.
```

## 4.2 Lead nhiều nhưng không đến khám
```
MODE 3 — CPL tốt (620k) nhưng chỉ 12% lead đến khám.
Vấn đề nằm ở đâu, sửa gì?
```

## 4.3 So sánh với control
```
MODE 3 — mẫu A: CTR 3,8% CPL 890k · control: CTR 3,1% CPL 1.100k.
Impression A 7.500, control 36.000. A có phải winner không?
```

---

# 5. Prompt hỏi đáp

| Mục đích | Prompt |
|---|---|
| Chấm từ khóa | `"niềng răng" được mấy điểm cổng WIN? Nên thu hẹp thế nào?` |
| Chọn giai đoạn | `"implant bao lâu thì lành" thuộc giai đoạn mấy, landing loại gì?` |
| Kiểm tra câu chữ | `Câu này có vi phạm gì không: "Răng sứ chính hãng, dùng vĩnh viễn, không đau"?` |
| Luật "chính hãng" | `Mình được dùng chữ "chính hãng" cho những gì?` |
| Chọn bằng chứng | `Giai đoạn 3 dịch vụ Implant nên dùng bằng chứng nào mạnh nhất?` |
| Thiết kế test | `Khách phản ứng với tên hãng hay với bác sĩ mạnh hơn? Thiết kế lô test.` |
| Giải thích chỉ số | `CPL thấp mà booking ít nghĩa là gì?` |

---

# 6. Prompt tinh chỉnh

```
15 headline đang thiếu nhóm gỡ nỗi sợ. Cân lại cho đủ 4 nhóm.
```
```
Hook này nghe như văn quảng cáo. Viết lại bằng đúng câu khách tự nói.
```
```
Bỏ hết chữ "chính hãng" ở chỗ không phải 4 hãng đối tác.
```
```
Thay mọi số giá bằng [CHỜ CẬP NHẬT], mình chưa lấy giá mới.
```
```
Chuyển landing này từ loại A sang loại B, giữ nguyên phần bác sĩ và trả góp.
```

---

# 7. Những gì Agent sẽ TỪ CHỐI hoặc CẢNH BÁO

| Yêu cầu | Phản hồi của Agent |
|---|---|
| "Viết Paris số 1 / tốt nhất" | Từ chối; đề xuất USP đo được (đối tác hãng · BS ĐH Y · GP Sở Y tế) |
| "Ghi niềng không đau / cam kết không biến chứng" | Từ chối; đề xuất ngôn ngữ xác suất + bằng chứng công nghệ giảm đau + dấu `*` |
| **"Ghi sứ này chính hãng cho sang"** | **Từ chối** nếu không thuộc Straumann/Invisalign/Nacera/Ormco; đây là tuyên bố pháp lý |
| "Hứa niềng xong trong 12 tháng" | Từ chối; thời gian tùy từng ca, không hứa cứng |
| "Điền đại giá implant vào" | Từ chối; `[CHỜ CẬP NHẬT]`; giá đổi theo đợt, phải lấy mới |
| "Lấy giá lần trước bạn viết" | Từ chối; số cũ có thể đã sai |
| "Bịa số ca cho hook mạnh hơn" | Từ chối; đổi archetype không cần số, hoặc dùng số có thật trong hồ sơ |
| "Thêm tên bác sĩ X" | Kiểm tra danh sách; không có → `[CHỜ CẬP NHẬT]` |
| "Viết review khách cho sinh động" | Từ chối bịa review |
| "Dùng ảnh before-after này" | Hỏi đã duyệt pháp lý + giấy đồng ý chưa |
| "So sánh trực diện với Elite Dental" | Từ chối nêu tên hạ thấp; đề xuất bộ tiêu chí khách quan |
| "Từ khóa này mình thích, cứ viết đi" | Cảnh báo < 2/3 tiêu chí; đề nghị thu hẹp bằng tên hãng/trả góp/địa điểm |
| "Xuất luôn, khỏi chấm điểm" | Cảnh báo chưa chấm WIN 12 điểm |
| "Scale mẫu này đi" (mẫu nhỏ) | Cảnh báo chưa đủ hiển thị/chi tiêu để kết luận |
| "Tư vấn luôn răng của khách này" | Từ chối chẩn đoán; mời thăm khám |
| "Gửi ảnh phim X-quang khách để viết case" | Từ chối; không nạp dữ liệu bệnh nhân lên công cụ công cộng |
