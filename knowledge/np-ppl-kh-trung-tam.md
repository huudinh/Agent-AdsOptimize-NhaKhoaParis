# PHƯƠNG PHÁP LUẬN — MARKETING LẤY KHÁCH HÀNG LÀM TRUNG TÂM
Version: 1.0 — áp dụng cho việc dựng bộ từ khoá Google Ads theo ZONE

> Nguồn: phương pháp luận MKT khách hàng trung tâm, chuyển từ ngành thẩm mỹ sang ngành nha khoa.
> Bộ não và 3 rào cản giữ nguyên; **lớp chân dung KH** là phần bổ sung so với `np-chan-dung-hanh-trinh.md`.

## Chuỗi quyết định

```
ZONE (lĩnh vực)
  └─ Đối tượng KH (nhóm chân dung)
       └─ Hành trình KH S1–S6 + insight từng chặng
            ├─ Kênh GOOGLE/WEBSITE → cụm truy vấn ưu tiên P1/P2/P3
            │     └─ cụm nội dung → thống nhất mục tiêu
            │          └─ thực thi: nội dung · tối ưu kỹ thuật SEO/GEO · báo cáo
            ├─ Kênh FB/TikTok → ngân hàng Hook × Format đúng chân dung
            │     └─ chọn hook ưu tiên · chọn format khả thi – hiệu quả
            └─ MKT automation (Caresoft / Zalo OA)
```

**Nguyên tắc gốc: chọn NGƯỜI trước, chọn TỪ KHOÁ sau.**
Gom từ khoá trước rồi gán người sau là cách làm cũ — nó tạo ra nhóm quảng cáo đúng ngữ pháp
nhưng sai tâm lý, và không giải thích được vì sao lead rẻ mà không ra ca.

## ZONE của Nha khoa Paris

| ZONE | Dịch vụ lõi | Giá trị ca | Rào cản nặng nhất |
|---|---|---|---|
| **Implant** | trồng răng Implant · All-On 4/6 · ghép xương · nâng xoang | Rất cao | NGỜ (trụ có đúng hãng không) |
| **Chỉnh nha** | Invisalign · mắc cài kim loại/sứ/pha lê/mặt trong | Rất cao | SỢ (lâu, đau, xấu khi đeo) |
| **Răng sứ** | bọc sứ thẩm mỹ · Veneer · răng sứ toàn hàm · cầu răng sứ | Cao | SỢ (mài mất răng thật) |
| **Tổng quát & Trẻ em** | nhổ răng Piezotome · tẩy trắng · điều trị tuỷ · cạo vôi · Teeth Spa | Thấp–Trung bình | NGẠI (ngại đi khám) |

Mỗi ZONE = **1 file cấu hình** trong `zones/` = **1 workbook** trong `out/`.
Không trộn hai ZONE vào một bộ từ khoá: rào cản khác nhau thì bằng chứng gỡ cũng khác nhau.

## Lớp chân dung KH — phần bổ sung quan trọng nhất

Phễu 6 giai đoạn trả lời *khách đang ở đâu*. Chân dung trả lời *khách là ai*.
Thiếu lớp này thì hai người rất khác nhau bị gộp chung một nhóm quảng cáo:

> "all on 4" và "trồng răng cho người già" cùng chặng S4, cùng dịch vụ toàn hàm.
> Nhưng người gõ câu thứ nhất là **bệnh nhân tự tìm hiểu**; người gõ câu thứ hai gần như luôn là
> **con cái tìm hộ bố mẹ**. Cùng một landing, cùng một mẫu quảng cáo → mất một nửa động cơ mua.

Mỗi chân dung phải trả lời được 5 câu:

1. **Ai** — tuổi, nghề, tình huống răng miệng.
2. **Nỗi đau thật** — không phải "muốn răng đẹp", mà "bỏ bữa vì nhai không nổi", "ngại nói trong cuộc họp".
3. **Rào cản chốt chính** — đúng 1 trong SỢ / NGỜ / NGẠI.
4. **Người gõ Google có phải người điều trị không** — nếu không, thông điệp viết cho người mua hộ.
5. **Giá trị ca** — quyết định được phép trả CPC bao nhiêu.

## Ánh xạ sang workbook

| Khối phương pháp luận | Nằm ở đâu trong file Excel |
|---|---|
| ZONE | Sheet 1, tiêu đề + mục tiêu |
| Đối tượng KH | Sheet 1 mục A · cột `Chân dung KH` ở sheet 2 · cột đầu sheet 4 |
| Hành trình S1–S6 + insight | Sheet 4 mục A |
| Cụm truy vấn ưu tiên P1/P2/P3 | Sheet 1 mục B (chiến dịch + cấp ưu tiên) · cột `Ưu tiên` sheet 2 |
| Cụm nội dung + thống nhất mục tiêu | Sheet 2 cột `Thông điệp / CTA` · Sheet 4 mục B (landing) |
| Hook × Format FB/TikTok | Sheet 4 mục C |
| Thực thi + báo cáo/đánh giá | Sheet 5: ngưỡng, lộ trình 3 pha, A/B test, rủi ro |

## Ba điều chỉnh khi chuyển từ thẩm mỹ sang nha khoa

**① Rào cản NGỜ nặng hơn hẳn.** Khách không tự kiểm tra được vật liệu trong miệng mình.
Đối tác hãng (Straumann · Invisalign · Nacera · Ormco) là bằng chứng mạnh nhất và khó sao chép nhất.
→ Chặng S3 phải được ngân sách thật, tối thiểu 10%, không phải phần thừa sau khi chia cho S4.

**② Hành trình dài hơn và có người mua hộ.** Ca toàn hàm thường do con cái quyết.
→ Trường `chan_dung` trong cấu hình phải ghi rõ ai là người gõ Google.

**③ Chặng S6 mạnh hơn.** Một khách nha khoa hài lòng thường kéo theo cả gia đình, và
tự nhiên chuyển sang ZONE khác (implant xong → bọc sứ răng kế cận → chỉnh nha cho con).
→ S6 là **cầu nối giữa các ZONE**, không phải đuôi phễu.

## Sai lầm hay gặp

| Sai | Đúng |
|---|---|
| Chia ngân sách theo volume tìm kiếm | Chia theo **ý định mua × giá trị ca** |
| Đánh giá chiến dịch bằng CPL | Đánh giá bằng **chi phí/ca chốt** và doanh thu |
| Phủ định để loại truy vấn lệch | Phủ định chéo để **điều hướng** về đúng chiến dịch; chỉ loại khi không chân dung nào khớp |
| Một landing cho mọi intent | 1 nhóm = 1 dịch vụ × 1 chặng × 1 intent = **1 trang** |
| Báo cáo theo chiến dịch | Báo cáo **theo chiến dịch VÀ theo chân dung KH** — cần trường chân dung trong Caresoft từ Pha 1 |
| Cắt S3 vì CPL cao | S3 là chặng rụng khách nhiều nhất; giữ tối thiểu 6 tuần trước khi phán xét |

## Công cụ

- Schema cấu hình: `zones/README.md`
- Generator: `tools/build_keyword_workbook.py`
- Prompt mẫu: `prompts/prompt-sinh-bo-tu-khoa-zone.md`
- Ví dụ hoàn chỉnh: `zones/implant.json`
