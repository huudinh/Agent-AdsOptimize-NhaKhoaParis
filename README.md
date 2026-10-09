# 🦷 ADS OPTIMIZE — Tối ưu quảng cáo hiệu suất (Nha khoa Paris)

> Version 2.3 · AI **sinh mẫu quảng cáo win · dựng landing page · chẩn đoán số liệu ADS + GA** cho **Hệ thống Nha khoa Tiêu chuẩn Pháp đầu tiên tại Việt Nam** — làm theo chỉ số, không làm theo cảm tính.

Theo công thức HCI **R·M·K·W·O**. Kiến trúc **BRAIN brand-neutral** ([`SYSTEM-PROMPT.md`](SYSTEM-PROMPT.md)) + **MODULE thương hiệu tách riêng** ([`knowledge/np-ho-so-thuong-hieu.md`](knowledge/np-ho-so-thuong-hieu.md)) → đổi brand chỉ cần thay module.

Agent anh em dùng chung bộ não: [`Agent-AdsOptimize-Kangnam`](../Agent-AdsOptimize-Kangnam/) (thẩm mỹ).

---

## Nguyên tắc tối thượng

> **Niềm tin xây bằng BẰNG CHỨNG, không bằng TÍNH TỪ.**

Khách nha khoa mua **chức năng + sự tự tin** — ăn nhai tốt lại, hết ê buốt, nụ cười đẹp. Nhưng chỉ xuống tiền khi gỡ được **3 rào cản: Sợ → Ngờ → Ngại**.

```
❌ "Nha khoa Paris — số 1 Việt Nam, niềng không bao giờ đau, đẹp tuyệt đối"
✅ "Giấy phép 2032/HNO-GPHĐ/CL1 · 100% bác sĩ tốt nghiệp ĐH Y có chứng chỉ hành nghề
   · đối tác Straumann và Invisalign Black Diamond · nhổ răng siêu âm Piezotome"
```

---

## Điểm khác biệt so với ngành thẩm mỹ: rào cản NGỜ nặng hơn hẳn

| Rào cản | Khách lo gì | Bằng chứng gỡ |
|---|---|---|
| **SỢ** | Đau/ê buốt · **mài mất răng thật** khi bọc sứ · niềng lâu–đau–xấu khi đeo | Piezotome · RECIPROC BLUE · Invisalign trong suốt |
| **NGỜ** ★ | **Trụ Implant / phôi sứ có chính hãng không?** · tay nghề · giá ẩn · biến chứng | **Straumann · Invisalign Black Diamond · Nacera · Ormco Diamond Star** · BS ĐH Y có chứng chỉ quốc tế |
| **NGẠI** | Điều trị dài · nhiều lần hẹn · chi phí lớn | Lộ trình rõ · **trả góp** · đặt lịch linh hoạt |

**Khách không tự kiểm tra được vật liệu trong miệng mình** — nên đối tác hãng chính hãng là bằng chứng mạnh nhất của Paris, và là thứ đối thủ khó sao chép.

> ⚠️ Vì vậy chữ **"chính hãng" là tuyên bố pháp lý**, chỉ được dùng cho 4 hãng trên. Dùng sai là **tự động 0 điểm** ở tiêu chí tuân thủ → loại thẳng mẫu.

---

## Bốn chế độ

| Mode | Làm gì | Input tối thiểu | Đầu ra |
|---|---|---|---|
| **1 · WIN-AD** | Từ từ khóa → mẫu QC Google RSA + Meta | từ khóa + dịch vụ | 15 headline + 4 description + 3–5 biến thể Meta + bảng chấm WIN + kế hoạch test |
| **2 · LDP-BUILD** | Từ từ khóa → landing loại A hoặc B | cụm từ khóa + dịch vụ | blueprint 13 section + copy, hoặc HTML single-file theo **khung trang chuẩn** + Design System v3.1 |
| **3 · LDP-ADVISOR** | Đọc ADS + GA → chẩn đoán | CTR·CPC·CPL·impression + scroll·form·booking | điểm nghẽn + 3 quyết định kèm ngưỡng và action |
| **4 · KEYWORD-ZONE** | Từ 1 ZONE dịch vụ → bộ từ khóa theo chân dung + hành trình | tên ZONE + ngân sách/tháng | chân dung KH · hành trình S1–S6 · chiến dịch kèm tỷ trọng ngân sách · 90–130 từ khóa · phủ định |

---

## Cổng WIN 2/3 — chạy trước mọi nội dung

| # | Tiêu chí | Đạt khi |
|---|---|---|
| ① | **Sát chuyển đổi** | Intent điều trị: giá · "ở đâu" · đặt lịch · **trả góp** |
| ② | **Cạnh tranh ít → bid thấp** | Ngách, dài, local, hoặc **theo tên hãng** |
| ③ | **Giá trị dịch vụ lớn** | **Implant · All-On 4/6 · Invisalign · răng sứ toàn hàm** |

**< 2/3 → KHÔNG làm nội dung.**

**Lưu ý riêng ngành nha khoa:** từ khóa đầu ngành ("trồng răng implant", "niềng răng") gần như **luôn trượt tiêu chí ②** — Elite Dental · Nha khoa Kim · I-Dent · Parkway · Lạc Việt Intech đều đấu giá. Phải thu hẹp bằng **tên hãng · "trả góp" · địa điểm · tình huống** ("mất răng lâu năm", "tiêu xương").

**Mỏ vàng bị bỏ quên:** từ khóa nỗi sợ — *"bọc sứ có hại răng thật không"*, *"implant có bị đào thải không"*. Cạnh tranh thấp, intent giai đoạn 3, và Paris có sẵn bằng chứng mạnh để trả lời.

---

## Phễu 6 giai đoạn

| Giai đoạn | Dấu hiệu từ khóa | Góc thông điệp | LDP |
|---|---|---|---|
| 1 **NHẬN BIẾT** | "là gì" · "răng xấu phải làm sao" | Giáo dục nhẹ, **chưa bán** | Không chạy LDP chốt |
| 2 **TÌM HIỂU** | "loại nào tốt" · "nha khoa nào uy tín" | So sánh + USP chuẩn Pháp / đối tác hãng | A hoặc B |
| 3 **CÂN NHẮC & NỖI SỢ** ★ | "có đau không" · "có hại không" · "trụ nào tốt" | **Gỡ nỗi sợ**: BS ĐH Y · hãng chính hãng · Piezotome · bảo hành | **Loại B (PAS)** |
| 4 **THỰC HIỆN** | "giá" · "ưu đãi" · **"trả góp"** · "đặt lịch" | Ưu đãi + trả góp + minh bạch chi phí | **Loại A** rút gọn |
| 5 **HẬU ĐIỀU TRỊ** | "chăm sóc sau" · "siết niềng đau" | Hướng dẫn + trấn an | Trang CRM |
| 6 **GẮN BÓ** | "khách cũ ưu đãi" · "nha khoa trẻ em" | Cross-sell + **gói gia đình** | **Loại A** |

**Giai đoạn 3 là điểm quyết định.** Giai đoạn 6 của nha khoa mạnh hơn thẩm mỹ — một khách hài lòng thường kéo theo cả gia đình.

---

## Hai cổng chặn không được bỏ qua

**① Cổng WIN 2/3** — từ khóa chưa đạt thì không sản xuất nội dung.
**② Chấm điểm WIN ≥ 10/12** — mẫu chưa đạt thì không xuất. **Tiêu chí tuân thủ bị 0 điểm → loại thẳng** bất kể tổng điểm; dùng sai chữ "chính hãng" là tự động 0 điểm.

---

## Quick start (4 bước)

1. Tạo 1 Project / GPT / Gem mới. Tên và mô tả ngắn: xem [`doc/01-cai-dat.md` §0](doc/01-cai-dat.md).
2. **Instructions:** dán khối ▼▲ trong [`SYSTEM-PROMPT.md`](SYSTEM-PROMPT.md) — riêng **ChatGPT** dùng [`SYSTEM-PROMPT-NGAN.md`](SYSTEM-PROMPT-NGAN.md).
3. **Knowledge:** upload 8 file `.md` trong [`knowledge/`](knowledge/).
4. Gọi mode: `MODE 1` · `MODE 2` · `MODE 3` · `MODE 4` — hoặc cứ nói bằng lời thường.

**Câu lệnh mẫu:**
```
MODE 1 — từ khóa "trồng răng implant trả góp hà nội". Chấm cổng WIN trước,
qua cổng thì sinh mẫu Google RSA + Meta.
```

**Chạy cả dây chuyền trong một lần?** Dán prompt trong
[`prompts/prompt-quy-trinh-tron-goi.md`](prompts/prompt-quy-trinh-tron-goi.md):

```
B1 bộ từ khóa → B2 ưu tiên → B3 insight → B4 mẫu QC → B5 layout → B6 HTML
   └── MODE 4 ────┘           └─── MODE 1 ───┘          └─── MODE 2 ───┘
             ▲CHỐT 1                      ▲CHỐT 2              ▲CHỐT 3
```

Agent dừng ở 3 chốt để bạn duyệt, không chạy một mạch tới cuối.

---

## 4 · Bộ từ khoá theo ZONE — sinh file Excel từ hành trình khách

> `MODE 4` trong bộ não (§12) lo phần nội dung; phần dưới đây là công cụ xuất file Excel cho cùng quy trình đó.

Phương pháp luận **lấy khách hàng làm trung tâm**: chọn **người** trước, chọn **từ khóa** sau.

```
ZONE → chân dung KH → hành trình S1–S6 → cụm truy vấn ưu tiên P1/P2/P3 → cụm nội dung → thực thi
```

1 ZONE = 1 file JSON trong [`zones/`](zones/) = 1 workbook 5 sheet trong `out/`.

```bash
pip install openpyxl
python tools/build_keyword_workbook.py zones/implant.json
```

**Cách nhanh nhất — để Agent tự xuất file:** upload `tools/build_keyword_workbook.py` + `zones/README.md` vào Knowledge, bật công cụ chạy code, rồi dán prompt §1 trong [`prompts/prompt-sinh-bo-tu-khoa-zone.md`](prompts/prompt-sinh-bo-tu-khoa-zone.md) — Agent sinh JSON, chạy generator và trả luôn file `.xlsx`. Cách chạy trên máy ở trên vẫn là cách duy nhất **tái lập được** bộ từ khoá và theo dõi thay đổi qua git.

Generator **chặn build** nếu: tổng tỷ trọng ngân sách ≠ 100% · từ khóa trỏ tới chiến dịch/landing/chân dung chưa khai báo · có Broad match · trùng từ khóa × kiểu khớp · thông điệp chứa **từ cấm quảng cáo y tế**.

> Sửa nội dung thì sửa JSON rồi build lại — **không sửa thẳng `.xlsx`**, lần build sau sẽ ghi đè.

**Từ workbook sang landing page:** bảng Landing ở sheet 4 ghi sẵn *Loại khung (A/B) · Chặng · Chân dung · Rào cản gỡ chính* cho từng LP — đủ đầu vào cho [`prompts/prompt-build-landing-page.md`](prompts/prompt-build-landing-page.md). LDP mặc định **mobile-first, single-file HTML**, tham chiếu trình bày từ `/trong-rang-implant-paris.html` nhưng **cấu trúc nội dung lấy từ hành trình KH**, không copy khung của trang đó.

---

## Tài liệu

| File | Nội dung | Trạng thái |
|---|---|---|
| [SYSTEM-PROMPT.md](SYSTEM-PROMPT.md) | Bộ não — 18 mục · **21.032 ký tự** | ✅ |
| [SYSTEM-PROMPT-NGAN.md](SYSTEM-PROMPT-NGAN.md) | Bản ngắn **7.959 ký tự** — chỉ cho **ChatGPT** · ⚠️ **chỉ dư 41 ký tự so với hạn mức 8.000, sửa phải đo lại** | ✅ |
| [knowledge/np-rao-phap-ly.md](knowledge/np-rao-phap-ly.md) | Từ cấm → từ đúng · **luật chữ "chính hãng"** · luật ảnh · HITL | ✅ |
| [knowledge/np-ho-so-thuong-hieu.md](knowledge/np-ho-so-thuong-hieu.md) | Định vị · **bộ nhận diện: màu + font** · Design System v3.1 · đối tác hãng · bác sĩ · taxonomy *(module swappable)* | ✅ |
| [knowledge/np-chan-dung-hanh-trinh.md](knowledge/np-chan-dung-hanh-trinh.md) | Insight · 3 rào cản đặc thù nha khoa · phễu 6 giai đoạn | ✅ |
| [knowledge/np-cong-win-tu-khoa.md](knowledge/np-cong-win-tu-khoa.md) | Cổng 2/3 · phiếu chấm · gom nhóm · lưu ý từ khóa ngành nha | ✅ |
| [knowledge/np-engine-win-ad.md](knowledge/np-engine-win-ad.md) | B1–B7 · 8 archetype hook · ma trận A/B · chấm điểm 12 · template QC | ✅ |
| [knowledge/np-khung-landing.md](knowledge/np-khung-landing.md) | Khung LDP A/B 13 section · **khung trang chuẩn** (header/footer/container) · **Design System v3.1** · micro-conversion | ✅ |
| [knowledge/np-chan-doan-chi-so.md](knowledge/np-chan-doan-chi-so.md) | WIN bằng số · bảng chẩn đoán · thư viện hook | ✅ |
| [knowledge/np-ppl-kh-trung-tam.md](knowledge/np-ppl-kh-trung-tam.md) | **PPL lấy KH làm trung tâm** · 4 ZONE · lớp chân dung KH · ánh xạ sang workbook | ✅ |
| [tools/build_keyword_workbook.py](tools/build_keyword_workbook.py) | Generator: 1 zone JSON → 1 file `.xlsx` 5 sheet, kèm cổng kiểm tra | ✅ |
| [zones/README.md](zones/README.md) | Schema 17 khối của zone config · trật tự điền bắt buộc | ✅ |
| [zones/implant.json](zones/implant.json) | ZONE Implant hoàn chỉnh: 6 chân dung · 11 chiến dịch · 123 từ khoá | ✅ |
| [prompts/prompt-sinh-bo-tu-khoa-zone.md](prompts/prompt-sinh-bo-tu-khoa-zone.md) | **Prompt chính: Agent tự xuất file `.xlsx` ngay trong phiên** · ngắn · mở rộng · rà soát · dự phòng ra bảng | ✅ |
| [prompts/prompt-build-landing-page.md](prompts/prompt-build-landing-page.md) | 5 prompt mẫu dựng LDP **mobile-first** từ sheet 4 Hành trình KH · checklist giao hàng | ✅ |
| [prompts/prompt-quy-trinh-tron-goi.md](prompts/prompt-quy-trinh-tron-goi.md) | **Dây chuyền 6 bước**: từ khóa → ưu tiên → insight → mẫu QC → layout → HTML · 3 chốt dừng | ✅ |
| [template/NKP _ Google Ads _ Bộ từ khoá Trồng răng Implant.xlsx](template/) | **File mẫu gốc** của workbook 5 sheet — generator dựng lại đúng file này | 📦 |
| [template/family-care.html](template/family-care.html) | **Trang production** đã lưu — nguồn của khung trang + Design System v3.1 | 📦 |
| [doc/01-cai-dat.md](doc/01-cai-dat.md) | Tên & mô tả · cài 3 nền tảng · smoke test · xử lý sự cố | ✅ |
| [doc/02-cau-lenh.md](doc/02-cau-lenh.md) | Câu lệnh 3 mode · prompt mẫu · điều Agent sẽ từ chối | ✅ |
| [doc/03-output-mau.md](doc/03-output-mau.md) | Output mẫu đủ 3 mode · dấu hiệu đúng/sai | ✅ |
| [doc/04-prompt-nguoi-moi.md](doc/04-prompt-nguoi-moi.md) | **21 prompt chia 7 nhóm — phủ hết việc Agent làm được**, cho người không chuyên ads | ✅ |
| [doc/CHANGELOG.md](doc/CHANGELOG.md) | Lịch sử · việc còn treo | ✅ |
| [doc/v1-ban-goc-1-file.md](doc/v1-ban-goc-1-file.md) | Bản gốc v1.3 một file — lưu để đối chiếu, **không dùng để cài** | 📦 |

---

## ⚠️ Giá, khuyến mãi & trả góp là dữ liệu động

Agent **bắt buộc** lấy giá tại `/hoan-my-bang-gia-dich-vu-nha-khoa.html` và ưu đãi tại trang ưu đãi hiện hành **ở thời điểm chạy**. Giá Implant/All-On và % ưu đãi **thay đổi theo đợt**. **Không bịa, không dùng số cũ đã nhớ.** Không truy cập được → `[CHỜ CẬP NHẬT]`.

Áp cho cả **điều kiện và lãi suất trả góp**.

---

## Ranh giới

Không cam kết kết quả ("đẹp tuyệt đối · khỏi 100% · **niềng không bao giờ đau** · không biến chứng · số 1 · tốt nhất · răng sứ dùng vĩnh viễn") · **không hứa thời gian điều trị cứng** · không chẩn đoán/kê đơn/báo giá ca cụ thể · không bịa giá · ưu đãi · số ca · % · chi nhánh · tên bác sĩ · review · **không gắn chữ "chính hãng" cho vật liệu ngoài 4 hãng đối tác** · không tạo ảnh kết quả giả · không dùng before–after chưa duyệt pháp lý · không nêu tên hạ thấp đối thủ · không nạp CCCD/hồ sơ bệnh án/ảnh khách lên công cụ công cộng.

Mọi mẫu QC / landing / tư vấn là **bản đề xuất**, phải qua người duyệt trước khi chạy.
"# Agent-AdsOptimize-NhaKhoaParis" 
