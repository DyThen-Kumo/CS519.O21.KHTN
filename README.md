<p align="center">
  <a href="https://www.uit.edu.vn/"><img src="https://www.uit.edu.vn/sites/vi/files/banner.png"></a>
<h1 align="center"><b>CS519.O21.KHTN - SCIENTIFIC RESEARCH METHODOLOGY</b></h1>

## Giới thiệu
* Tên môn học: PHƯƠNG PHÁP LUẬN NGHIÊN CỨU KHOA HỌC - SCIENTIFIC RESEARCH METHODOLOGY
* Mã lớp: CS519.O21.KHTN
* Năm học: Học kỳ 4 (2023-2024)

### Giảng viên
* PGS.TS Lê Đình Duy - duyld@uit.edu.vn

### Thành viên nhóm

| STT | Họ và tên | MSSV | Email | Github |
| :---: | --- | --- | --- | --- |
| 1 | Nguyễn Duy Thắng | 22521333 | 22521333@gm.uit.edu.vn | [github](https://github.com/DyThen-Kumo) |

### Tóm tắt
Nhận diện chữ viết tay tiếng Việt gặp nhiều thách thức do tính đa dạng và phức tạp của các ký tự và dấu thanh. Các mô hình truyền thống thường kết hợp CNN để xử lý hình ảnh, RNN để tạo ra đầu ra và một mô hình ngôn ngữ để sửa lỗi chính tả, dẫn đến hệ thống phức tạp và khó tối ưu hóa. Kiến trúc Transformer, đã đạt nhiều thành công trong xử lý ngôn ngữ tự nhiên (NLP) và thị giác máy tính (CV), có thể giải quyết những hạn chế này. Tuy nhiên, các mô hình OCR dựa trên Transformer hiện nay thường được huấn luyện trên bộ dữ liệu tiếng Anh, giảm hiệu quả khi áp dụng cho tiếng Việt. Việc huấn luyện lại từ đầu rất tốn kém tài nguyên và thời gian. Liệu có cách nào để khắc phục điều đó? Câu trả lời là tinh chỉnh (finetuning) một mô hình đã được đào tạo trên ngôn ngữ có bảng chữ cái Latinh để đào tạo thêm về tiếng Việt vì mô hình đã học được một số nét chữ cơ bản. Nghiên cứu này nhằm finetuning mô hình OCR sử dụng kiến trúc Transformer (TrOCR) để nhận diện chữ viết tay tiếng Việt, mang lại hiệu suất cao hơn và khả năng ứng dụng rộng rãi hơn.

## Bài toán
Nhận diệng chữ viết tay tiếng Việt bằng OCR dựa trên Transformer (TrcOCR).
- Input: Một hoặc nhiều hình ảnh chữ viết tay tiếng Việt và dataset chữ viết tay tiếng Việt đã được gán nhãn.
- Output: Văn bản được trích xuất từ hình ảnh đầu vào. Văn bản này có thể được lưu dưới dạng chuỗi ký tự hoặc dưới dạng tệp văn bản (.txt) hoặc các định dạng tài liệu khác (ví dụ: .docx, .pdf).
### Computational Thinking

| Step | Decomposition | Abstraction | Pattern Recognition | Algorithm |
| :---: | --- | --- | --- | ---|
| 1 | Thu thập dữ liệu |  |  |  |
| 2 | Nhận diện chữ viết tay tiếng Việt | Bài toán nhận diện chữ viết tay bằng Transformer nói chung | Bài toán nhận diện chữ viết tay dựa trên Transformer đã được đào tạo trước nhưng chỉ trên dữ liệu tiếng Anh | Finetuning mô hình TrOCR được đào tạo trên dữ liệu tiếng Anh và đào tạo lại trên dữ liệu tiếng Việt. |

## Data
* Dữ liệu được tham khảo và tổng hợp từ Kaggle: [link](https://www.kaggle.com/datasets/ducthinhhust/vietocr)
* Label (ground truth) được lấy ra và tổng hợp trong folder gt.
* Dữ liệu sau đó được tách ra thành các tập train, test, val:

|  | Train | Test | Val |
| :---: | --- | --- | --- |
| Kích thước | 5097 | 1024 | 1161 |

## Kết quả
* Chi tiết ở trong slide.

## Reference
[1]. Minghao Li, Tengchao Lv, Jingye Chen, Lei Cui, Yijuan Lu, Dinei A. F. Florêncio, Cha Zhang, Zhoujun Li, Furu Wei:
TrOCR: Transformer-Based Optical Character Recognition with Pre-trained Models. AAAI 2023: 13094-13102

[2]. Jan Kohút, Michal Hradis:
Fine Tuning Is a Surprisingly Effective Domain Adaptation Baseline in Handwriting Recognition. CoRR abs/2302.06308 (2023)

[3]. Ashish Vaswani, Noam Shazeer, Niki Parmar, Jakob Uszkoreit, Llion Jones, Aidan N. Gomez, Lukasz Kaiser, Illia Polosukhin:
Attention is All You Need. NIPS 2017: 5998-6008

[4]. Michael Jungo, Lars Vögtlin, Atefeh Fakhari, Nathan Wegmann, Rolf Ingold, Andreas Fischer, Anna Scius-Bertrand:
Impact of Ground Truth Quality on Handwriting Recognition. CoRR abs/2312.09037 (2023)

[5]. Vittorio Pippi, Silvia Cascianelli, Christopher Kermorvant, Rita Cucchiara:
How to Choose Pretrained Handwriting Recognition Models for Single Writer Fine-Tuning. CoRR abs/2305.02593 (2023)

[6]. Mst. Shapna Akter, Hossain Shahriar, Alfredo Cuzzocrea, Nova Ahmed, Carson K. Leung:
Handwritten Word Recognition using Deep Learning Approach: A Novel Way of Generating Handwritten Words. CoRR abs/2303.07514 (2023)
