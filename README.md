# TrOCR Handwritten Vietnamese

Dự án này là một mô hình nhận diện chữ viết tay tiếng Việt sử dụng TrOCR (Transformer-based Optical Character Recognition). Để cải thiện khả năng nhận diện, chúng tôi đã sử dụng PhoBERT làm tokenizer.

## Cấu hình Mô hình

- **Mô hình cơ sở (Base Model):** TrOCR Handwritten Base
- **Tokenizer:** PhoBERT

## Kết quả Huấn luyện

| Bước | Training Loss | Validation Loss | CER    |
|------|---------------|-----------------|--------|
| 400  | 0.088000      | 0.230644        | 0.077707 |
| 800  | 0.053600      | 0.201272        | 0.073229 |
| 1200 | 0.006400      | 0.218866        | 0.069131 |
| 1600 | 0.004000      | 0.220150        | 0.064510 |
| 2000 | 0.002700      | 0.220505        | 0.066606 |
| 2400 | 0.000900      | 0.221266        | 0.065320 |

**Chú thích:**
- **Training Loss:** Mất mát trong quá trình huấn luyện.
- **Validation Loss:** Mất mát trên tập dữ liệu kiểm tra.
- **CER (Character Error Rate):** Tỷ lệ lỗi ký tự.

Pre-trained Model is available at [Hugging Face Model Hub](https://huggingface.co/Daominhwysi/trocr-base-vietnamese-handwritten/tree/main).

## So sánh State-of-the-Art


| Phương Pháp                                                                                                  | CER (Character Error Rate) |
|--------------------------------------------------------------------------------------------------------------|-----------------------------|
| VietOCR ([Vietnamese Handwritten Text Recognition Using TransformerOCR](https://github.com/HungPham2002/Vietnamese-handwritten-text-recognition-using-TransformerOCR)) | 0.1021                      |
| CRNN/CTC ([Vietnamese Handwriting Recognition OCR](https://github.com/TomHuynhSG/Vietnamese-Handwriting-Recognition-OCR))             | 0.0476              |
| Pre-trained Transformer ([TrOCR Vietnamese (Our Model)](https://huggingface.co/Daominhwysi/trocr-base-vietnamese-handwritten/tree/main)) | 0.0653            |


## Liên hệ

Nếu bạn có bất kỳ câu hỏi nào hoặc cần thêm thông tin, vui lòng liên hệ với daominhwysi@gmail.com hoặc daominhwysi trên Discord.

### Todo

- [ ] Thêm PhoBERT để chữa lỗi ngữ pháp
- [ ] Sử dụng mô hình trocr-large-handwritten 
- [ ] Sử dụng Dataset từ 5k ảnh chữ viết tay
