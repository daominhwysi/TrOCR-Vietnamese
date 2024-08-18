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

---

## So sánh State-of-the-Art
---

## So sánh State-of-the-Art

| Phương Pháp                                                                                                  | CER (Character Error Rate (Lower is better) |
|--------------------------------------------------------------------------------------------------------------|-----------------------------|
| [Transformer-based](https://github.com/HungPham2002/Vietnamese-handwritten-text-recognition-using-TransformerOCR) | 0.1021                      |
| [CRNN/CTC](https://github.com/TomHuynhSG/Vietnamese-Handwriting-Recognition-OCR)         | 0.0476                      |
| [Pre-trained TransformerOCR Vietnamese (Our Model)](https://huggingface.co/Daominhwysi/trocr-base-vietnamese-handwritten/tree/main) | 0.0645                  |
---

Nếu cần thêm bất kỳ điều chỉnh nào, hãy cho tôi biết!

## Liên hệ

Nếu bạn có bất kỳ câu hỏi nào hoặc cần thêm thông tin, vui lòng liên hệ với daominhwysi@gmail.com hoặc daominhwysi trên Discord.

