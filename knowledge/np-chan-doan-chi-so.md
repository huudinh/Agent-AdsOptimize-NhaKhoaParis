# CHẨN ĐOÁN CHỈ SỐ → QUYẾT ĐỊNH (MODE 3)
Version: 2.0 — kế thừa mục 5.3 + B8–B9 bản v1.3

## B8 · Định nghĩa WIN bằng số

Chưa có benchmark của team → **lấy control hiện tại làm mốc**.
→ Ad nào **CTR cao hơn control** VÀ **CPL thấp hơn control**, trong **cùng điều kiện** (cùng nhóm từ khóa, cùng khung giờ, cùng ngân sách tương đối) = **winner**.

**Chỉ kết luận khi đủ lượng hiển thị / chi tiêu tối thiểu.** Mẫu nhỏ thì mọi chênh lệch đều có thể là nhiễu — nói rõ *"chưa đủ dữ liệu để kết luận"* thay vì chọn bừa. Đây là lỗi tốn tiền nhất trong tối ưu ads.

**Lưu ý riêng ngành nha khoa:** chu kỳ quyết định dài hơn thẩm mỹ — khách Implant/Invisalign thường cân nhắc nhiều tuần. **CPL thấp chưa chắc là thắng** nếu lead không ra booking. Khi có dữ liệu booking, ưu tiên đọc **CPL → booking rate** thay vì chỉ CPL.

**Số liệu cần có:**
- **ADS:** CTR · CPC · CPL · chi phí · impression · từ khóa
- **GA:** scroll depth · time-on-page · form view → submit · booking
- **Nếu có:** tỷ lệ lead → đến khám → chốt điều trị

Thiếu chỉ số nào → nói rõ **thiếu gì** và **kết luận nào chưa đưa ra được**.

---

## Bảng triệu chứng → chẩn đoán → quyết định

| Triệu chứng số liệu | Chẩn đoán | Quyết định |
|---|---|---|
| **CTR thấp + impression cao** | Ad/hook yếu hoặc sai đối tượng | Sửa mẫu QC (MODE 1) — **chưa đụng landing** |
| **CTR cao + CVR/form thấp + scroll nông** | Traffic vào nhưng landing không chốt | **Làm lại LDP** — đổi hook hero / CTA / phần gỡ nỗi sợ |
| **CPC cao + cạnh tranh cao + CPL xấu** | Từ khóa đắt / sai intent | **Đổi hoặc thu hẹp từ khóa** — ngách/local theo cơ sở, hoặc từ khóa theo hãng |
| **CVR ổn nhưng CPL vẫn cao** | Giá thầu / phân bổ ngân sách sai | **Giữ landing**, tối ưu bidding + ngân sách |
| **Form view cao, submit thấp** | Form rườm rà hoặc thiếu niềm tin tại chỗ điền | Rút gọn form + thêm trust (**đối tác hãng / bảo hành**) cạnh nút; cân nhắc chèn **công cụ kiểm tra online** làm micro-conversion |
| **Nỗi đau nhóm ≠ khung landing** | Sai **loại LDP** | **Chuyển A↔B** |
| **Lead nhiều nhưng không đến khám** | Lead chất lượng thấp, hoặc kỳ vọng giá bị lệch | Xem lại thông điệp giá/trả góp trên landing; cân nhắc lọc intent chặt hơn ở từ khóa |

**Mỗi dòng khi xuất phải kèm đủ 4 thứ:**
① ngưỡng cụ thể đang vi phạm · ② lý do dựa trên số · ③ action tiếp theo · ④ chỉ số cần theo dõi sau khi sửa.

---

## Ba quyết định của MODE 3

**① Đổi từ khóa?**
Khi intent lệch landing, hoặc CTR thấp + CPC cao + cạnh tranh cao.
→ Quay về `np-cong-win-tu-khoa.md`. Với nha khoa, hướng thu hẹp hiệu quả nhất: **thêm tên hãng** (implant straumann) · **thêm "trả góp"** · **thêm địa điểm** · **thêm tình huống** (mất răng lâu năm, tiêu xương).

**② Làm lại LDP?**
Khi CTR ổn nhưng CVR / scroll / form thấp.
→ Sửa theo thứ tự: hero → phần gỡ 3 rào cản → micro-conversion (công cụ kiểm tra) → CTA → form.

**③ Đổi mẫu QC hoặc đổi loại LDP (A↔B)?**
Khi hook yếu, hoặc nỗi đau–khát khao không khớp khung.
→ Quay B2–B3 của engine, hoặc đổi loại landing.

---

## B9 · Quản trị creative

- **Winner → scale**: tăng ngân sách + nhân bản sang nhóm/cơ sở tương tự (Paris có 7 tỉnh thành → dư địa nhân bản local lớn).
- **Luôn giữ 1–2 challenger mới mỗi lô** — chống ad fatigue.
- **Lưu thư viện hook thắng theo dịch vụ** để tái sử dụng.

**Mẫu ghi thư viện hook:**
```
Dịch vụ:      Trồng răng Implant
Giai đoạn:    3 · Cân nhắc & nỗi sợ
Archetype:    4 · Phá vỡ hiểu lầm
Bằng chứng:   Đối tác Straumann
Hook:         "[nguyên văn hook thắng]"
Kết quả:      CTR __% (control __%) · CPL __ (control __) · booking rate __%
Điều kiện:    [thời gian chạy · ngân sách · nhóm từ khóa · cơ sở]
```

> Luôn ghi kèm **điều kiện** — một hook thắng ở Hà Nội với ngân sách nhỏ chưa chắc thắng ở TP.HCM khi scale.
