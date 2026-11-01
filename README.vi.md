<div align="center">

<img src="icons/icon.svg" alt="Logo COMIC TRANS" width="96" height="96">

# COMIC TRANS

**Dịch truyện tranh, manga và webtoon ngay trên trang web — chữ gốc được xoá theo từng nét, bản dịch được vẽ lại đúng chỗ.**

[![Phiên bản](https://img.shields.io/badge/version-2.6.0-blue?style=flat-square)](https://github.com/ToanCreator/COMIC-TRANS/releases)
[![Giấy phép: MIT](https://img.shields.io/badge/license-MIT-green?style=flat-square)](LICENSE)
[![Miễn phí](https://img.shields.io/badge/gi%C3%A1-mi%E1%BB%85n%20ph%C3%AD-brightgreen?style=flat-square)](#-miễn-phí--mã-nguồn-mở)
[![Mã nguồn mở](https://img.shields.io/badge/open%20source-%E2%9D%A4-red?style=flat-square)](https://github.com/ToanCreator/COMIC-TRANS)
[![Phụ thuộc](https://img.shields.io/badge/npm%20dependencies-0-success?style=flat-square)](#-công-nghệ)
[![AI](https://img.shields.io/badge/AI%20erase-LaMa%20%28optional%29-blueviolet?style=flat-square)](#-công-nghệ)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-orange?style=flat-square)](#-đóng-góp)

[English](README.md) · **🌐 Tiếng Việt** · [简体中文](README.zh-CN.md) · [日本語](README.ja.md)

<!-- ⬇️ Thay các liên kết bên dưới bằng đường dẫn thật trên cửa hàng tiện ích -->
[![Tải cho Firefox](https://img.shields.io/badge/Firefox-T%E1%BA%A3i%20ti%E1%BB%87n%20%C3%ADch-FF7139?style=for-the-badge&logo=firefox-browser&logoColor=white)](https://addons.mozilla.org/firefox/addon/comic-trans/)
[![Chrome](https://img.shields.io/badge/Chrome-S%E1%BA%AFp%20ra%20m%E1%BA%AFt-4285F4?style=for-the-badge&logo=googlechrome&logoColor=white)](https://chromewebstore.google.com/detail/YOUR-EXTENSION-ID)
<!-- Khi bản Chrome được phát hành, đổi "S%E1%BA%AFp%20ra%20m%E1%BA%AFt" thành "T%E1%BA%A3i%20ti%E1%BB%87n%20%C3%ADch" -->

</div>

---

<!-- 📸 Thêm ảnh GIF demo hoặc ảnh trước/sau tại đây, ví dụ:
<p align="center"><img src="docs/demo.gif" alt="Demo COMIC TRANS" width="720"></p>
-->

## ✨ COMIC TRANS là gì?

Phần lớn công cụ dịch truyện chỉ dán một khung chữ đè lên chữ gốc. **COMIC TRANS** đi xa hơn: tiện ích **tìm đúng các điểm ảnh của chữ gốc, xoá chúng, vá lại nền tranh bên dưới rồi vẽ bản dịch vào**, để trang truyện trông như được phát hành bằng ngôn ngữ của bạn.

Bạn dùng **API key [Google Gemini](https://ai.google.dev/) của chính mình**. Mọi việc còn lại — xử lý ảnh, xoá chữ, dàn chữ, lưu bộ nhớ đệm — đều chạy **ngay trong trình duyệt của bạn**.

> Thiết kế ưu tiên điện thoại (chạy được trên Firefox Android), nhưng dùng trên máy tính cũng rất mượt.

## 🚀 Tính năng

| | |
|---|---|
| 🧽 **Xoá chữ thật sự** | Xoá chữ gốc theo từng nét chứ không tô hình chữ nhật nhoè. Viền bong bóng được giữ nguyên. |
| 🖌️ **Dàn chữ thông minh** | Bản dịch được xếp vừa trong bong bóng, dừng khi chạm viền hoặc nét chưa xoá, không đè lên chữ khác. |
| 📜 **Hợp webtoon** | Ảnh dài được cắt tại *hàng trống giữa các khung tranh*, không bao giờ cắt ngang chữ. |
| ⚡ **Nhanh, song song** | Giới hạn song song riêng cho từng key, tự giảm tốc khi gặp lỗi 429 và tự tăng lại khi ổn. Thêm nhiều key để nhân tốc độ. |
| 📱 **Giao diện cảm ứng** | Nút nổi, chạm để chọn ảnh, khoanh vùng bằng ngón tay để dịch lại chữ nhỏ, vùng chạm ≥ 44px. |
| 🔁 **Vẽ lại tức thì** | Vùng chữ được lưu theo từng ảnh — đổi phông hoặc cỡ chữ là vẽ lại ngay, **không tốn thêm lượt gọi API**. |
| 🧠 **Tự sửa lỗi** | Bước rà soát tuỳ chọn sửa từ vô nghĩa/sai chính tả; tiếng Việt tự được khôi phục dấu nếu model trả câu không dấu. |
| 📖 **Thuật ngữ & ghi chú** | Giữ nhất quán tên riêng, quy định xưng hô và văn phong cho từng bộ truyện. |
| 📄 **Xuất PDF** | Lưu chương đã dịch thành PDF (tự sinh, không dùng thư viện PDF). |
| 🌍 **180+ ngôn ngữ** | Dịch giữa mọi cặp ngôn ngữ mà Gemini hỗ trợ. Giao diện có **English, Tiếng Việt, 日本語, 中文**. |
| 🤖 **Xoá chữ bằng AI (LaMa)** *(tuỳ chọn)* | Xoá chữ nằm trực tiếp trên tranh bằng mô hình inpainting **LaMa**, chạy **ngay trong trình duyệt** (ONNX Runtime + WebAssembly). Tải một lần (~208 MB) rồi lưu lại. Gặp lỗi sẽ tự quay về cách nhanh. |
| 🪟 **Bảng & cửa sổ hệ thống** | Nhận ra cửa sổ chỉ số kiểu game, thông báo và bảng chữ dài nhiều dòng như một loại vùng riêng, rồi điền lại như bảng phẳng. |
| 🔒 **Riêng tư từ thiết kế** | Không tài khoản, không theo dõi, không máy chủ riêng. Xem [Quyền riêng tư](#-quyền-riêng-tư--bảo-mật). |

## 🆕 Có gì mới trong 2.6.0

*Các thay đổi so với 2.3.0.*

- 🤖 **Xoá chữ bằng AI với LaMa** — tuỳ chọn, mặc định tắt, chạy hoàn toàn cục bộ. Nhắm tới chữ trên tranh có hoạ tiết, nơi cách điền thông thường có thể hơi mờ. [Chi tiết](#-tuỳ-chọn-xoá-chữ-bằng-ai-lama)
- 🪟 **Loại vùng mới: cửa sổ hệ thống / bảng chữ dài** (thêm cài đặt, mặc định bật).
- 🧵 **Vá đường nối mảnh** — các đường thẳng dày 1–3 px (vết ghép ảnh, mối nối khung tranh) được coi là nền, nên chữ chạm vào đường vẫn xoá được và bong bóng không bị cắt đôi.
- 🫧 **"Túi" bong bóng bền hơn** — nền bong bóng giờ được tính *sau khi* đã biết viền ở đâu và bịt bằng rào 3 px, nên viền "lông nhím" hoặc có khe hở vẫn chứa đúng chữ của nó.
- 📊 **Quản lý model trong Cài đặt** — thanh tiến độ kèm tốc độ, thời gian còn lại, thời gian đã chạy, nút huỷ tải và *Xoá model đã tải*.

## 📦 Cài đặt

### Firefox (khuyên dùng)

1. Mở trang tiện ích → **[Tải COMIC TRANS cho Firefox](https://addons.mozilla.org/firefox/addon/comic-trans/)**
2. Bấm **Thêm vào Firefox**.

### Chrome / Edge / Brave

Sắp ra mắt — xem [Lộ trình](#-lộ-trình). Theo dõi tiến độ tại [Issues](https://github.com/ToanCreator/COMIC-TRANS/issues).

### Từ mã nguồn (mọi bản Firefox, dành cho lập trình viên)

```bash
git clone https://github.com/ToanCreator/COMIC-TRANS.git
```

1. Mở `about:debugging#/runtime/this-firefox`
2. Bấm **Load Temporary Add-on…** và chọn file `manifest.json`
3. Tab Cài đặt sẽ tự mở.

> Tiện ích tạm thời sẽ mất khi tắt Firefox. Muốn cài vĩnh viễn, hãy dùng bản trên cửa hàng hoặc tự ký bản build bằng `web-ext sign`.

## 🧭 Bắt đầu nhanh

1. **Lấy API key Gemini miễn phí** tại [Google AI Studio](https://aistudio.google.com/apikey).
2. Mở **COMIC TRANS → Cài đặt**, dán key (mỗi dòng một key — nhiều key = nhanh hơn), bấm **Kiểm tra key**.
3. Chọn **ngôn ngữ gốc** và **ngôn ngữ đích**.
4. Mở một trang truyện bất kỳ và chạm vào **nút nổi** (góc phải dưới, kéo được).

| Chế độ | Công dụng |
|---|---|
| **Dịch cả trang** | Ảnh đang xem dịch trước, các ảnh khác chạy song song |
| **Ảnh đang xem** | Chỉ dịch ảnh ở giữa màn hình |
| **Từ đây trở xuống** | Ảnh hiện tại và mọi ảnh phía sau — hợp đọc webtoon |
| **Chạm để chọn ảnh** | Chạm vào ảnh nào thì dịch ảnh đó |
| **Khoanh vùng** | Khoanh quanh chữ nhỏ; vùng được phóng to rồi gộp vào kết quả |
| **Tự dịch khi cuộn tới** | Ảnh sắp cuộn tới được dịch trước |
| **Xem gốc / Xuất PDF** | So sánh hoặc lưu thành quả |

**Phím tắt trên máy tính:** `Alt+Shift+T` hiện/ẩn bảng · `Alt+Shift+Y` dịch cả trang · chuột phải lên ảnh → *Dịch ảnh này*.

### 🤖 Tuỳ chọn: xoá chữ bằng AI (LaMa)

1. Vào **Cài đặt → Xoá chữ bằng AI (LaMa)**, bật *Xoá chữ trên tranh bằng AI* (giữ bật mục *Chữ nằm trực tiếp trên tranh*).
2. Bấm **Tải / kiểm tra model**. Chỉ **tải một lần** (~208 MB với model mặc định), có thanh tiến độ, tốc độ, thời gian còn lại và nút huỷ. Model được lưu trong bộ nhớ đệm của trình duyệt; xoá bất cứ lúc nào bằng *Xoá model đã tải*.
3. Dịch như bình thường. Chữ nằm trên tranh có hoạ tiết sẽ được LaMa xoá; bong bóng và bảng phẳng vẫn dùng cách nhanh.

> Nếu bỏ qua bước 2, model sẽ tự bắt đầu tải ở lần dịch đầu tiên.
> Các file ONNX Runtime nằm trong `vendor/` (~40 MB). Nếu bản repo của bạn thiếu, hãy chạy `tools/get-lama-assets.sh` (hoặc `.ps1` trên Windows).
> Chậm hơn cách mặc định, nhất là trên điện thoại. Không bao giờ chặn việc dịch: gặp lỗi thì giữ kết quả của cách nhanh.

## ⚙️ Cơ chế hoạt động

```mermaid
flowchart LR
    A["Trang truyện<br/>(nhiều ảnh lớn)"] --> B["Content script<br/>nhận diện ảnh · giao diện nổi"]
    B --> C["Background<br/>tải ảnh · cắt tại hàng trống"]
    C --> D["Gemini API<br/>khung chữ + bản dịch"]
    D --> E["Web Worker<br/>tìm nét chữ · xoá · dàn chữ"]
    E --> F["Ảnh đã dịch<br/>thay tại chỗ"]
    E -. "chữ trên tranh<br/>(tuỳ chọn)" .-> L["Worker LaMa<br/>ONNX Runtime · WASM"]
    L -.-> E
    E -. "lưu vùng chữ" .-> C
```

1. **Nhận diện** — content script tìm các ảnh cỡ truyện (kể cả ảnh tải lười) và hiện bảng điều khiển nhẹ trong Shadow DOM, không đụng CSS của trang.
2. **Cắt lát** — ảnh dài được cắt tại những hàng ngang yên tĩnh nhất giữa các khung tranh, không cắt theo chiều cao cố định.
3. **Giao cho model *ít việc hơn*** — Gemini chỉ trả về phần mà mô hình thị giác làm tốt: **khung chữ, bản dịch và loại vùng** (bong bóng, chú thích, chữ tự do, tiếng động, bảng hệ thống). Phần nặng được xử lý ngay trên máy.
4. **Tìm đúng nét chữ** — khung của model thường nhỏ hơn hoặc lệch so với chữ thật, nên chỉ dùng làm "hạt giống". Worker lan theo các nét chữ sát nhau trong cùng bong bóng (flood-fill trên nền cục bộ; top-hat / black-hat cho chữ nằm trên tranh) để có mặt nạ chữ đầy đủ. Đường nối mảnh và khe hở ở viền được vá trước để các bong bóng không dính vào nhau.
5. **Xoá chữ — đường nhanh** — các điểm ảnh trong mặt nạ được điền lại (push-pull + thêm hạt nhiễu cho khớp tranh) nên vùng sửa hoà vào nền. Nếu không tìm thấy chữ, **ảnh được giữ nguyên**. Bong bóng và nền phẳng (khung màu, trời một màu) luôn dùng cách chính xác này.
6. **Xoá chữ — đường AI (tuỳ chọn)** — khi bật *Xoá chữ bằng AI* và chữ nằm trên tranh có hoạ tiết thật sự, kết quả được tinh chỉnh bằng **LaMa**: cắt một hình vuông có nhiều ngữ cảnh quanh mặt nạ, đổi về **512 × 512** và gửi tới một worker riêng duy nhất chạy model qua ONNX Runtime Web (WebAssembly). Chỉ các điểm ảnh **nằm trong mặt nạ** được dán lại; phần còn lại không bị đổi. Gặp lỗi hoặc quá thời gian thì giữ kết quả của đường nhanh.
7. **Dàn chữ** — bản dịch được ngắt dòng và xếp vừa vùng trống, dừng trước viền hoặc nét chưa xoá.
8. **Lưu đệm** — vùng chữ được lưu theo từng ảnh; đổi kiểu chữ là vẽ lại ngay, không tốn phí.

## 🛠️ Điểm nhấn kỹ thuật

*Dành cho người tò mò — và cho ai đang xem xét mã nguồn.*

- **Gần như không phụ thuộc.** JavaScript thuần (ES2020), WebExtension API, Web Worker. Không bundler, không framework, không `node_modules` khi chạy. Thành phần bên thứ ba duy nhất là **ONNX Runtime Web** (đặt sẵn trong `vendor/`), chỉ được nạp khi bật xoá chữ bằng AI.
- **Lõi thuần, dễ kiểm thử.** `worker/core.js` không chạm DOM, nên cùng một thuật toán chạy được trong Web Worker **và** trong Node để test.
- **Pipeline thị giác máy tính tự viết.** Phân tích màu chủ đạo, thống kê nét theo hàng/cột, phép toán hình thái học (mở/đóng), gom thành phần liên thông, vá đường nối, inpainting push-pull, ước lượng nhiễu + tạo hạt, loại trùng bằng IoU.
- **Tích hợp AI inpainting cẩn thận.** Một worker LaMa dùng chung phục vụ cả nhóm worker ảnh qua các cổng `MessageChannel` riêng (model chỉ nạp một lần, không nhân bản theo worker); yêu cầu được xếp hàng tuần tự; logic cắt vùng/tạo tensor/dán lại nằm ở một module thuần (`lamafill.js`); khoảng giá trị đầu ra của model (0–1 hay 0–255) được tự nhận biết; có timeout 120 giây và cơ chế quay về cách nhanh, nên AI không thể làm hỏng một lần dịch.
- **Tải model đúng cách.** Tải dạng luồng kèm tiến độ, tốc độ, thời gian còn lại; cấp phát sẵn bộ đệm theo `Content-Length` để không tốn gấp đôi RAM trên điện thoại; model được lưu bền trong Cache Storage; kiểm tra file runtime *trước khi* tải hàng trăm MB.
- **Client API bền bỉ.** Tự dò model chấp nhận cấu hình nào (thinking → safety → JSON schema) bằng một ảnh nhỏ rồi hạ cấp êm; cứu JSON bị cắt giữa chừng; xử lý 429 bằng song song thích ứng theo từng key; nhận ra các key dùng chung hạn mức của một project.
- **Không làm đơ trang.** Phần xử lý điểm ảnh nặng chạy trong nhóm Worker có số lượng theo số nhân CPU.
- **Tự viết bộ xuất PDF.** Bản PDF được tạo bằng một bộ serializer PDF nhỏ viết tay.
- **Đa ngôn ngữ ngay từ đầu.** Giao diện 4 ngôn ngữ, tự nhận theo trình duyệt.
- **Kiểm thử nhiều tầng.** Test thuật toán trên trang truyện giả lập, test đơn vị và test luồng (model từ chối cấu hình, quota 0, 429, JSON bị cắt, key sai, 404, thiếu quyền tuỳ chọn), cùng test E2E/cảm ứng trên trình duyệt thật bằng Playwright ở khung nhìn điện thoại.

## 🔒 Quyền riêng tư & bảo mật

- **API key chỉ lưu trong trình duyệt của bạn** (`browser.storage.local`) và **chỉ** được gửi tới `generativelanguage.googleapis.com`.
- Tiện ích chỉ nói chuyện với **hai loại máy chủ**: **Gemini API** (để dịch) và — *chỉ khi bạn bật xoá chữ bằng AI* — **tải model một lần từ `huggingface.co`** (địa chỉ có thể sửa trong Cài đặt). Ảnh truyện của bạn **không bao giờ** được gửi tới Hugging Face; model chạy cục bộ và sau đó được lưu trong trình duyệt.
- Không phân tích, không theo dõi, không tài khoản.
- ⚠️ Để dịch, **các ảnh bạn chọn được gửi tới Gemini API của Google**. Áp dụng điều khoản của Google theo gói key của bạn (với key miễn phí, Google có thể dùng dữ liệu theo chính sách hiện hành — hãy tự đọc kỹ). Đừng dịch nội dung bạn không muốn gửi đi.
- Đừng chia sẻ ảnh chụp màn hình lộ header `x-goog-api-key`. Nếu lỡ lộ key, hãy thu hồi và tạo key mới.

## 🧰 Công nghệ

`JavaScript` · `WebExtensions (Firefox, Manifest V2)` · `Web Workers` · `Canvas / ImageData` · `Google Gemini API` · `ONNX Runtime Web (WASM)` · `LaMa inpainting (ONNX)` · `Node.js + Playwright (kiểm thử)`

## 🗂️ Cấu trúc dự án

```
COMIC-TRANS/
├── manifest.json          # manifest của WebExtension (v2.6.0)
├── background/
│   ├── main.js            # điều phối: tải ảnh, cắt lát, hàng đợi, bộ nhớ đệm, song song theo key,
│   │                      #   nhóm worker + tải/lưu/khởi động model LaMa
│   ├── gemini.js          # client Gemini: prompt, phân tích kết quả, thử lại, tự kiểm tra
│   └── settings.js        # giá trị mặc định & lưu trữ
├── content/content.js     # nhận diện ảnh, bảng nổi (Shadow DOM), cử chỉ cảm ứng, xuất PDF
├── worker/
│   ├── core.js            # thuật toán thuần: mặt nạ chữ, đường nối, inpainting, dàn chữ, cắt lát
│   ├── worker.js          # worker ảnh: cắt lát, xoá chữ, dàn chữ, client LaMa
│   ├── lamafill.js        # tiền/hậu xử lý LaMa (thuần): chọn vùng, tensor 512×512, dán lại
│   └── lama_worker.js     # worker duy nhất chạy phiên ONNX
├── vendor/                # ONNX Runtime Web 1.17.3 (JS + WASM) — chỉ dùng cho xoá chữ bằng AI
├── options/               # trang cài đặt (gồm phần quản lý model)
├── shared/                # chuỗi giao diện (en/vi/ja/zh) & danh sách ngôn ngữ
├── tools/                 # get-lama-assets.sh / .ps1 — tải các file trong vendor/
└── tests/                 # test đơn vị, luồng, thuật toán và E2E trên trình duyệt
```

## 🧪 Phát triển & kiểm thử

```bash
cd tests
python3 make_synth.py && python3 make_tall.py && python3 make_widths.py   # tạo trang truyện giả lập
node test_units.js && node test_flow.js && node run_core.js               # đơn vị + luồng + lõi
node browser_worker_test.js && node browser_content_test.js && node browser_e2e_test.js  # cần Playwright + Chromium
```

> **Tình trạng thực tế:** các test tự động đã chạy với Worker thật, content script thật và luồng background thật trong **Chromium**, với Gemini được giả lập. Việc kiểm thử trên Firefox thật (máy tính & Android), Gemini API thật và nhiều trang truyện thật vẫn đang tiếp tục — rất hoan nghênh báo lỗi.
>
> Rất hoan nghênh phản hồi về đường xoá chữ bằng AI trên thiết bị thật (nhất là điện thoại).

## ⚠️ Giới hạn đã biết

- **Xoá chữ bằng AI** (tuỳ chọn): model mặc định **nặng ~208 MB**, chỉ tải một lần; khởi động mất **10–60 giây** (điện thoại có thể lâu hơn). Model chạy trên **CPU qua WebAssembly, một luồng** (đa luồng cần trang cách ly nguồn gốc mà tiện ích không có) nên chậm hơn cách mặc định. Model làm việc ở 512 × 512, nên vùng rất lớn sẽ bị xử lý ở độ phân giải thấp hơn. Chỉ áp dụng cho chữ nằm trên tranh có hoạ tiết.
- Khi không bật AI, chữ nằm trên tranh nhiều chi tiết được xoá sạch nhưng chỗ điền lại có thể hơi mờ — hãy bật LaMa, hoặc tắt mục *"Chữ nằm trực tiếp trên tranh"* nếu muốn để nguyên.
- Chữ xoay nghiêng/cong và chữ dính sát viền bong bóng chưa được xử lý riêng; chữ dọc chỉ ước lượng cỡ.
- Chỉ dùng phông đã cài trong máy (hãy chọn phông có đủ ký tự cho ngôn ngữ đích).
- Ảnh nằm trong `<iframe>` chưa được hỗ trợ.

## 📍 Lộ trình

- [ ] 🟦 Bản **Chrome / Edge / Brave** (Manifest V3, offscreen document)
- [x] 🧠 Inpainting thần kinh (LaMa qua `onnxruntime-web`) cho chữ trên tranh — **đã có từ 2.6.0 (tuỳ chọn)**
- [ ] 🚀 Xoá chữ AI nhanh hơn (backend WebGPU, model lượng tử hoá nhỏ hơn)
- [ ] 🖥️ Chế độ máy chủ riêng tuỳ chọn (detector + OCR + inpainting trên GPU; Gemini chỉ dịch văn bản)
- [ ] ⏩ Streaming phản hồi để bắt đầu vẽ trước khi model trả xong
- [ ] 🌐 Thêm ngôn ngữ giao diện (hoan nghênh PR!)

## 🤝 Đóng góp

Mọi đóng góp, dù nhỏ, đều được chào đón — báo lỗi, bản dịch giao diện, cải tiến thuật toán, tài liệu.

1. Fork repo và tạo nhánh: `git checkout -b feature/y-tuong-cua-ban`
2. Thực hiện thay đổi và chạy các test trong `tests/`
3. Mở Pull Request mô tả *làm gì* và *vì sao*

**Dịch README hoặc giao diện:** sao chép `README.md` thành `README.<mã-ngôn-ngữ>.md` (ví dụ `README.ko.md`) và thêm vào thanh ngôn ngữ ở đầu trang; chuỗi giao diện nằm trong `shared/i18n.js`.

## 💚 Miễn phí & mã nguồn mở

COMIC TRANS **miễn phí 100%** — không quảng cáo, không thu phí, không gói trả phí — và là **mã nguồn mở** theo **Giấy phép MIT**. Bạn có thể đọc, fork, học hỏi và cải tiến. Bạn chỉ trả tiền trực tiếp cho Google khi vượt hạn mức miễn phí của gói API.

## 🙏 Ghi công & thành phần bên thứ ba

Mã nguồn của COMIC TRANS theo giấy phép MIT. Các thành phần bên thứ ba giữ giấy phép riêng của chúng:

- **LaMa** — *Resolution-robust Large Mask Inpainting with Fourier Convolutions*, Suvorov và cộng sự, WACV 2022 · [advimman/lama](https://github.com/advimman/lama) · Apache-2.0
- **Bản xuất ONNX của LaMa** — [Carve/LaMa-ONNX](https://huggingface.co/Carve/LaMa-ONNX) · Apache-2.0. Model **không được đóng gói** trong repo này; nó được tải khi bạn yêu cầu.
- **ONNX Runtime Web 1.17.3** — Microsoft · MIT · đặt sẵn trong `vendor/`
- **Google Gemini API** — OCR + dịch

## 📄 Giấy phép

Phát hành theo [Giấy phép MIT](LICENSE). Truyện tranh và webtoon bạn dịch vẫn thuộc quyền sở hữu của tác giả — hãy ủng hộ tác giả gốc, tôn trọng bản quyền và điều khoản sử dụng của từng trang web.

## 👤 Tác giả

Được làm bằng ☕ bởi **[ToanCreator](https://github.com/ToanCreator)**.
Nếu dự án giúp ích cho bạn, một ⭐ trên repo là niềm động viên rất lớn!

<div align="center">

[⬆ Lên đầu trang](#comic-trans)

</div>
