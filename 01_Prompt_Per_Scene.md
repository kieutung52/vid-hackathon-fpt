Cách ổn định nhất là dùng Veo 3 tạo **hình ảnh + ambience (âm thanh môi trường) + SFX (hiệu ứng âm thanh)**, còn voice-over và nhạc nền được ghép thành track xuyên suốt trong hậu kỳ. Nếu yêu cầu Veo sinh giọng đọc riêng cho 12 clip, chất giọng và nhịp đọc có thể thay đổi giữa các cảnh.

Google khuyến nghị prompt video nên mô tả rõ máy quay, chủ thể, hành động, bối cảnh, phong cách và âm thanh; Veo 3.1 hỗ trợ clip 8 giây, 16:9, 1080p, âm thanh đồng bộ và cơ chế First/Last Frame để nối cảnh. [Google AI Veo guide](https://ai.google.dev/gemini-api/docs/video), [Google Cloud Veo 3.1 guide](https://cloud.google.com/blog/products/ai-machine-learning/ultimate-prompting-guide-for-veo-3-1).

# 1. Style Lock dùng chung

Dán nguyên khối này vào đầu cả 12 prompt:

```text
Tạo một video điện ảnh dài chính xác 8 giây, tỷ lệ 16:9, 24fps, chất lượng 1080p, một cú máy liên tục, không cắt cảnh bên trong clip.

Đây là một bộ phim công nghệ–pháp lý về hệ thống tuân thủ trong ngân hàng Việt Nam. Phong cách cinematic banking compliance techno-thriller, siêu chân thực, nghiêm túc, cao cấp, không mang phong cách khoa học viễn tưởng viển vông.

Bảng màu cố định:
- Midnight Navy #071426 cho không gian và nền.
- Legal Cyan #4CC9F0 cho dữ liệu hợp lệ và hệ thống đang hoạt động.
- Evidence Gold #D9B76E cho điều khoản được xác thực và bằng chứng nguồn.
- Alert Red #E23D3D chỉ dùng cho nội dung lỗi thời, bị ngưng hiệu lực hoặc chưa được duyệt.

Ngôn ngữ hình ảnh cố định:
- Tài liệu pháp lý là những tờ giấy trắng cao cấp, cạnh sắc, không có chữ đọc được.
- Điều khoản được thể hiện thành các module kính trong suốt có lõi ánh sáng.
- Nội dung còn hiệu lực phát sáng cyan–gold.
- Nội dung hết hoặc ngưng hiệu lực phát ánh đỏ.
- Cổng kiểm soát là một vòng titanium tối màu, có viền cyan mảnh.
- Ánh sáng thể tích, phản xạ kính tinh tế, sương điện ảnh rất nhẹ.
- Ống kính anamorphic 40mm, độ sâu trường ảnh nông vừa phải, chuyển động máy mượt và có trọng lượng.
- Film grain rất nhẹ, black level sâu, highlight không cháy sáng.
- Chuyển động vật lý chậm, chắc chắn, chính xác, mang cảm giác hệ thống ngân hàng đáng tin cậy.

Không tạo chữ có thể đọc được, không tạo phụ đề, không logo, không watermark, không ký hiệu thương hiệu, không giao diện có chữ ngẫu nhiên, không khuôn mặt nhìn thẳng camera, không bàn tay biến dạng, không phong cách hoạt hình.

Âm thanh trong clip chỉ gồm ambience và SFX được mô tả riêng. Không có lời thoại, không voice-over, không nhạc nền hoàn chỉnh. Giữ khoảng âm thanh sạch để ghép voice-over và soundtrack trong hậu kỳ.
```

# 2. Prompt chi tiết từng cảnh

## Cảnh 1 — Câu trả lời nghe đúng nhưng sai

```text
[Áp dụng toàn bộ STYLE LOCK]

Bối cảnh là trung tâm vận hành tuân thủ của một ngân hàng hiện đại vào ban đêm. Khung hình mở đầu bằng extreme close-up phản chiếu trong mắt kính của một chuyên viên tuân thủ người Việt trưởng thành, chỉ nhìn nghiêng và không thấy rõ khuôn mặt. Trong mắt kính là một màn hình chứa các dòng dữ liệu trắng trừu tượng, tuyệt đối không có chữ đọc được.

0–2 giây: camera đứng rất gần mắt kính, nhịp chuyển động gần như bất động, tạo cảm giác tập trung và tin tưởng.

2–5 giây: camera dolly lùi chậm qua vai nhân vật, hé lộ hàng nghìn tài liệu pháp lý mờ trong không gian phía sau. Màn hình trước mặt phát ánh cyan bình thường, giống như đang đưa ra một câu trả lời tự tin.

5–8 giây: một ánh đỏ rất nhỏ xuất hiện sâu bên trong dữ liệu, sau đó lan dần qua phản chiếu trên kính. Không có cảnh báo bằng chữ; chỉ dùng sự thay đổi màu để cho thấy câu trả lời có một lỗi nguy hiểm bị che giấu. Kết thúc bằng phản chiếu đỏ phủ lên một tờ văn bản pháp lý ở tiền cảnh để nối sang cảnh 2.

Âm thanh: tiếng điều hòa và máy chủ ngân hàng rất nhỏ; nhịp tim trầm 58 BPM; tiếng điện tử cyan ổn định trong 4 giây đầu; từ giây 5 xuất hiện một rung động sub-bass thấp và tiếng cảnh báo xa, rất kín đáo. Không có tiếng nói.
```

**Voice-over hậu kỳ:**

> “Nguy hiểm nhất không phải câu trả lời vô lý… mà là câu nghe đúng, nhưng dựa trên luật đã cũ.”

**Chữ hậu kỳ:**

> NGHE ĐÚNG. NHƯNG SAI.

---

## Cảnh 2 — TT39 ban hành Điều 8

```text
[Áp dụng toàn bộ STYLE LOCK]

Bắt đầu từ cận cảnh một tờ văn bản pháp lý đang phản chiếu ánh đỏ giống đúng frame cuối cảnh 1. Camera macro trượt ngang trên bề mặt giấy, sau đó ánh đỏ biến mất và được thay bằng ánh Evidence Gold trang trọng.

0–2 giây: những mép giấy, dấu pháp lý dập nổi không có chữ và kết cấu sợi giấy hiện rõ dưới ánh sáng điện ảnh.

2–5 giây: camera nâng lên chậm. Từ chính giữa tờ văn bản, một cấu trúc Điều luật bằng kính trong suốt được dựng lên. Cấu trúc có một module chính lớn và nhiều module khoản nhỏ được tổ chức rõ ràng, cân đối.

5–8 giây: module Điều luật khóa vào vị trí bằng một chuyển động cơ khí chính xác. Lõi gold chuyển sang cyan–gold, biểu thị đây là phiên bản có hiệu lực. Camera tiến gần vào lõi module chính. Kết thúc bằng module Điều luật chiếm gần toàn bộ khung hình để nối sang cảnh 3.

Âm thanh: tiếng giấy lật rất sạch, tiếng bút máy lướt một nhịp ngắn, sau đó là tiếng khóa kim loại trầm khi cấu trúc Điều luật hoàn thành; cuối cảnh có một tiếng confirmation chime gold mềm và chắc chắn.
```

**Voice-over:**

> “Thông tư 39 ban hành Điều 8: những nhu cầu vốn không được cho vay.”

**Chữ hậu kỳ:**

> TT 39/2016  
> BAN HÀNH ĐIỀU 8

---

## Cảnh 3 — TT06 sửa đổi toàn bộ

```text
[Áp dụng toàn bộ STYLE LOCK]

Bắt đầu bằng module Điều luật cyan–gold từ frame cuối cảnh 2. Một tờ văn bản pháp lý thứ hai đi vào từ phía trên như một lớp dữ liệu mới, không va chạm bạo lực, mà phủ lên cấu trúc cũ bằng một làn sóng cyan có kiểm soát.

0–2 giây: camera thực hiện arc shot nhẹ quanh module Điều luật, cho thấy phiên bản cũ vẫn còn nguyên cấu trúc.

2–5 giây: làn sóng cyan đi từ trái sang phải và tái cấu trúc toàn bộ module. Các đường liên kết cũ tháo ra rồi gắn lại theo cấu trúc mới. Không làm module vỡ; đây là sửa đổi pháp lý có kiểm soát.

5–7 giây: đúng ba module khoản mới màu Evidence Gold mọc lên ở phía cuối cấu trúc, tách biệt rõ với nhóm module đã có. Ba module mới phải đồng đều, không tạo thêm module thứ tư.

7–8 giây: toàn bộ cấu trúc khóa lại. Camera dừng ở bố cục cho thấy nhóm cũ cyan–gold và nhóm ba module mới gold. Kết thúc bằng ánh sáng gold từ ba module mới phủ khung hình.

Âm thanh: tiếng tháo lắp cơ khí chính xác, các nhịp dữ liệu điện tử đi từ trái sang phải, ba tiếng activation chime liên tiếp tương ứng với ba module mới, sau đó là tiếng khóa hệ thống trầm.
```

**Voice-over:**

> “Thông tư 06 sửa đổi toàn bộ Điều 8, đồng thời bổ sung thêm khoản 8, 9 và 10.”

**Chữ hậu kỳ:**

> TT 06/2023  
> SỬA ĐỔI TOÀN BỘ ĐIỀU 8

---

## Cảnh 4 — TT10 ngưng đúng ba khoản

```text
[Áp dụng toàn bộ STYLE LOCK]

Mở đầu bằng cấu trúc Điều luật hoàn chỉnh từ cảnh 3. Bố cục chia thành hai nhóm rõ ràng: một nhóm lớn gồm các module cyan–gold đang hoạt động và một nhóm riêng đúng ba module gold mới ở phía cuối.

0–2 giây: một văn bản pháp lý thứ ba đi vào khung hình từ phía sau, được chiếu sáng bằng một đường viền Alert Red rất mảnh.

2–5 giây: một dải năng lượng đỏ chính xác quét đến đúng nhóm ba module gold. Chỉ ba module này chuyển sang đỏ, ánh sáng bên trong giảm xuống và bị bao phủ bởi lớp kính băng trong suốt.

5–7 giây: nhóm module cyan–gold còn lại tiếp tục hoạt động bình thường. Các dòng dữ liệu hợp lệ vẫn đi qua chúng, nhấn mạnh rằng chỉ một phần bị ngưng hiệu lực.

7–8 giây: camera push-in vào ranh giới giữa nhóm còn hiệu lực và nhóm ba module bị đóng băng. Kết thúc bằng cận cảnh ba module đỏ để nối sang cảnh 5.

Âm thanh: tiếng văn bản đi vào như một luồng gió nặng; một tiếng đóng dấu pháp lý cực trầm tại giây 3; ba tiếng crystal freeze ngắn; phía nhóm còn hiệu lực vẫn có tiếng hệ thống chạy đều. Không dùng còi báo động lớn.
```

**Voice-over:**

> “Rồi Thông tư 10 ngưng đúng ba khoản ấy. Khoản 1 đến 7 vẫn tiếp tục hiệu lực.”

**Chữ hậu kỳ:**

> NGƯNG KHOẢN 8–10  
> KHOẢN 1–7 VẪN HIỆU LỰC

---

## Cảnh 5 — RAG phẳng để luật cũ lọt vào Top-K

```text
[Áp dụng toàn bộ STYLE LOCK]

Bắt đầu bằng cận cảnh ba module đỏ bị đóng băng từ cảnh 4. Camera đột ngột xuyên vào bề mặt kính đỏ và đi vào một không gian xử lý dữ liệu khổng lồ.

0–2 giây: hàng nghìn văn bản pháp lý bị một hệ thống cũ cắt thành các mảnh chữ nhật phẳng, mất cấu trúc và mất đường liên kết. Tất cả các mảnh trông gần giống nhau, không còn phân biệt Điều, Khoản hay phiên bản.

2–5 giây: các mảnh dữ liệu trôi hỗn loạn về phía một cổng xếp hạng đơn giản. Phần lớn mảnh có ánh trắng hoặc cyan nhạt, nhưng có một mảnh Alert Red ẩn giữa chúng.

5–7 giây: mảnh đỏ vượt qua cổng cùng các mảnh hợp lệ. Camera tracking theo đúng mảnh đỏ khi nó đi nhanh về phía một lõi AI sáng trắng.

7–8 giây: ngay trước khi mảnh đỏ chạm lõi AI, khung hình xuất hiện glitch mạnh rồi đóng băng trong một phần giây. Kết thúc bằng mảnh đỏ nằm giữa khung hình.

Âm thanh: tiếng giấy bị cắt thành mẩu, âm thanh dữ liệu dồn dập, glitch stereo tăng dần; giây 6 có tiếng whoosh mạnh khi mảnh đỏ vượt cổng; cuối cảnh là một cú bass stop đột ngột.
```

**Voice-over:**

> “RAG thông thường cắt tất cả thành mẩu phẳng. Một quy định cũ vẫn có thể lọt vào Top-K.”

**Chữ hậu kỳ:**

> FLAT CHUNKS  
> OUTDATED RULE ENTERS TOP-K

---

## Cảnh 6 — Lọc hiệu lực trước Top-K

```text
[Áp dụng toàn bộ STYLE LOCK]

Mở đầu bằng mảnh dữ liệu đỏ đang đóng băng giữa khung hình từ cảnh 5. Một xung ánh sáng cyan chạy xuyên qua không gian và tái tổ chức toàn bộ các mảnh hỗn loạn thành một kiến trúc pháp lý có trật tự.

0–2 giây: các mảnh dữ liệu tự ghép lại thành các tầng lồng nhau: tài liệu ở ngoài, Điều ở giữa, Khoản ở trong, phiên bản và thời gian ở lõi. Không dùng chữ; phân biệt bằng hình học và màu sắc.

2–5 giây: phía trước kiến trúc xuất hiện cổng kiểm soát titanium có viền cyan. Các module hợp lệ cyan–gold được phép đi qua. Mảnh đỏ tiến đến nhưng bị một mặt phẳng thời gian trong suốt chặn lại trước cổng xếp hạng.

5–7 giây: mảnh đỏ phân rã thành bụi sáng và biến mất hoàn toàn. Các module hợp lệ tiếp tục đi qua cổng theo hàng rất chính xác.

7–8 giây: camera lao theo một module gold xuyên qua cổng. Ánh sáng cyan–white lấp đầy toàn bộ frame, tạo điểm cắt hoàn hảo sang màn hình demo.

Âm thanh: tiếng cấu trúc lắp ráp theo từng lớp, tiếng vòng titanium mở khóa, tiếng mảnh đỏ bị triệt tiêu như thủy tinh tan thành bụi, sau đó là một tiếng confirmation chime rõ và một rising whoosh dẫn vào demo.
```

**Voice-over:**

> “Chúng tôi quản lý từng Điều, từng Khoản, từng phiên bản—và lọc hiệu lực trước khi tìm kiếm.”

**Chữ hậu kỳ:**

> EFFECTIVE FILTER  
> BEFORE TOP-K

# 3. Demo màn hình 84 giây

Phần này quay màn hình thật, không dùng Veo. Giữ nhạc nền nhỏ hơn voice-over khoảng 18–22 dB.

Ở cuối demo, dừng tại màn hình câu trả lời hoặc Knowledge Graph. Dùng chính screenshot cuối đó làm **first frame** cho cảnh 7 để chuyển tiếp mượt.

# 4. Prompt outro

## Cảnh 7 — Ba chân truy hồi hội tụ

```text
[Áp dụng toàn bộ STYLE LOCK]

Nếu dùng image-to-video, sử dụng screenshot cuối phần demo làm first frame. Màn hình demo phải dần tan thành ba luồng dữ liệu điện ảnh, không biến mất đột ngột.

0–2 giây: camera tiến vào một kết quả tìm kiếm trên màn hình. Các pixel của giao diện tách ra thành ba luồng ánh sáng.

2–5 giây: luồng thứ nhất gồm các khối ý nghĩa trừu tượng màu cyan; luồng thứ hai gồm các ký hiệu hình học giống token nhưng không có chữ đọc được, màu Evidence Gold; luồng thứ ba là mạng lưới node–edge màu trắng lạnh.

5–7 giây: cả ba luồng xoắn quanh nhau theo chuyển động có kiểm soát và hội tụ vào một module điều khoản duy nhất.

7–8 giây: module điều khoản sáng cyan–gold, bay về phía camera. Kết thúc bằng module này chiếm phần trung tâm khung hình để nối cảnh 8.

Âm thanh: ba luồng có ba cao độ khác nhau; cyan là âm tổng hợp mềm, gold là tiếng click kim loại, graph là các pulse ngắn; khi hội tụ tạo thành một hợp âm xác nhận trầm và sạch.
```

**Voice-over:**

> “Ba chân truy hồi phối hợp: ngữ nghĩa, mặt chữ và quan hệ. Chỉ chân cần thiết mới được kích hoạt.”

**Chữ hậu kỳ:**

> MEANING + TEXT + RELATION

---

## Cảnh 8 — Truy ngược về nguồn

```text
[Áp dụng toàn bộ STYLE LOCK]

Mở đầu với module điều khoản cyan–gold từ cảnh 7 đang lơ lửng ở trung tâm. Camera orbit chậm quanh module trong một không gian lưu trữ pháp lý cao cấp.

0–2 giây: từ module xuất hiện một sợi Evidence Gold rất mảnh, chạy ngược về phía sau.

2–5 giây: sợi gold chia thành ba điểm neo liên tiếp: một hồ sơ văn bản, một trang giấy cụ thể và một vùng trích dẫn được viền sáng trên trang. Không có chữ đọc được, nhưng cấu trúc truy xuất phải rõ ràng.

5–7 giây: camera tracking dọc theo sợi ánh sáng, từ câu trả lời quay ngược về trang nguồn. Vùng trích dẫn trên trang phát sáng gold, trong khi phần còn lại của tài liệu giữ màu trắng lạnh.

7–8 giây: một dấu xác nhận hình học không có chữ khóa vào vùng trích dẫn. Kết thúc bằng đường viền gold chạy khỏi khung hình về phía cảnh 9.

Âm thanh: các tiếng data pulse chạy ngược theo đường ánh sáng, tiếng lật đúng một trang giấy, ba confirmation click nhỏ tương ứng văn bản–trang–trích dẫn, cuối cùng là một tiếng khóa bằng chứng chắc chắn.
```

**Voice-over:**

> “Mỗi kết quả truy ngược đến đúng văn bản, đúng trang, đúng bằng chứng. Không có nguồn, hệ thống không trả lời.”

**Chữ hậu kỳ:**

> SOURCE-CITED  
> PAGE-LEVEL TRACEABILITY

---

## Cảnh 9 — Chặn nội dung chưa duyệt và prompt injection

```text
[Áp dụng toàn bộ STYLE LOCK]

Đường viền gold từ cảnh 8 đi vào một lõi AI được bảo vệ bởi một lá chắn kính trong suốt hình vòng cung. Lõi AI không có hình người hoặc khuôn mặt, chỉ là một cấu trúc dữ liệu trắng–cyan.

0–2 giây: các module hợp lệ cyan–gold đi qua một khe kiểm duyệt và vào trong lá chắn.

2–5 giây: từ vùng tối xuất hiện hai loại mối đe dọa: một tài liệu phát đỏ biểu thị chưa được duyệt và những mảnh dữ liệu đen–đỏ có hình dạng sắc nhọn biểu thị prompt injection. Không sử dụng chữ hoặc mã lệnh có thể đọc được.

5–7 giây: cả hai va vào lá chắn và bị chặn hoàn toàn. Tài liệu chưa duyệt dừng nguyên vẹn bên ngoài; các mảnh tiêm lệnh vỡ thành hạt đỏ rồi tắt.

7–8 giây: lá chắn phát một pulse cyan ổn định và lõi AI bên trong tiếp tục hoạt động bình thường. Kết thúc bằng pulse cyan lan toàn màn hình.

Âm thanh: tiếng lá chắn hum trầm, hai tiếng va chạm kính dày, âm thanh mối đe dọa bị triệt tiêu, sau đó là một tiếng hệ thống hoạt động trở lại rất sạch. Không có âm thanh báo động hỗn loạn.
```

**Voice-over:**

> “Nội dung chưa duyệt bị chặn mặc định. Tài liệu là dữ liệu—không bao giờ được phép ra lệnh cho AI.”

**Chữ hậu kỳ:**

> REVIEWED ONLY  
> FAIL-CLOSED

---

## Cảnh 10 — Đo lường và SourceSpan

```text
[Áp dụng toàn bộ STYLE LOCK]

Pulse cyan từ cảnh 9 mở ra một đại sảnh kiểm định dữ liệu rộng, tối và trang nghiêm. Hàng trăm module điều khoản được sắp xếp thành một lưới ba chiều có trật tự.

0–2 giây: camera crane shot đi từ thấp lên cao, cho thấy quy mô của hệ thống kiểm định.

2–5 giây: từ mỗi module xuất hiện một sợi Evidence Gold nối đến đúng vị trí trên các trang tài liệu nguồn ở phía đối diện. Tất cả đường nối phải thẳng, rõ ràng và không giao nhau hỗn loạn.

5–7 giây: một làn sóng kiểm tra cyan chạy qua toàn bộ lưới. Mỗi đường nối sau khi được kiểm tra chuyển từ trắng sang gold, biểu thị round-trip chính xác.

7–8 giây: camera dừng ở góc rộng đối xứng, toàn bộ đại sảnh chuyển trạng thái xác nhận. Chừa vùng tối sạch ở bên phải để chèn số liệu hậu kỳ.

Âm thanh: hàng trăm tiếng click rất nhỏ nhưng đồng bộ, tiếng scan điện tử chạy từ trái sang phải, cuối cùng là một hợp âm confirmation sâu, rộng, không quá phô trương.
```

**Voice-over:**

> “Mọi thay đổi đều phải qua benchmark và kiểm tra SourceSpan. Không có chuyện chỉnh tham số bằng cảm giác.”

**Chữ hậu kỳ:**

> 70 EVIDENCE CASES  
> 205 SOURCE SPANS  
> 0 MISMATCH

---

## Cảnh 11 — Pilot 30 ngày

```text
[Áp dụng toàn bộ STYLE LOCK]

Chuyển từ đại sảnh dữ liệu sang trung tâm tuân thủ ngân hàng vào buổi sáng. Không gian hiện đại, sạch, thực tế, có nhiều chuyên viên trưởng thành làm việc nhưng không thấy rõ khuôn mặt và không nhìn vào camera.

0–2 giây: một chuyên viên nhận yêu cầu tra cứu và đặt nó vào hệ thống dưới dạng một module cyan.

2–5 giây: module đi qua một chuỗi mốc thời gian hình học được bố trí như lịch vận hành. Mỗi mốc lần lượt phát sáng gold, biểu thị các ngày của pilot và quá trình đo lường liên tục.

5–7 giây: kết quả có bằng chứng quay trở lại bàn làm việc gần như tức thời. Chuyên viên chuyển từ trạng thái căng thẳng sang tập trung và chủ động, thể hiện qua tư thế chứ không qua cận mặt.

7–8 giây: camera dolly lùi, hé lộ toàn trung tâm vận hành hoạt động trơn tru. Chừa vùng trống phía trên để chèn thông tin pilot.

Âm thanh: ambience văn phòng cao cấp, tiếng bàn phím rất nhỏ, tiếng đồng hồ nhịp đều, các confirmation click tăng dần theo timeline, cuối cảnh có một rising tone tích cực nhưng vẫn trang nghiêm.
```

**Voice-over:**

> “Pilot 30 ngày bắt đầu từ quy định cho vay: đo đúng phiên bản, đúng trích dẫn và thời gian tra cứu.”

**Chữ hậu kỳ:**

> 30-DAY PILOT  
> LENDING REGULATIONS

---

## Cảnh 12 — Kết thúc hoành tráng

```text
[Áp dụng toàn bộ STYLE LOCK]

Toàn cảnh thành phố tài chính hiện đại lúc bình minh, nhìn từ góc cao. Một tòa nhà ngân hàng lớn nhưng không có logo đứng ở trung tâm. Phía trước tòa nhà là cổng kiểm soát titanium quen thuộc từ các cảnh trước.

0–2 giây: camera crane bắt đầu thấp phía sau cổng, nhìn thấy các module pháp lý cyan–gold đang đi vào ngân hàng.

2–5 giây: từ phía ngoài xuất hiện các mảnh pháp lý Alert Red đại diện cho quy định lỗi thời. Chúng lao đến nhưng bị cổng chặn lại và tan thành bụi đỏ bên ngoài. Không có vụ nổ hoặc phá hủy.

5–7 giây: camera nâng cao qua cổng, để lộ toàn cảnh thành phố và ánh mặt trời đầu ngày. Các đường dữ liệu gold kết nối ngân hàng với hệ thống pháp lý như một mạng lưới đáng tin cậy.

7–8 giây: camera dừng ở hero shot đối xứng. Phần giữa và phía trên khung hình phải sạch, ít chi tiết, đủ không gian để đặt logo và tagline. Ánh sáng gold–cyan hội tụ nhẹ tại trung tâm rồi giữ ổn định ở frame cuối.

Âm thanh: tiếng gió thành phố buổi sớm, cổng titanium khóa bằng một tiếng trầm chắc chắn, các mảnh đỏ tan bằng âm thanh mềm, sau đó là một cinematic impact sâu kết hợp một tiếng chime gold kéo dài đến frame cuối.
```

**Voice-over:**

> “Đây là lớp an toàn cho quyết định ngân hàng: đúng điều khoản, đúng phiên bản, đúng thời điểm.”

**Chữ kết thúc:**

> ĐÚNG ĐIỀU KHOẢN  
> ĐÚNG PHIÊN BẢN  
> ĐÚNG THỜI ĐIỂM

# 5. Track nhạc nền xuyên suốt

Không nên sinh nhạc riêng trong từng clip. Dùng một track duy nhất:

- **Tempo:** 68–72 BPM.
- **Tông:** D minor.
- **0:00–0:32:** heartbeat, sub-bass, cello thấp, pulse điện tử tối.
- **0:32–0:48:** tăng nhịp, glitch nhẹ, dừng nhạc 0,3 giây trước khi vào demo.
- **0:48–2:12:** nhạc tối giản, chỉ giữ pulse và pad thấp để không lấn voice-over.
- **2:12–2:44:** thêm string ostinato và percussion điện ảnh.
- **2:44–2:52:** nhạc nâng dần, cảm giác tiến tới triển khai thật.
- **2:52–3:00:** brass trầm, cinematic impact và hợp âm kết thúc lớn.

## Quy trình giữ tính nhất quán

1. Sinh trước ba ảnh tham chiếu: module điều khoản, cổng titanium và phòng vận hành.
2. Dùng cùng các ảnh đó làm Ingredients/Reference cho mọi cảnh nếu giao diện hỗ trợ.
3. Lấy frame cuối cảnh trước làm first frame cảnh sau.
4. Mỗi cảnh sinh 2–4 phiên bản, chọn theo chuyển động và bố cục, không chỉ theo độ đẹp.
5. Không nhờ Veo tạo chữ; toàn bộ số hiệu, tagline và logo thêm trong hậu kỳ.
6. Khóa cùng một LUT (bộ màu hậu kỳ), film grain và soundtrack cho cả 12 clip.