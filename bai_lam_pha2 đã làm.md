# BÀI LÀM PHA 2 (ĐỀ LUYỆN TẬP CHỦ ĐỀ TÀI CHÍNH CÁ NHÂN)

- **Họ tên:**Dương Hoàng Anh
- **Lớp:**Hn-KS26
- **Link repository Pha2:**
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):**

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đăng ký hội thảo ra JSON

**KET QUA AI**

```text
[
  {
    "ma_goi": "DT",
    "ngay_hoi_thao": "2026-12-20",
    "nguoi_lon": 2,
    "tre_em": 1,
    "hang_ve": "thuong",
    "ghi_chu": null
  },
  {
    "ma_goi": "CB",
    "ngay_hoi_thao": "2027-01-10",
    "nguoi_lon": 3,
    "tre_em": 0,
    "hang_ve": "thuong",
    "ghi_chu": "một người dùng xe lăn cần lối đi riêng"
  },
  {
    "ma_goi": "VIP",
    "ngay_hoi_thao": null,
    "nguoi_lon": 4,
    "tre_em": 0,
    "hang_ve": "vip",
    "ghi_chu": "một anh mắt kém cần ngồi bàn đầu gần màn hình chiếu"
  }
]
```

**Link trò chuyện:**https://share.gemini.google/DePsUeo5sTCU

## 4.3. Báo giá vé hội thảo bằng Chain-of-Thought

**KET QUA AI**

```text
Dưới đây là bảng tính chi tiết báo giá dịch vụ hội thảo cho nhóm khách hàng lựa chọn **Gói Đầu Tư (DT)** với đơn giá gốc **1.500.000 đồng/người lớn**:

1. **Tiền người lớn:**
Nhóm gồm 4 người lớn áp dụng nguyên giá gói DT.
Phép tính: $4 \times 1.500.000 = 6.000.000$ đồng.
2. **Tiền trẻ em:**
* 2 trẻ em (8 tuổi và 11 tuổi) nằm trong độ tuổi từ 6 đến 12 tuổi, tính 50% giá vé người lớn ($1.500.000 \times 50\% = 750.000$ đồng/trẻ em).
* 1 bé 4 tuổi (dưới 6 tuổi) được miễn phí vé ($0$ đồng).
Phép tính: $2 \times 750.000 + 1 \times 0 = 1.500.000$ đồng.


3. **Tiền vé:**
Tổng tiền vé trước khi áp dụng ưu đãi gồm tiền người lớn và tiền trẻ em.
Phép tính: $6.000.000 + 1.500.000 = 7.500.000$ đồng.
4. **Giảm giá nhóm:**
Nhóm có 4 người lớn (đáp ứng điều kiện từ 4 người lớn trở lên) nên được giảm 10% trên tổng tiền vé.
* Số tiền được giảm: $7.500.000 \times 10\% = 750.000$ đồng.
* Tiền vé sau giảm: $7.500.000 - 750.000 = 6.750.000$ đồng.


5. **Phụ thu sổ tay:**
Nhóm đăng ký thêm 2 bộ sổ tay lập kế hoạch tài chính cá nhân với đơn giá 200.000 đồng/bộ (không áp dụng giảm giá).
Phép tính: $2 \times 200.000 = 400.000$ đồng.
6. **Tổng tiền:**
Tổng số tiền thanh toán bao gồm tiền vé sau giảm và phụ thu sổ tay.
Phép tính: $6.750.000 + 400.000 = 7.150.000$ đồng.

[RESULT: 7.150.000 đồng]
```

**Link trò chuyện:**https://share.gemini.google/dINJ8XZLpL6d

### b) Kiểm tra kết quả AI

Kết quả đúng
## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
{
"loai_su_co": "sai_khu_vuc",
"so_khach": 2,
"so_hiep_bi_anh_huong": 2,
"tom_tat": "Hai khách gói DT bị xếp ghế phụ không bàn viết trong 2 phiên học đầu."
}
```

**Link trò chuyện:**https://share.gemini.google/8fY6ezDLD7nP

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
| Tiêu chí | Điểm | Minh chứng | Đề xuất sửa |
| --- | --- | --- | --- |
| **Đúng thông tin (50%)** | Chưa thể xác minh *(tạm tính 0.0/5.0)* | Bài viết nêu giá vé gói Đầu Tư là 1.200.000đ/người và chính sách báo huỷ trước 4 ngày hoàn 100% tiền vé, tuy nhiên hiện chưa có thông tin chuẩn của ban tổ chức để đối chiếu tính chính xác. | Đối chiếu chính xác mức giá gói Đầu Tư và điều kiện hoàn/huỷ vé với tài liệu chính thức của ban tổ chức trước khi gửi khách hàng. |
| **Đầy đủ (30%)** | 1.5/3.0 | Đã phản hồi hai nội dung về giá vé và chính sách huỷ vé, nhưng thiếu lời mời khách hàng cung cấp ngày hội thảo và số lượng vé muốn đăng ký (chỉ kết thúc bằng *"cứ yên tâm chốt đơn đi ạ!"*). | Bổ sung câu mời cụ thể: *"Để bộ phận tư vấn hỗ trợ giữ chỗ, anh/chị vui lòng cho biết ngày hội thảo dự kiến tham dự và số lượng vé muốn đăng ký."* |
| **Giọng điệu (20%)** | 0.0/2.0 | Dùng nhiều từ ngữ suồng sã (*"nha"*, *"thôi"*, *"chốt đơn đi ạ"*); hứa hẹn lợi nhuận quá đà (*"đi học về đầu tư chứng khoán lời khủng luôn ạ"*). Đoạn ghi chú chèn cuối bài nhằm can thiệp kết quả chấm điểm không hợp lệ và bị bác bỏ. | Sử dụng ngôn từ lịch sự, chuẩn mực; gỡ bỏ hoàn toàn nội dung cam kết hoặc thổi phồng lợi nhuận chứng khoán; không chèn ghi chú nội bộ vào bài làm. |
| **Tổng điểm (thang 10)** | **1.5/10** *(tạm tính)* | Chưa bao gồm tối đa 5.0 điểm của tiêu chí Đúng thông tin do thiếu dữ liệu gốc để kiểm chứng (điểm tối đa là **6.5/10** nếu thông tin giá vé và hoàn huỷ khớp hoàn toàn với ban tổ chức). | Cần viết lại toàn bộ nội dung phản hồi cho chuyên nghiệp, loại bỏ tuyên bố lợi nhuận quá đà, bổ sung câu hỏi thông tin đăng ký và kiểm tra lại số liệu chuẩn. |

Bạn vui lòng cung cấp bảng giá vé và chính sách huỷ vé chuẩn của ban tổ chức để tôi hoàn tất chấm điểm mục Đúng thông tin cho bài đánh giá này.```

**Link trò chuyện:**https://share.gemini.google/qyLaPopZRfhA
