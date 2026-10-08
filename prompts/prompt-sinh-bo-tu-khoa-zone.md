# PROMPT MẪU — sinh bộ từ khoá Google Ads cho 1 ZONE

Agent trả về **file JSON** theo schema `zones/README.md`. Người dùng lưu vào `zones/<ma>.json` rồi chạy:

```bash
python tools/build_keyword_workbook.py zones/<ma>.json
```

---

## 1 · PROMPT ĐẦY ĐỦ — tạo ZONE mới từ đầu

> Dán nguyên khối dưới đây, chỉ thay 3 dòng trong ngoặc vuông.

```
Áp phương pháp luận MARKETING LẤY KHÁCH HÀNG LÀM TRUNG TÂM để sinh bộ từ khoá
Google Ads cho Nha khoa Paris.

ZONE:         [Niềng răng Invisalign]
MÃ ZONE:      [nieng-invisalign]
NGÂN SÁCH:    [150.000.000 VND/tháng]

Đọc trước, theo đúng thứ tự:
  knowledge/np-ho-so-thuong-hieu.md   - USP, đối tác hãng, bác sĩ, taxonomy dịch vụ
  knowledge/np-chan-dung-hanh-trinh.md - 3 rào cản SỢ/NGỜ/NGẠI, phễu 6 giai đoạn
  knowledge/np-cong-win-tu-khoa.md     - cổng WIN 2/3, cách gom nhóm
  knowledge/np-rao-phap-ly.md          - từ cấm, luật chữ "chính hãng"
  zones/README.md                      - schema JSON bắt buộc
  zones/implant.json                   - ví dụ đã hoàn chỉnh, dùng làm chuẩn độ chi tiết

LÀM THEO ĐÚNG TRẬT TỰ NÀY, không đảo:

1. CHÂN DUNG KH (4-7 nhóm). Với mỗi nhóm viết insight là NỖI ĐAU THẬT, không phải
   mô tả nhân khẩu học. Nếu người gõ Google khác người điều trị (con cái tìm cho
   bố mẹ, vợ tìm cho chồng) thì phải nói rõ — thông điệp viết cho NGƯỜI MUA HỘ.
   Gắn mỗi nhóm đúng 1 rào cản chốt chính: SỢ / NGỜ / NGẠI.

2. HÀNH TRÌNH S1-S6 cho zone này. Mỗi chặng ghi: chân dung chính, tâm lý, rào cản,
   bằng chứng BẮT BUỘC phải xuất hiện, landing, chuyển đổi đo lường, hành động sau
   lead trong Caresoft, KPI. S1 và S5 không chạy landing chốt.

3. CHIẾN DỊCH, đặt tên theo mẫu `NKP | <chặng> | <cụm truy vấn>`. Phân bổ ngân sách
   theo Ý ĐỊNH MUA × GIÁ TRỊ CA, tổng đúng 100%. S3 (Cân nhắc & nỗi sợ) phải được
   ít nhất 10% — đây là chặng quyết định của ngành nha và là ngách cạnh tranh thấp.

4. LANDING PAGE: 1 nhóm = 1 dịch vụ × 1 chặng × 1 intent = 1 trang. Mỗi trang có
   micro-conversion trước form.

5. TỪ KHOÁ, 90-130 dòng. Mỗi dòng gắn ĐỦ: chặng, mã chân dung, rào cản, mức cạnh
   tranh, điểm cổng WIN (x/3), landing, thông điệp + CTA.
   - Chỉ Exact và Phrase. KHÔNG Broad.
   - Để TRỐNG cột volume và cpc.
   - Từ khoá đầu ngành (cạnh tranh rất cao, intent loãng) chấm 1/3: vẫn giữ để hứng
     volume nhưng để P2/P3 và ghi rõ quy tắc cắt trong ghi_chu.
   - Ưu tiên 3 ngách Paris đang có lợi thế: từ khoá NỖI SỢ, từ khoá TÊN HÃNG đối tác,
     từ khoá TÌNH HUỐNG cụ thể.

6. TỪ KHOÁ PHỦ ĐỊNH: danh sách chung + phủ định chéo. Phủ định chéo là để ĐIỀU HƯỚNG
   truy vấn về đúng chiến dịch, không phải để loại khách.

7. NGƯỠNG, LỘ TRÌNH 3 PHA, QUY TẮC CẠNH TRANH, A/B TEST, RỦI RO.
   Ngân hàng Hook × Format cho FB/TikTok: cùng chân dung, cùng chặng với nhóm Search.

RÀNG BUỘC KHÔNG ĐƯỢC VI PHẠM:
  - Không dùng: tốt nhất, số 1, không đau 100%, cam kết thành công, khỏi 100%,
    đẹp tuyệt đối, vĩnh viễn, duy nhất. Không hứa thời gian điều trị cứng.
  - Chữ "chính hãng" CHỈ dùng cho Straumann (Implant), Invisalign, Nacera, Ormco.
  - Không bịa giá, ưu đãi, số ca, %, tên bác sĩ, tên cơ sở, review.
    Chưa chắc thì ghi [CHỜ CẬP NHẬT].
  - Không nêu tên đối thủ trong thông điệp quảng cáo.
  - Mọi lời hứa phải dẫn được 1 bằng chứng kiểm chứng được.

XUẤT RA: đúng 1 khối JSON hợp lệ theo schema zones/README.md, không kèm giải thích.
```

---

## 2 · PROMPT NGẮN — khi đã quen

```
Sinh zone JSON cho [tên zone], ngân sách [X]/tháng, theo schema zones/README.md.
Lấy zones/implant.json làm chuẩn độ chi tiết. Trật tự: chân dung KH → S1-S6 →
chiến dịch → landing → từ khoá (90-130 dòng, Exact/Phrase, để trống volume và cpc)
→ phủ định. S3 tối thiểu 10% ngân sách. Tuân thủ np-rao-phap-ly.md.
Chỉ xuất JSON.
```

---

## 3 · PROMPT BỔ SUNG — mở rộng zone đã có

```
Đọc zones/implant.json. Thêm [20] từ khoá cho chân dung [CD4 - mất răng lâu năm,
tiêu xương], tập trung chặng [S3].
Chỉ trả về các phần tử MỚI của mảng tu_khoa, giữ nguyên format các trường.
Không trùng cặp (từ khoá × kiểu khớp) đã có trong file.
```

---

## 4 · PROMPT RÀ SOÁT — trước khi giao team chạy ads

```
Đọc zones/<ma>.json và rà soát theo 6 câu hỏi, trả lời từng câu kèm dẫn chứng dòng:

1. Có từ khoá nào không gắn được chân dung KH nào không? Nếu có → nên bỏ hay nên
   bổ sung chân dung?
2. Chân dung nào đang không có từ khoá ở chặng S3? S3 là chặng rụng khách nhiều nhất.
3. Ngân sách có đang dồn vào chặng có ý định mua cao nhất không, hay đang dồn vào
   chặng có volume lớn nhất? (Volume lớn ≠ ra ca.)
4. Truy vấn nào có thể rơi vào 2 chiến dịch cùng lúc? Đã có phủ định chéo chưa?
5. Thông điệp nào đang hứa mà không dẫn được bằng chứng?
6. Có chỗ nào dùng chữ "chính hãng" ngoài Straumann / Invisalign / Nacera / Ormco không?
```

---

## 5 · PROMPT ĐỔI THƯƠNG HIỆU

Bộ não brand-neutral, module thương hiệu tách riêng — đổi brand chỉ cần thay 2 file knowledge.

```
Dựng lại zones/<ma>.json cho thương hiệu [tên brand] thay vì Nha khoa Paris.
Giữ nguyên cấu trúc, chân dung KH và hành trình S1-S6.
Thay: từ khoá brand, tên hãng đối tác, bằng chứng (giấy phép, bác sĩ, công nghệ),
mạng lưới cơ sở, danh sách đối thủ.
Đọc module thương hiệu mới trước khi làm. Chỗ nào chưa có dữ liệu → [CHỜ CẬP NHẬT].
```

---

## Sau khi có JSON

```bash
python tools/build_keyword_workbook.py zones/<ma>.json
```

Generator chặn build nếu: tổng tỷ trọng ≠ 100% · từ khoá trỏ tới chiến dịch/landing/chân dung
chưa khai báo · có Broad match · trùng từ khoá × kiểu khớp · thông điệp chứa từ cấm.
Sửa JSON rồi chạy lại — **không sửa thẳng file `.xlsx`**, lần build sau sẽ ghi đè.
