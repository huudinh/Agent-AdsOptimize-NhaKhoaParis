# ZONE CONFIG — schema của file JSON sinh bộ từ khoá

Mỗi ZONE = **1 file JSON** trong thư mục này → **1 file `.xlsx` 5 sheet** trong `out/`.

```bash
python tools/build_keyword_workbook.py zones/implant.json
python tools/build_keyword_workbook.py "zones/*.json" -o out/
```

Yêu cầu: `pip install openpyxl`.

Generator **từ chối build** nếu cấu hình sai — xem mục [Cổng kiểm tra](#cổng-kiểm-tra) ở cuối.

---

## Trật tự bắt buộc khi điền — đây chính là phương pháp luận

Điền **đúng thứ tự này**. Đảo thứ tự là quay về cách làm cũ (gom từ khoá trước, gán người sau):

```
zone → chan_dung → hanh_trinh → chien_dich → landing → tu_khoa → phu_dinh → nguong/lo_trinh
 ①       ②            ③            ④           ⑤          ⑥          ⑦            ⑧
```

① ZONE là gì · ② **ai** mua · ③ họ đi qua **chặng nào** · ④ mỗi chặng cần **chiến dịch** gì ·
⑤ mỗi chiến dịch đổ về **trang** nào · ⑥ người đó **gõ gì** · ⑦ chặn và điều hướng truy vấn lệch · ⑧ ngưỡng vận hành.

---

## 17 khối bắt buộc

### ① `zone` — định danh

| Khoá | Kiểu | Ghi chú |
|---|---|---|
| `ten` | string | Tên hiển thị, vào tiêu đề sheet 1 |
| `ma` | string | slug, dùng đặt tên nội bộ |
| `nganh` | string | `Dental` |
| `ten_file` | string | Tên file xuất, **không kèm `.xlsx`** |
| `ds_phu_dinh_chung` | string | Tên danh sách phủ định cấp tài khoản, vd `NKP_Neg_Chung` |
| `ngan_sach_thang` | number | VND. Ô đầu vào (nền vàng) trên sheet 1 |
| `muc_tieu` | string | 1 câu, nêu rõ thứ tự ưu tiên chỉ số |

### ② `chan_dung[]` — chân dung KH

Khuyến nghị **4–7 chân dung**. Ít hơn 4 thường là chưa tách đủ; nhiều hơn 7 thì không đủ ngân sách phục vụ riêng.

| Khoá | Ghi chú |
|---|---|
| `ma` | `CD1`, `CD2`… — cột `chan_dung` của từ khoá tham chiếu mã này |
| `ten` | Ai, bao nhiêu tuổi, đang ở tình huống nào |
| `insight` | **Nỗi đau thật**, không phải mô tả nhân khẩu học. Nếu người gõ Google khác người điều trị (con cái mua hộ cho bố mẹ) thì **phải ghi rõ ở đây** |
| `rao_can` | `SỢ` / `NGỜ` / `NGẠI` + một câu giải thích |
| `chang_vao` | Chặng họ bước vào phễu, vd `S2-S3` |
| `chien_dich` | Các chiến dịch phục vụ chân dung này |
| `gia_tri_ca` | `Thấp` / `Trung bình` / `Cao` / `Rất cao` |

### ③ `hanh_trinh[]` — 6 chặng S1→S6

Đúng **6 phần tử**, theo thứ tự. Khoá: `chang`, `chan_dung`, `tam_ly`, `rao_can`, `chien_dich`,
`tu_khoa`, `thong_diep`, `bang_chung`, `lp`, `chuyen_doi`, `sau_lead`, `kpi`, `tiep_theo`.

| Chặng | Dấu hiệu trong từ khoá | Lưu ý |
|---|---|---|
| S1 NHẬN BIẾT | "là gì" · "phải làm sao" | Không chạy landing chốt |
| S2 TÌM HIỂU | "loại nào tốt" · "so sánh" | |
| **S3 CÂN NHẮC & NỖI SỢ** | "có đau không" · "có hại không" · "review" | **Chặng quyết định** — cạnh tranh thấp nhất, Paris có bằng chứng mạnh nhất |
| S4 THỰC HIỆN | "giá" · "ở đâu" · "trả góp" · "đặt lịch" | |
| S5 TRẢI NGHIỆM & HẬU PHẪU | "sau khi" · "kiêng gì" | Không chạy landing chốt |
| S6 GẮN BÓ & MỞ RỘNG | "khách cũ" · "cả gia đình" | Cross-sell sang ZONE khác |

### ④ `chien_dich[]` + ⑤ `cap_uu_tien[]`

`chien_dich[]`: `ten`, `uu_tien` (phải khớp một `cap` trong `cap_uu_tien`), `vai_tro`,
`ty_trong` (**tổng đúng 1.0**), `diem {y_dinh, gia_tri, kha_nang_chot}` (1–5), `bid`, `chi_tieu`.

> Quy ước đặt tên: `NKP | <chặng> | <cụm truy vấn>` — vd `NKP | S4 | Giá & Trả góp`.
> Tên này là **khoá nối** sang sheet 2 (`COUNTIF`) và sheet 5 (tham chiếu ô). Sửa tên ở một nơi phải sửa cả hai.

`cap_uu_tien[]`: `cap` (`P1`…`P4`), `quy_tac`.

### ⑥ `landing[]`

`ma_ten` dạng **`LPx: tên trang`** — generator cắt phần trước dấu `:` làm mã đối chiếu với cột `lp` của từ khoá.

| Khoá | Ghi chú |
|---|---|
| `loai` | Khung nội dung: `A - AIDA`, `B - PAS`, hoặc `Công cụ` / `Trang CRM` nếu không chạy landing chốt. Quy tắc chọn: xem `np-khung-landing.md` |
| `chang` | Chặng trang này phục vụ, vd `S3` |
| `chan_dung` | Mã `CDx`, có thể nhiều mã |
| `rao_can` | Rào cản **trang này phải gỡ** — section "Gỡ 3 rào cản" bám vào đây, không gỡ chung chung cả ba |
| `noi_dung` | Nội dung bắt buộc phải có trên trang |
| `cta` | CTA chính |
| `micro` | Micro-conversion đặt **trước** form booking |

> 4 trường `loai` / `chang` / `chan_dung` / `rao_can` là đầu vào trực tiếp của
> [`prompts/prompt-build-landing-page.md`](../prompts/prompt-build-landing-page.md). Thiếu thì Agent phải đoán khung A/B.

### ⑦ `tu_khoa[]` — 1 dòng = 1 từ khoá × 1 kiểu khớp

| Khoá | Ghi chú |
|---|---|
| `chien_dich` | Phải khớp **chính xác** một `chien_dich[].ten` |
| `nhom_qc` | Nhóm quảng cáo |
| `tu_khoa` | Viết thường, không dấu ngoặc |
| `khop` | `Exact` / `Phrase`. **`Broad` bị generator chặn** — chỉ mở ở Pha 3 |
| `uu_tien` | `P1`…`P4`, có thể khác cấp của chiến dịch |
| `chang` | `S1`…`S6` |
| `chan_dung` | Mã `CDx` |
| `rao_can` | `SỢ` / `NGỜ` / `NGẠI` |
| `canh_tranh` | `Thấp` / `Trung bình` / `Cao` / `Rất cao` |
| `win` | Điểm cổng WIN dạng `2/3`. Xem bảng dưới |
| `lp` | Mã `LPx` |
| `thong_diep` | Thông điệp + CTA. **Bị quét từ cấm** |
| `volume`, `cpc` | **Để trống** — điền sau từ Keyword Planner |
| `ghi_chu` | Điều kiện bật/tắt, cảnh báo pháp lý, quy tắc cắt |

**Cổng WIN** (`knowledge/np-cong-win-tu-khoa.md`) — ① sát chuyển đổi · ② cạnh tranh ít · ③ giá trị dịch vụ lớn:

- `3/3`, `2/3` → được sản xuất nội dung riêng.
- `1/3` → **vẫn có thể giữ từ khoá** để hứng volume, nhưng **không viết nội dung riêng**, phải để P3/P4 và ghi rõ quy tắc cắt trong `ghi_chu`.

### ⑧ `phu_dinh_chung[]` / `phu_dinh_cheo[]` / `quy_trinh_phu_dinh[]`

Khoá: `nhom`, `tu`, `khop`, `ap_dung`, `ly_do`.

> **Phủ định chéo không phải để loại khách — là để điều hướng.** Trước khi thêm một phủ định, hỏi:
> truy vấn này thuộc chân dung nào? Có chân dung phù hợp → đẩy sang đúng chiến dịch. Không có → mới loại.

### ⑨ Còn lại

`phieu` (6 giả định phễu + `ghi_chu`), `nguyen_tac[]`, `nguong[]` (`moc` = `cpl` hoặc `ca_chot`),
`lo_trinh[]` (3 pha), `quy_tac_canh_tranh[]`, `ab_test[]`, `rui_ro[]`, `hook_format[]` (tuỳ chọn — ngân hàng Hook × Format cho FB/TikTok).

---

## Cổng kiểm tra

Generator dừng và in lỗi nếu:

- thiếu bất kỳ khoá nào trong 17 khối bắt buộc;
- `sum(ty_trong) ≠ 1.0`;
- từ khoá trỏ tới `chien_dich` / `lp` / `chan_dung` chưa khai báo;
- chiến dịch dùng `uu_tien` chưa có trong `cap_uu_tien`;
- có `khop: "Broad"`;
- trùng cặp (từ khoá × kiểu khớp);
- `thong_diep` chứa từ cấm quảng cáo y tế: *tốt nhất · số 1 · không đau 100 · cam kết thành công · khỏi 100 · đẹp tuyệt đối · vĩnh viễn · duy nhất*.

Cổng này chặn lỗi cấu trúc, **không thay người duyệt**. Mọi mẫu quảng cáo và landing vẫn phải qua pháp chế.

---

## Sau khi build

1. Mở file trong `out/`, điền 2 cột Keyword Planner (`volume`, `cpc`).
2. Thay các ô **nền vàng chữ xanh** ở sheet 1 và sheet 5 bằng số thực của Paris (Caresoft).
3. Giá và ưu đãi là **dữ liệu động** — lấy tại `/hoan-my-bang-gia-dich-vu-nha-khoa.html` và trang ưu đãi hiện hành **ở thời điểm chạy**.
4. Sửa nội dung thì sửa **file JSON rồi build lại**, đừng sửa thẳng `.xlsx` — lần build sau sẽ ghi đè.
