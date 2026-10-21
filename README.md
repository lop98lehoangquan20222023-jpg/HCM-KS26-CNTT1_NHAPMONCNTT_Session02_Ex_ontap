
## PHẦN 1:

### 1. Lựa chọn ứng viên kỹ thuật
* **Lựa chọn:** **Ứng viên B** (Lĩnh vực Mạng máy tính / Quản trị hệ thống).
* **Giải thích:** Nhu cầu cốt lõi và cấp thiết nhất của Cyber Arena là duy trì hệ thống máy chơi game hoạt động ổn định, xử lý các sự cố về phần cứng, cấu hình mạng nội bộ mượt mà và tối ưu đường truyền livestream.
### 2. Sắp xếp đơn vị lưu trữ theo thứ tự tăng dần
* **Thứ tự đúng:** **Byte < KB < MB < GB < TB**


## PHẦN 2: MÔ HÌNH IPO VÀ LĨNH VỰC CNTT

### 1. Mô hình IPO cho hệ thống quay và xem lại trận đấu

| Thành phần | Trong hệ thống quay/xem lại trận đấu |
| :--- | :--- |
| **Input** | tín hiệu game ,camera,micro |
| **Process** | CPU và GPU xử lý mã hóa thông tin từ cam và micro |
| **Output** | luồng video livestream phát trực tiếp lên YouTube hoặc hiển thị trên màn hình xem lại |
| **Storage** | Ổ cứng SSD/HDD dùng để lưu trữ lâu dài các file video trận đấu đã xuất |

### 2. Các lĩnh vực CNTT liên quan
1. **Mạng máy tính & Truyền thông (Computer Networking):** Đảm bảo hạ tầng mạng kết nối ổn định, băng thông đủ lớn để tải dữ liệu livestream video chất lượng cao lên nền tảng YouTube không bị gián đoạn.
2. **Quản trị Hệ thống & Phần cứng (System Administration):** Chịu trách nhiệm tối ưu hóa cấu hình phần cứng máy tính và vận hành các phần mềm ghi hình/livestream (như OBS Studio) hoạt động mượt mà.


## PHẦN 3:

### 1. Tính dung lượng lưu trữ
Dung lượng (1 tháng): $20 \text{ trận} \times 500 \text{ MB} = 10.000 \text{ MB} \approx 9,77 \text{ GB}$.SSD 512 GB chứa thoải mái (trống $502,23 \text{ GB}$).Tốc độ mạng: $100 \text{ Mbps} = 12,5 \text{ MB/s}$.Upload video 200 MB: tối thiểu 16 giây.Thực tế lâu hơn do: trễ mạng (latency), sụt giảm băng thông ISP hoặc giới hạn từ YouTube.
 

### 2. Tính tốc độ mạng
* **Chuyển đổi tốc độ:**
  $$\text{Tốc độ truyền tải} = 100 \text{ Mbps} \div 8 = 12,5 \text{ MB/s}$$
* **Thời gian tải lên (upload) tối thiểu cho video 200 MB:**
  $$\text{Thời gian} = 200 \text{ MB} \div 12,5 \text{ MB/s} = 16 \text{ giây}$$
* **Vì sao thực tế thường lâu hơn con số tính toán?**
  * Do độ trễ mạng , sự dao động băng thông, nghẽn mạng nội bộ hoặc giới hạn tốc độ nhận dữ liệu từ phía máy chủ tiếp nhận.

---

## PHẦN 4: PHẦN CỨNG VÀ MÔ HÌNH DIKW

### 1. Giải quyết vấn đề giật lag khi chơi game kết hợp livestream
* **Lựa chọn nâng cấp:** **Nâng cấp CPU**.
* **Giải thích:** CPU đóng vai trò xử lý toàn bộ logic của game đồng thời gánh thêm nhiệm vụ mã hóa luồng video livestream trong thời gian thực. Dung lượng RAM 16 GB hiện tại đã đủ dùng; việc giật lag xảy ra do CPU bị quá tải khi xử lý đa nhiệm nặng.

### 2. Áp dụng mô hình DIKW vào tình huống thực tế

| Tầng | Nội dung trong tình huống | Vì sao thuộc tầng này? |
| :--- | :--- | :--- |
| **Data** | Các đoạn video quay lại trận đấu | Là dữ liệu thô chưa qua phân tích, xử lý hay gán ngữ cảnh. |
| **Information** | Tuyển thủ hay bị gục ở phút 15 đến 20 | Dữ liệu thô đã được tổng hợp, sắp xếp và phân tích theo chuỗi thời gian. |
| **Knowledge** | Nguyên nhân dẫn đến bị hạ gục là do thiếu tầm nhìn bản đồ | Đã kết nối thông tin với ngữ cảnh chuyên môn để hiểu rõ bản chất vấn đề. |
| **Wisdom** | HLV yêu cầu mua thêm mắt (Ward) cho trận đấu tiếp theo | Vận dụng hiểu biết để đưa ra quyết định hành động thực tế nhằm cải thiện kết quả. |