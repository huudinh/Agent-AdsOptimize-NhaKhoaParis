# 04 · 21 PROMPT — PHỦ HẾT VIỆC AGENT LÀM ĐƯỢC

Dành cho bạn nếu **chưa quen thuật ngữ quảng cáo**. Không cần biết "phễu", "CVR", "archetype" là gì — cứ nói như đang nhắn tin.

**Agent sẽ:** mở đầu bằng một dòng *"Mình hiểu là…"* để bạn soát → làm việc → nói kết quả bằng chữ dễ hiểu.

Bảy nhóm dưới đây là **toàn bộ** việc Agent làm được. Muốn chỉ định rõ thì gõ `MODE 1`…`MODE 4` ở đầu câu, nhưng không bắt buộc.

---

# Mẫu điền chỗ trống

```
Mình muốn [QUẢNG CÁO / TRANG BÁN HÀNG / BỘ TỪ KHOÁ / XEM SỐ LIỆU] cho [DỊCH VỤ].
Khách đang [TÌM GÌ / LO GÌ].
[Số liệu nếu có]
```

---

# A · Lọc từ khoá

## 1 · Từ khoá này có đáng làm không
> Mình định chạy quảng cáo từ khóa **"trồng răng implant"**. Có đáng tiền không hay nên đổi? Giải thích giúp mình.

**Nhận được:** phiếu chấm 3 tiêu chí. Với từ khóa đầu ngành như thế này, gần như chắc chắn Agent sẽ bảo **quá đắt** và gợi ý cách thu hẹp.

**Vì sao đáng hỏi trước:** từ khóa trượt cổng lọc thì mọi thứ phía sau — mẫu quảng cáo, trang đích — đều lãng phí. Agent **không viết** nội dung cho từ khóa chưa qua cổng.

---

## 2 · Lọc cả danh sách
> Mình có một đống từ khóa chưa biết chọn cái nào. Lọc giúp mình cái nào nên chạy trước, cái nào bỏ. Chưa cần viết quảng cáo.
> *(dán danh sách)*

**Nhận được:** chia 3 nhóm — chạy ngay · thu hẹp rồi chạy · bỏ — kèm lý do từng dòng.

---

# B · Bộ từ khoá

## 3 · Bộ từ khoá ra file Excel
> Dựng bộ từ khoá cho **trồng răng Implant**, ngân sách **200 triệu một tháng**, rồi **xuất file Excel cho mình tải về**. Làm theo thứ tự: chân dung khách trước, rồi hành trình 6 chặng, rồi mới tới từ khoá.

**Nhận được:** file `.xlsx` 5 sheet có công thức sẵn — đổi ngân sách là bảng tự tính lại.

**Cần làm trước một lần:** upload `tools/build_keyword_workbook.py` và `zones/README.md` vào Knowledge; ChatGPT phải bật **Code Interpreter**. Thiếu phần này Agent chỉ trả được bảng trong chat. Bản prompt đầy đủ, có mọi ràng buộc, nằm ở [`prompts/prompt-sinh-bo-tu-khoa-zone.md`](../prompts/prompt-sinh-bo-tu-khoa-zone.md).

---

## 4 · Ngân sách có đang chia đúng chỗ không
> Xem giúp mình bộ từ khoá này: ngân sách đang dồn vào chặng khách **sắp mua**, hay dồn vào chặng có **nhiều lượt tìm kiếm nhất**? Chân dung khách nào đang chưa có từ khoá nào phục vụ?
> *(dán bộ từ khoá)*

**Nhận được:** 6 câu rà soát trước khi giao team chạy.

**Vì sao đáng hỏi:** chia ngân sách theo lượt tìm kiếm là **lỗi gốc hay gặp nhất**. Lượt tìm kiếm lớn không đồng nghĩa ra ca — chặng "đang cân nhắc và còn sợ" ít lượt hơn nhiều nhưng là chặng rụng khách nhiều nhất.

---

## 5 · Từ khoá phủ định
> Cho mình danh sách **từ khoá phủ định** cho chiến dịch **trồng răng Implant**. Tách rõ phần chặn hẳn và phần **điều hướng** truy vấn về đúng chiến dịch khác.

**Nhận được:** hai danh sách riêng, dán thẳng vào trình quản lý được.

**Vì sao phải tách:** phủ định chéo là để **đẩy truy vấn về đúng nhóm**, không phải để loại khách. Nhập chung hai loại là tự chặn khách thật.

---

## 6 · Thêm từ khoá cho một nhóm khách
> Thêm **20 từ khoá** cho nhóm khách **mất răng lâu năm, đã tiêu xương**, tập trung chặng **đang cân nhắc và còn sợ**. Không trùng những từ đã có.
> *(dán bộ từ khoá hiện tại)*

**Nhận được:** chỉ phần mới, giữ nguyên format để bạn chèn thẳng vào bộ cũ.

---

# C · Mẫu quảng cáo

## 7 · Quảng cáo Google
> Viết giúp mình quảng cáo Google cho **niềng răng trả góp ở Hà Nội**. Khách quan tâm chi phí và sợ tốn.

**Nhận được:** 15 tiêu đề + 4 mô tả đúng giới hạn ký tự, chia theo góc tiếp cận, kèm bảng chấm điểm và kế hoạch test.

---

## 8 · Quảng cáo Facebook hoặc TikTok
> Viết giúp mình quảng cáo Facebook cho **trồng răng Implant**. Khách lớn tuổi, hay sợ đau và sợ bị đào thải trụ.

**Nhận được:** 3–5 biến thể theo góc khác nhau để chạy thử song song, kèm gợi ý hình và câu mở đầu cho video ngắn.

---

## 9 · Câu mở đầu theo nỗi lo của khách
> Mình bí câu mở đầu. Cho mình **6 câu khác kiểu** cho **bọc răng sứ**, khách hay lo **mài sẽ hỏng răng thật**.

**Nhận được:** 6 kiểu mở đầu **khác nhau về cách tiếp cận** — không phải 6 cách viết lại một câu — ghi rõ câu nào đánh vào nỗi sợ nào.

---

## 10 · Chấm điểm mẫu đang chạy
> Chấm điểm giúp mình mẫu quảng cáo này rồi nói nên sửa gì trước. Sau đó lên **kế hoạch A/B**: đổi một thứ mỗi lần, đo bằng chỉ số nào.
> *(dán mẫu)*

**Nhận được:** thang 12 điểm; dưới 10 là Agent đề nghị sửa rồi chấm lại.

**Vì sao kế hoạch test quan trọng:** đổi nhiều thứ một lượt thì thắng cũng không biết nhờ cái gì. Agent chỉ đổi **một** biến mỗi lần.

---

# D · Landing page

## 11 · Trang cho khách đang chọn chỗ
> Làm giúp mình **trang bán hàng cho răng sứ thẩm mỹ**. Khách đã muốn làm, đang so sánh xem làm ở đâu.

**Nhận được:** bố cục từng phần + nội dung, theo khung **AIDA** — bán giấc mơ nụ cười. Agent nói rõ vì sao chọn khung đó, và hỏi bạn muốn bản chữ hay bản HTML chạy được.

---

## 12 · Trang cho khách đang sợ
> Khách của mình hay lo **bọc sứ sẽ hỏng răng thật**. Làm trang bán hàng cho nhóm này, phần gỡ nỗi lo và phần nói về hãng sứ viết kỹ giúp mình.

**Nhận được:** trang theo khung **PAS** — gọi tên nỗi đau trước, rồi mới nói giải pháp.

**Vì sao hay dùng hơn AIDA:** phần lớn khách nha khoa xuất phát từ **nỗi đau**, không phải từ khát khao. Nhóm từ khóa nỗi sợ cũng ít đối thủ đấu giá hơn.

---

## 13 · Xuất thẳng ra file HTML
> Làm trang bán hàng cho **trồng răng Implant** cho nhóm khách **sợ đau và sợ đào thải trụ**, rồi **xuất ra file HTML chạy được luôn**. Ưu tiên xem trên điện thoại, có nút đặt lịch dính dưới màn hình và phần hỏi đáp bác sĩ.

**Nhận được:** một file mở bằng trình duyệt là xem được — đúng màu, đúng font thương hiệu, đúng khung trang của trang mẫu.

---

## 14 · Sửa trang đang có
> Trang bán hàng hiện tại nhiều người vào nhưng **gần như không ai điền form**. Đề xuất sửa phần nào trước. Chưa cần viết lại cả trang.

**Nhận được:** danh sách **xếp theo thứ tự việc nào sửa trước cho đáng công**, không phải danh sách dài vô thứ tự. Thường Agent gợi ý chèn **công cụ kiểm tra online** làm bước trung gian trước ô điền số.

---

## 15 · Cần cấp những ảnh nào
> Trang vừa làm cần những ảnh gì? Liệt kê từng ô: nằm ở phần nào, tỉ lệ bao nhiêu, nội dung ảnh cần là gì, ai phải duyệt.

**Nhận được:** bảng kê ảnh cần cấp — dùng được như phiếu đặt hàng cho bên thiết kế.

**Vì sao có bảng này:** chỗ chưa có ảnh thật, Agent dựng **ô ảnh tạm** viền đứt ghi rõ cần ảnh gì. Nó **không bao giờ** chèn ảnh stock hay ảnh AI, vì ảnh kết quả điều trị giả là rủi ro pháp lý thật.

---

# E · Đọc số liệu

## 16 · Chạy rồi mà không ra khách
> Quảng cáo chạy 2 tuần, nhiều người bấm vào nhưng **gần như không ai để lại số**. Xem giúp hỏng ở đâu.
> *(dán số liệu nếu có)*

**Nhận được:** chỉ ra nghẽn ở từ khoá, ở trang, hay ở mẫu — rồi chọn **một** việc sửa trước.

---

## 17 · Có nên tăng tiền không
> Mẫu này đang tốt hơn mẫu cũ. **Tăng ngân sách được chưa**?
> *(dán số liệu)*

**Nhận được:** nếu dữ liệu còn ít, Agent sẽ bảo **chưa đủ để kết luận**. Đây là chỗ nhiều người đốt tiền oan nhất.

---

## 18 · Ngưỡng nào thì cắt, theo chỉ số nào
> Mình sắp bật chiến dịch mới. Đặt giúp mình **ngưỡng cắt** và **danh sách chỉ số cần theo** theo từng tuần, để biết lúc nào nên dừng chứ không đốt tiền tiếp.

**Nhận được:** ngưỡng cắt theo từng chặng + lộ trình 3 pha.

**Vì sao hỏi trước khi chạy:** ngưỡng đặt **trước** thì mới khách quan. Đặt sau khi đã thấy số thì rất khó cắt một chiến dịch mình đã bỏ tiền vào.

---

# F · Pháp lý & thương hiệu

## 19 · Câu này viết vậy có bị phạt không
> Mình định viết **"răng sứ chính hãng, dùng vĩnh viễn, niềng không đau"**. Có vấn đề gì không?

**Nhận được:** chỉ rõ từng chỗ sai và câu thay thế dẫn được bằng chứng thật. Riêng chữ **"chính hãng"** Agent sẽ hỏi bạn dùng sứ hãng nào — đây là tuyên bố pháp lý, dùng sai là rắc rối thật.

---

## 20 · Dùng bộ này cho thương hiệu khác
> Mình muốn dùng bộ này cho một thương hiệu nha khoa khác. Cần thay những gì, và chỗ nào bắt buộc phải có dữ liệu mới?

**Nhận được:** danh sách đúng những chỗ phải thay.

**Vì sao làm được:** bộ não không gắn cứng vào Paris — phần thương hiệu tách riêng thành file hồ sơ. Đổi brand chủ yếu là thay file đó, phần phương pháp giữ nguyên.

---

# G · Chạy cả dây chuyền

## 21 · Từ từ khoá tới file HTML trong một lần
> Chạy quy trình trọn gói cho **trồng răng Implant**, ngân sách **200 triệu một tháng**, đích cuối là **một trang bán hàng cho nhóm khách sợ đau và sợ đào thải trụ**. Làm tuần tự: bộ từ khoá, xếp ưu tiên, đào insight, mẫu quảng cáo Google, layout trang, rồi xuất file HTML. Dừng cho mình duyệt sau bước xếp ưu tiên, sau mẫu quảng cáo, và sau layout.

**Nhận được:** 6 bước nối liền, **3 lần dừng** để bạn duyệt.

**Vì sao có 3 chốt dừng:** sai ở bước đầu mà chạy hết dây chuyền thì phải làm lại cả 6 bước. Bản đầy đủ ở [`prompts/prompt-quy-trinh-tron-goi.md`](../prompts/prompt-quy-trinh-tron-goi.md).

---

# 3 điều bạn KHÔNG cần lo

| Bạn lo | Thực tế |
|---|---|
| "Không biết từ khóa thuộc giai đoạn nào" | Agent tự xếp và nói rõ vì sao. |
| "Không nhớ giới hạn ký tự của Google" | Agent tự đếm và viết đúng giới hạn. |
| "Không biết câu nào phạm luật quảng cáo y tế" | Agent tự tránh và tự thay. |

---

# 3 điều bạn PHẢI kiểm khi nhận bài

**① `[CHỜ CẬP NHẬT]` là chỗ thiếu số thật** — gần như luôn là **giá**, **ưu đãi** và **lãi suất trả góp**. Giá Implant và All-On đổi theo đợt; điền số cũ vào quảng cáo là chuyện lớn. Lấy số mới tại trang bảng giá rồi điền.

**② Chữ "chính hãng" chỉ được dùng cho 4 hãng đối tác** — Straumann · Invisalign · Nacera · Ormco. Thấy chữ này ở chỗ khác thì bỏ ngay, đây là tuyên bố pháp lý chứ không phải từ quảng cáo.

**③ Mọi mẫu phải qua pháp chế** — nội dung quảng cáo dịch vụ khám chữa bệnh cần **giấy xác nhận nội dung quảng cáo**. Ảnh trước–sau phải có giấy đồng ý của khách.

---

# Nếu kết quả chưa vừa ý

```
Nói đơn giản thôi, mình mới chạy ads.
```
```
Mấy câu này nghe như quảng cáo quá, viết giống lời khách nói hơn đi.
```
```
Bỏ hết chữ "chính hãng" đi, mình chưa chắc dùng hãng nào.
```
```
Bỏ hết giá đi, mình chưa lấy giá mới.
```
```
Cho mình thêm 3 câu mở đầu khác kiểu.
```
```
Không phải, mình muốn…
```
