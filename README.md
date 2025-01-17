# SpamFilter-for-Vietnamese-Travel-Review
Model lọc spam cho các bình luận tiếng Việt về chủ đề du lịch. Đây là model được train để sử dụng trong môn Lập trình Python - Nhóm 12 - NLU 2024-2025

---
### Về model SpamFilter
- Model này sử dụng `Stacking Ensemble Learning` và train bằng `scikit-learn`:
  - **Base Model** là `Multinomial Naive Bayes` và `Random Forest`
  - **Meta Model** là `LogisticRegression`
- Sử dụng `Bag of Word` để trích xuất các vector đặc trưng cho input
- Model sử dụng Python `3.10`

### Dataset dùng để train model
- Dataset của model này bị chắp vá (do không tìm đủ lượng dataset có chất lượng tốt để train) nên kết quả đôi lúc sẽ không chuẩn xác
- Data train gồm:
  - 20000 bình luận gán nhãn không spam (Nhãn 0)
  - 20000 bình luận gán nhãn spam (Nhãn 1)
- Data test gồm:
  - 5231 bình luận gán nhãn không spam (Nhãn 0)
  - 3986 bình luận gán nhãn spam (Nhãn 1)
- Độ chính xác của model khi test đạt `94%`
- Đặc biệt có tác dụng hơn với các bình luận tiếng Việt ở Airbnb (do nguồn dataset)

### Các thư viện yêu cầu:
- `scikit-learn` 1.6.1 - Cho việc train model
- `underthesea` 6.8.4 - Cho việc tiền xử lý input



##### Đây là model đầu tiên của một người chỉ mới tiếp xúc với ML nên vẫn còn nhiều sai sót ;-;