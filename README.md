# DATASET
Bộ dữ liệu dược thu thập từ Kaggle chứa dữ liệu theo dõi thể dục cá nhân từ các người dùng Fitbit.  
Tập dữ liệu **dailyActivity_merged.csv** gồm 940 hàng và 15 cột mô tả sức khỏe, thể hiện mức độ vận động, thời gian ở các trạng thái hoạt động khác nhau và năng lượng tiêu hao mỗi ngày.  
* Id: Mã định danh người dùng 
* ActivityDate: Ngày ghi nhận hoạt động
* TotalSteps: Tổng số bước đi trong ngày
* TotalDistance: Tổng quãng đường di chuyển 
* TrackerDistance: Quãng đường đo trực tiếp từ thiết bị.
* LoggedActivitiesDistance: Quãng đường được nhập thủ công bởi người dùng.
* VeryActiveDistance / ModeratelyActiveDistance / LightActiveDistance / SedentaryActiveDistance: Quãng đường di chuyển trong các mức độ hoạt động (rất năng động, trung bình, nhẹ, ít vận động)
* VeryActiveMinutes / FairlyActiveMinutes / LightlyActiveMinutes / SedentaryMinutes: Số phút ở các trạng thái hoạt động tương ứng
* Calories: Lượng calo đã đốt cháy trong ngày

  Tập dữ liệu **sleepDay_merged.csv** gồm 413 hàng và 5 cột mô tả thói quen ngủ của người dùng, cho biết họ ngủ bao lâu, nằm trên giường bao lâu và số lần ngủ/ngày.
* Id: Mã định danh người dùng 
* SleepDay: Ngày ghi nhận giấc ngủ 
* TotalSleepRecords: Số lần ngủ trong ngày 
* TotalMinutesAsleep: Tổng số phút ngủ 
* TotalTimeInBed: Tổng số phút nằm trên giường (bao gồm cả lúc chưa ngủ hoặc đã thức).

# Quá trình phân tích
* Quá trình làm sạch dữ liệu bao gồm: convert lại tên cột, ngày giờ, xử lý các giá trị null, trùng, ngoại lệ, tính tổng thời gian hoạt động trong ngày và thời gian bắt đầu vào giấc ngủ sau đó join 2 bảng theo id, sleepday và weekday.
* Phân tích 410 bản ghi dữ liệu Fitbit để xác định 60.9% người dùng có chất lượng giấc ngủ tốt bằng cách áp dụng tiêu chí y khoa (≤30 phút để ngủ, >85% thời gian ngủ hiệu quả) sau đó trực quan hóa dữ liệu bằng Python (matplotlib, seaborn) và power bi

# Kết luận 
* Người dùng có xu hướng ngủ muộn, dậy muộn; cuối tuần mất nhiều thời gian để vào giấc — có khả năng bị ảnh hưởng bởi thiết bị điện tử, caffeine/đồ uống kích thích, hoặc thay đổi lịch sinh hoạt.
* Chất lượng giấc ngủ tốt nhất rơi vào Thứ 4–Thứ 7; kém nhất Chủ Nhật –>Thứ 3 → phản ánh áp lực/lo lắng đầu tuần và thay đổi nhịp sinh học giữa tuần/cuối tuần.
* Hoạt động & ngủ: Giấc ngủ tốt liên quan tới nhiều hoạt động nhẹ trong ngày (lightly active) hơn là chỉ vận động mạnh. Ngược lại, nhóm có nhiều hoạt động fairly active/mạnh không đồng nghĩa ngủ tốt — có thể do phân bổ hoạt động chưa hợp lý hoặc gắng sức.
* Người có 1 giấc chính, hoặc 2 giấc/ngày có chất lượng tổng thể tốt hơn; ngủ 3 lần/ngày dễ dẫn đến ngủ quá nhiều, làm giảm chất lượng.
* Thứ Bảy hoạt động cao nhất; Chủ Nhật hoạt động thấp nhất — đây là thói quen tuần điển hình có thể tận dụng cho chiến dịch cuối tuần vs chuẩn bị cho tuần mới.

# Hành động
* Nhắc nhở giúp người dùng ngủ đúng giờ.
* Gợi ý các hoạt động vận động nhẹ nhàng (walk, yoga, stretching).
* Tận dụng insight thứ bảy hoạt động cao và chủ nhật hđ thấp gợi ý hoạt động thử thách cuối tuần
* Tạo app challenges người dùng sẽ nhận được huy hiệu nếu như hoàn thành challenges sau đó có thể chia sẻ thành tích lên mạng xã hội tạo động lực cho những người dùng khác
* Thu thập thêm dữ liệu như giới tính, tuổi tác hoặc nghề nghiệp để hiểu rõ hơn về người dùng
