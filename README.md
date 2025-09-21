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
