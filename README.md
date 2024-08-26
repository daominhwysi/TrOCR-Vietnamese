# TrOCR Handwritten Vietnamese

Dự án này phát triển một mô hình nhận dạng chữ viết tay tiếng Việt, sử dụng TrOCR (Transformer-based Optical Character Recognition). Để cải thiện hiệu quả nhận dạng, chúng tôi đã tích hợp PhoBERT làm tokenizer.

## Cấu hình Mô hình

- **Mô hình nền tảng:** TrOCR Handwritten Base
- **Tokenizer:** PhoBERT

## Kết quả Huấn luyện

| Mô hình                    | Số lượng tham số | CER ↓ |
|----------------------------|-----------------|-------|
| TrOCR handwritten base      | 348M            | 0.064 |
| TrOCR handwritten large     | 558M            | 0.025 |

- **CER (Character Error Rate):** Tỷ lệ lỗi ký tự, giá trị càng thấp, mô hình càng chính xác.
## So sánh với các phương pháp State-of-the-Art

| Phương pháp                                                                                                  | CER ↓ |
|--------------------------------------------------------------------------------------------------------------|-------|
| VietOCR ([Vietnamese Handwritten Text Recognition Using TransformerOCR](https://github.com/HungPham2002/Vietnamese-handwritten-text-recognition-using-TransformerOCR)) | 0.1021|
| TrOCR + Rethinking Head ([VNHTR](https://github.com/nguyenhoanganh2002/vnhtr))                               | 0.078 |
| CRNN/CTC ([Vietnamese Handwriting Recognition OCR](https://github.com/TomHuynhSG/Vietnamese-Handwriting-Recognition-OCR)) | 0.0476|
| Fine-tuning TrOCR ([Mô hình của chúng tôi](https://huggingface.co/Daominhwysi/vietnamese-trocr-large-handwritten/upload/main)) | **0.025**|

Bảng trên tổng hợp các phương pháp nhận dạng chữ viết tay tiếng Việt hàng đầu và kết quả CER tương ứng.

### Pre-trained Model

- [**TrOCR Handwritten Base**](https://huggingface.co/Daominhwysi/trocr-base-vietnamese-handwritten/tree/main)
- [**TrOCR Handwritten Large**](https://huggingface.co/Daominhwysi/vietnamese-trocr-large-handwritten/upload/main)

## Liên hệ

Nếu có bất kỳ câu hỏi nào hoặc cần thêm thông tin, vui lòng liên hệ với tôi qua email tại daominhwysi@gmail.com hoặc qua Discord với tên người dùng daominhwysi.

### Todo

- [ ] Tích hợp PhoBART để cải thiện phát hiện và sửa lỗi ngữ pháp.
- [x] Triển khai mô hình trocr-large-handwritten.
- [ ] Sử dụng Dataset từ 5k ảnh chữ viết tay để huấn luyện thêm.
