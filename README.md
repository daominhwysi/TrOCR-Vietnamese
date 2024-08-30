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
| Fine-tuning TrOCR [[1]](https://huggingface.co/Daominhwysi/vietnamese-trocr-large-handwritten/) | **0.025** |
| CRNN/CTC [[2]](https://github.com/TomHuynhSG/Vietnamese-Handwriting-Recognition-OCR) | 0.0476 |
| TrOCR + Rethinking Head [[3]](https://github.com/nguyenhoanganh2002/vnhtr)                             | 0.078 |
| Attetion OCR [[4]](https://github.com/tamlthari/vietnamese_handwritten_text_recognition_cinnamon_ocr) | 0.081 |
| VietOCR [[5]](https://github.com/HungPham2002/Vietnamese-handwritten-text-recognition-using-TransformerOCR) | 0.1021 |

### Pre-trained Model

- [**TrOCR Handwritten Base**](https://huggingface.co/Daominhwysi/trocr-base-vietnamese-handwritten/)
- [**TrOCR Handwritten Large**](https://huggingface.co/Daominhwysi/vietnamese-trocr-large-handwritten/)

## Liên hệ

Nếu có bất kỳ câu hỏi nào hoặc cần thêm thông tin, vui lòng liên hệ với tôi qua email tại daominhwysi@gmail.com hoặc qua Discord với tên người dùng daominhwysi.

### Todo

- [ ] https://arxiv.org/pdf/2105.07983
- [ ] Tích hợp PhoBART để cải thiện phát hiện và sửa lỗi ngữ pháp.
- [x] Triển khai mô hình trocr-large-handwritten.
- [x] Sử dụng Dataset từ 5k ảnh chữ viết tay để huấn luyện thêm.
