# TrOCR Handwritten Vietnamese

Dự án này phát triển một mô hình nhận dạng chữ viết tay tiếng Việt, sử dụng TrOCR (Transformer-based Optical Character Recognition). Để cải thiện hiệu quả nhận dạng, mình đã tích hợp PhoBERT làm tokenizer.
# Datasets

Datasets được lấy từ VNonDB và CinamonAI.
https://huggingface.co/datasets/Daominhwysi/vietnamese_handwritten

## Kết quả Huấn luyện

| Mô hình                    | Số lượng tham số | CER ↓ |
|----------------------------|-----------------|-------|
| TrOCR handwritten base      | 348M            | - |
| TrOCR handwritten large     | 558M            | - |

- **CER (Character Error Rate):** Tỷ lệ lỗi ký tự, giá trị càng thấp, mô hình càng chính xác.

### Pre-trained Model

- [**TrOCR Handwritten Base**](https://huggingface.co/Daominhwysi/trocr-base-vietnamese-handwritten/)
- [**TrOCR Handwritten Large**](https://huggingface.co/Daominhwysi/vietnamese-trocr-large-handwritten-v2/)

## Liên hệ

Nếu có bất kỳ câu hỏi nào hoặc cần thêm thông tin, vui lòng liên hệ với tôi qua email tại daominhwysi@gmail.com hoặc qua Discord với tên người dùng daominhwysi.

### Todo

- [ ] https://arxiv.org/pdf/2105.07983
- [ ] Tích hợp PhoBART để cải thiện phát hiện và sửa lỗi ngữ pháp.
- [x] Triển khai mô hình trocr-large-handwritten.
- [x] Sử dụng Dataset từ 5k ảnh chữ viết tay để huấn luyện thêm.
