# TrOCR Handwritten Vietnamese

Dự án này là một mô hình nhận diện chữ viết tay tiếng Việt sử dụng TrOCR (Transformer-based Optical Character Recognition). Để cải thiện khả năng nhận diện, chúng tôi đã sử dụng PhoBERT làm tokenizer.

## Cấu hình Mô hình

- **Mô hình cơ sở (Base Model):** TrOCR Handwritten Base
- **Tokenizer:** PhoBERT

## Kết quả Huấn luyện

| Mô hình                    | Số lượng tham số | CER   |
|----------------------------|---------------------------|-------|
| TrOCR handwritten base      | 348M                      | 0.064 |
| TrOCR handwritten large     | 558M                      | 0.032    |

Bảng này thể hiện sự khác biệt giữa hai mô hình TrOCR handwritten base và large về số lượng tham số và CER (Character Error Rate).

**Chú thích:**
- **Training Loss:** Mất mát trong quá trình huấn luyện.
- **Validation Loss:** Mất mát trên tập dữ liệu kiểm tra.
- **CER (Character Error Rate):** Tỷ lệ lỗi ký tự.

Pre-trained Base Model is available at [Hugging Face Model Hub](https://huggingface.co/Daominhwysi/trocr-base-vietnamese-handwritten/tree/main).

## So sánh State-of-the-Art

| Phương Pháp                                                                                                  | CER (Character Error Rate) |
|--------------------------------------------------------------------------------------------------------------|----------------------------|
| VietOCR ([Vietnamese Handwritten Text Recognition Using TransformerOCR](https://github.com/HungPham2002/Vietnamese-handwritten-text-recognition-using-TransformerOCR)) | 0.1021                     |
| CRNN/CTC ([Vietnamese Handwriting Recognition OCR](https://github.com/TomHuynhSG/Vietnamese-Handwriting-Recognition-OCR))             | 0.0476                     |
| TrOCR + Rethinking Head ([VNHTR](https://github.com/nguyenhoanganh2002/vnhtr))                               | 0.078                       |
| Pre-trained Transformer with PhoBERT ([Our Model](https://huggingface.co/Daominhwysi/trocr-base-vietnamese-handwritten/tree/main)) | **0.032**                    |

## Liên hệ

Nếu bạn có bất kỳ câu hỏi nào hoặc cần thêm thông tin, vui lòng liên hệ với daominhwysi@gmail.com hoặc daominhwysi trên Discord.

### Todo

- [ ] Thêm PhoBART để chữa lỗi ngữ pháp
- [x] Sử dụng mô hình trocr-large-handwritten 
- [ ] Sử dụng Dataset từ 5k ảnh chữ viết tay
