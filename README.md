# My Smart Home

## Giới thiệu

**My Smart Home** là một dự án ứng dụng **Internet of Things (IoT)** nhằm xây dựng một hệ thống nhà thông minh, cho phép người dùng giám sát và điều khiển các thiết bị trong nhà từ xa [1, 2]. Dự án này tập trung vào việc cải thiện chất lượng cuộc sống thông qua việc **giám sát môi trường sống**, **tăng cường an ninh** và **tiết kiệm năng lượng** [2-4]. Hệ thống sử dụng các cảm biến để thu thập dữ liệu về nhiệt độ, độ ẩm, ánh sáng, và phát hiện khí gas, lửa [5, 6]. Dữ liệu này được truyền tải và xử lý để người dùng có thể theo dõi và điều khiển các thiết bị thông qua một ứng dụng di động [7, 8].

## Các tính năng chính

*   **Giám sát môi trường**:
    *   Xem các thông số môi trường như nhiệt độ, độ ẩm, ánh sáng theo thời gian thực [9].
    *   Xem biểu đồ biến động môi trường trong một khoảng thời gian nhất định [9].
*   **Quản lý an ninh**:
    *   Quan sát khu vực sinh hoạt từ xa thông qua camera [9, 10].
    *   Nhận thông báo và cảnh báo nguy hiểm khi phát hiện sự cố [11, 12].
*   **Điều khiển từ xa**:
    *   Bật/tắt các thiết bị điện từ xa thông qua ứng dụng [11, 13].
    *   Tạo điều kiện tự động bật/tắt thiết bị dựa trên các ngưỡng cảm biến [11, 14].
    *   Lên lịch bật/tắt các thiết bị tự động [11, 15].
*   **Tích hợp AI**:
    *   Nhận diện khuôn mặt để tăng cường an ninh [16-19].
    *   Nhận diện giọng nói để điều khiển thiết bị [16, 18, 20, 21].

## Kiến trúc hệ thống

Hệ thống **My Smart Home** được xây dựng dựa trên 4 khối chức năng chính [22]:

1.  **Khối Things**: Bao gồm các thiết bị vật lý như cảm biến, relay, và vi điều khiển ESP32 [6, 23, 24].
2.  **Khối IoT Gateway**: Đóng vai trò cầu nối giữa các thiết bị và server, sử dụng giao thức MQTT để truyền dữ liệu [6, 7, 18, 25, 26]. Gateway được hiện thực bằng Python [18, 27].
3.  **Khối Server**: Quản lý, lưu trữ và xử lý dữ liệu từ các thiết bị, đồng thời đưa ra các lệnh điều khiển [6-8]. Sử dụng Adafruit IO để thu thập, xử lý và hiển thị dữ liệu [27-29].
4.  **Khối Ứng dụng**: Cung cấp giao diện cho người dùng cuối để giám sát và tương tác với hệ thống [6-8, 30]. Ứng dụng được phát triển cho nền tảng Android [27, 31].


## Công nghệ sử dụng

*   **Phần cứng**:
    *   Vi điều khiển **ESP32** [6, 24, 32].
    *   Cảm biến nhiệt độ, độ ẩm **DHT11** [5, 23, 33].
    *   Cảm biến ánh sáng [5, 23, 34].
    *   Cảm biến khí gas **MQ2** [5, 25, 35].
    *   Cảm biến lửa [6, 25, 36].
    *   Mạch ổn áp **LM2596** [6, 32, 37].
*   **Phần mềm**:
    *   Ngôn ngữ lập trình **Python** (cho IoT Gateway) [27, 28, 38].
        *   Thư viện **pyserial** [27, 28].
        *   Thư viện **Adafruit\_IO** [27, 28].
        *   Thư viện **asyncio** [16, 29].
        *   Thư viện **threading** [16, 29].
    *   Ngôn ngữ lập trình **Java** (cho ứng dụng Android) [27, 31].
        *   Thư viện **Paho MQTT Android** [27, 31].
        *   Thư viện **org.eclipse.paho.client.mqttv3** [27, 31].
    *   **Tensorflow** (cho nhận diện khuôn mặt) [16, 19].
    *   **Keras** (cho nhận diện khuôn mặt) [16, 19].
    *   **OpenCV** (cho nhận diện khuôn mặt) [16, 19].
    *   **Numpy** (cho nhận diện khuôn mặt) [16, 39].
    *   **Websockets** (cho nhận diện giọng nói) [16, 21].
*   **Giao thức**:
    *   **UART** (giao tiếp giữa Things và Gateway) [27, 40].
    *   **MQTT** (giao tiếp giữa Gateway, Server và Ứng dụng) [26, 27, 38].