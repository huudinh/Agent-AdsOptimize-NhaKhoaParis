# PROMPT MẪU — bộ từ khoá Google Ads cho 1 ZONE

**Một prompt, một kết quả: file `.xlsx` 5 sheet tải về ngay trong chat.** Không cần cài Python trên máy, không cần ai chạy lệnh hộ.

---

## Cần chuẩn bị một lần

| | Việc |
|---|---|
| **1** | Bật công cụ chạy code: ChatGPT → **Code Interpreter** trong tab *Configure* · Claude và Gemini có sẵn |
| **2** | Upload thêm **2 file** vào Knowledge, cạnh 8 file `knowledge/`: `tools/build_keyword_workbook.py` và `zones/README.md` |
| **3** | Nên upload cả `zones/implant.json` — Agent lấy đó làm chuẩn độ chi tiết, chất lượng khác hẳn |

Thiếu bước 1 thì Agent không xuất được file — khi đó nó phải nói ngay và chuyển sang §5 (ra bảng).

---

## 1 · PROMPT CHÍNH — ra thẳng file Excel

> Sửa **3 dòng trong ngoặc vuông**, dán nguyên phần còn lại.

```
Tạo bộ từ khoá Google Ads cho Nha khoa Paris và XUẤT RA FILE EXCEL cho tôi tải về,
làm trọn trong phiên chat này. Đừng bắt tôi chạy script trên máy.

ZONE:      [Niềng răng Invisalign]
MÃ ZONE:   [nieng-invisalign]
NGÂN SÁCH: [150.000.000 VND/tháng]

Đọc trước, theo đúng thứ tự:
  knowledge/np-rao-phap-ly.md           - từ cấm, luật chữ "chính hãng"
  knowledge/np-ho-so-thuong-hieu.md     - USP, đối tác hãng, bác sĩ, taxonomy
  knowledge/np-chan-dung-hanh-trinh.md  - 3 rào cản SỢ/NGỜ/NGẠI, phễu 6 giai đoạn
  knowledge/np-cong-win-tu-khoa.md      - cổng WIN 2/3, cách gom nhóm
  knowledge/np-ppl-kh-trung-tam.md      - ZONE → chân dung → S1-S6 → cụm ưu tiên
  zones/README.md                       - schema JSON bắt buộc
  zones/implant.json                    - ví dụ hoàn chỉnh, chuẩn độ chi tiết

BƯỚC 1 — DỰNG NỘI DUNG, đúng trật tự này, không đảo:

  1. CHÂN DUNG KH (4-7 nhóm). Insight phải là NỖI ĐAU THẬT, không phải mô tả nhân
     khẩu học. Người gõ Google khác người điều trị (con tìm cho bố mẹ, vợ tìm cho
     chồng) thì ghi rõ — thông điệp viết cho NGƯỜI MUA HỘ. Mỗi nhóm gắn đúng 1 rào
     cản chốt: SỢ / NGỜ / NGẠI.

  2. HÀNH TRÌNH S1-S6. Mỗi chặng: chân dung chính, tâm lý, rào cản, bằng chứng BẮT
     BUỘC phải xuất hiện, landing, chuyển đổi đo lường, hành động sau lead, KPI.
     S1 và S5 không chạy landing chốt.

  3. CHIẾN DỊCH, tên theo mẫu `NKP | <chặng> | <cụm truy vấn>`. Chia ngân sách theo
     Ý ĐỊNH MUA × GIÁ TRỊ CA, KHÔNG chia theo lượng tìm kiếm. Tổng đúng 100%.
     S3 (Cân nhắc & nỗi sợ) tối thiểu 10% — chặng quyết định của ngành nha, cạnh
     tranh thấp.

  4. LANDING: 1 nhóm = 1 dịch vụ × 1 chặng × 1 intent = 1 trang, có micro-conversion
     trước form.

  5. TỪ KHOÁ, 90-130 dòng. Mỗi dòng gắn đủ: chặng, mã chân dung, rào cản, mức cạnh
     tranh, điểm cổng WIN (x/3), landing, thông điệp + CTA.
     - Chỉ Exact và Phrase. KHÔNG Broad.
     - Để TRỐNG volume và cpc — số đó lấy từ Keyword Planner.
     - Từ khoá đầu ngành chấm 1/3: vẫn giữ để hứng volume nhưng để P2/P3, ghi rõ
       quy tắc cắt trong ghi_chu.
     - Dồn vào 3 ngách Paris đang có lợi thế: từ khoá NỖI SỢ · TÊN HÃNG đối tác
       · TÌNH HUỐNG cụ thể.

  6. PHỦ ĐỊNH: danh sách chung + phủ định chéo. Phủ định chéo để ĐIỀU HƯỚNG truy vấn
     về đúng chiến dịch, không phải để loại khách.

  7. NGƯỠNG, LỘ TRÌNH 3 PHA, QUY TẮC CẠNH TRANH, A/B TEST, RỦI RO. Ngân hàng Hook ×
     Format cho FB/TikTok: cùng chân dung, cùng chặng với nhóm Search.

BƯỚC 2 — GHI FILE JSON đúng schema zones/README.md, lưu tên `<mã zone>.json` vào thư
mục làm việc của phiên (ChatGPT: /mnt/data).

BƯỚC 3 — CHẠY GENERATOR TÔI ĐÃ UPLOAD, đừng tự viết lại:
    pip install openpyxl -q
    python build_keyword_workbook.py <mã zone>.json -o .
  KHÔNG sửa script. KHÔNG tự chế cấu trúc file Excel — cấu trúc 5 sheet, công thức
  và định dạng là của file mẫu, không phải chỗ để sáng tạo.
  Script tự chặn 5 lỗi: tỷ trọng ≠ 100% · từ khoá trỏ tới chiến dịch/landing/chân
  dung chưa khai báo · có Broad · trùng từ khoá × kiểu khớp · thông điệp chứa từ cấm.
  Báo lỗi thì SỬA JSON rồi chạy lại, tối đa 3 lần. Vẫn lỗi thì dán nguyên thông báo
  lỗi cho tôi, đừng lách bằng cách bỏ bớt dữ liệu.

BƯỚC 4 — ĐƯA FILE .xlsx cho tôi tải về, kèm báo cáo ngắn:
  số chân dung · số chiến dịch · số từ khoá · bảng tỷ trọng ngân sách theo chặng
  · danh sách mọi chỗ [CHỜ CẬP NHẬT] tôi cần điền trước khi chạy ads.

RÀNG BUỘC KHÔNG ĐƯỢC VI PHẠM:
  - Không dùng: tốt nhất, số 1, duy nhất, không đau 100%, cam kết thành công,
    khỏi 100%, đẹp tuyệt đối, vĩnh viễn. Không hứa thời gian điều trị cứng.
  - Chữ "chính hãng" CHỈ dùng cho Straumann (Implant), Invisalign, Nacera, Ormco.
  - Không bịa giá, ưu đãi, số ca, %, tên bác sĩ, tên cơ sở, review.
    Chưa chắc thì ghi [CHỜ CẬP NHẬT].
  - Không nêu tên đối thủ trong thông điệp quảng cáo.
  - Mọi lời hứa phải dẫn được 1 bằng chứng kiểm chứng được.

Nếu phiên này không chạy được code: nói ngay ở câu đầu tiên, đừng làm xong rồi mới
báo. Khi đó xuất 5 bảng thay cho file.
```

---

## 2 · PROMPT NGẮN — khi đã quen

```
Dựng zone [tên zone], ngân sách [X]/tháng → xuất file .xlsx cho tôi tải về.
Sinh JSON theo zones/README.md, lấy zones/implant.json làm chuẩn độ chi tiết, rồi
chạy build_keyword_workbook.py tôi đã upload. Trật tự: chân dung KH → S1-S6 →
chiến dịch → landing → từ khoá (90-130 dòng, Exact/Phrase, để trống volume và cpc)
→ phủ định. S3 tối thiểu 10% ngân sách. Tuân thủ np-rao-phap-ly.md.
Script báo lỗi thì sửa JSON rồi chạy lại.
```

---

## 3 · PROMPT BỔ SUNG — mở rộng zone đã có

```
Đọc zones/implant.json. Thêm [20] từ khoá cho chân dung [CD4 - mất răng lâu năm,
tiêu xương], tập trung chặng [S3].
Không trùng cặp (từ khoá × kiểu khớp) đã có. Chèn vào mảng tu_khoa rồi chạy lại
build_keyword_workbook.py, đưa tôi file .xlsx mới.
```

---

## 4 · PROMPT RÀ SOÁT — trước khi giao team chạy ads

```
Đọc file zone vừa tạo và rà soát theo 6 câu hỏi, trả lời từng câu kèm dẫn chứng dòng:

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

## 5 · DỰ PHÒNG — phiên không chạy được code

Nền tảng không có công cụ chạy code thì không có file. Khi đó lấy bảng rồi dán sang Excel: cột của Bảng 4 đặt đúng thứ tự sheet `2. Bộ từ khoá` của file mẫu nên dán vào là khớp.

```
Dựng bộ từ khoá Google Ads cho [tên zone], ngân sách [X]/tháng, theo phương pháp
lấy khách hàng làm trung tâm. Xuất ra BẢNG, không xuất JSON.

Ra LẦN LƯỢT từng bảng, xong một bảng thì DỪNG và hỏi "tiếp bảng sau?". Đừng dồn cả
5 bảng vào một lượt — sẽ bị cắt giữa bảng và tôi phải làm lại từ đầu.

BẢNG 1 — CHÂN DUNG KH (4-7 nhóm)
  Mã | Tên nhóm | Ai gõ Google | Nỗi đau thật | Rào cản chốt | Bằng chứng gỡ
BẢNG 2 — HÀNH TRÌNH S1-S6
  Chặng | Chân dung chính | Tâm lý | Rào cản | Bằng chứng bắt buộc | Landing | Chuyển đổi | KPI
BẢNG 3 — CHIẾN DỊCH & NGÂN SÁCH
  Tên chiến dịch | Chặng | Cụm truy vấn | Tỷ trọng % | Số tiền/tháng | Lý do
  Chia theo ý định mua × giá trị ca, KHÔNG theo lượng tìm kiếm. Tổng 100%. S3 ≥ 10%.
BẢNG 4 — BỘ TỪ KHOÁ (60-120 dòng), đúng 16 cột theo thứ tự:
  STT | Chiến dịch | Nhóm quảng cáo | Từ khoá | Kiểu khớp | Ưu tiên | Chặng hành trình |
  Chân dung KH | Rào cản chốt | Cạnh tranh dự kiến | Cổng WIN (/3) | Landing page |
  Thông điệp / CTA chính | Lượng tìm kiếm/tháng | CPC đề xuất VND | Ghi chú vận hành
  Chỉ Exact và Phrase, KHÔNG Broad. Để TRỐNG hai cột lượng tìm kiếm và CPC.
  Ra 25-30 dòng mỗi lượt rồi dừng.
BẢNG 5 — TỪ KHOÁ PHỦ ĐỊNH
  Phủ định chung | Phủ định chéo (truy vấn → đẩy về chiến dịch nào)

Sau 5 bảng: ngưỡng cắt, lộ trình 3 pha, kế hoạch A/B, rủi ro.

Ràng buộc: không dùng "tốt nhất · số 1 · duy nhất · không đau 100% · cam kết thành
công · khỏi 100% · đẹp tuyệt đối · vĩnh viễn"; không hứa thời gian điều trị cứng;
chữ "chính hãng" chỉ cho Straumann / Invisalign / Nacera / Ormco; không bịa giá, ưu
đãi, số ca, %, tên bác sĩ, review → ghi [CHỜ CẬP NHẬT]; không nêu tên đối thủ.
```

Bảng dán tay **không có mô hình phễu tự tính** của sheet 1 — đó là phần chỉ file `.xlsx` mới có.

---

## Phụ lục — chạy trên máy, khi cần dựng lại nhiều lần

Giữ JSON trong `zones/` rồi build lại là cách duy nhất **tái lập được** bộ từ khoá và theo dõi thay đổi qua git:

```bash
pip install openpyxl
python tools/build_keyword_workbook.py zones/<ma>.json
```

Sửa nội dung thì sửa JSON rồi build lại — **không sửa thẳng `.xlsx`**, lần build sau sẽ ghi đè.

**Đổi thương hiệu** (bộ não brand-neutral, module thương hiệu tách riêng):

```
Dựng lại zone cho thương hiệu [tên brand] thay vì Nha khoa Paris. Giữ nguyên cấu
trúc, chân dung KH và hành trình S1-S6. Thay: từ khoá brand, tên hãng đối tác, bằng
chứng (giấy phép, bác sĩ, công nghệ), mạng lưới cơ sở, đối thủ. Đọc module thương
hiệu mới trước khi làm. Chỗ chưa có dữ liệu → [CHỜ CẬP NHẬT].
```
