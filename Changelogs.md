## ☢ Change Logs - Version 1.1.0
 - ✅ Update thêm phần chọn GSM.
 - ✅ Fix lỗi hiển thị phần danh sách COM - bug không thể scroll để chọn COM.
 - ✅ Thêm tính năng xóa trong MenuContext.
 - ✅ Thêm tính năng xuất dữ liệu dạng txt.
 - ✅ Thêm tính năng xuất dữ liệu dạng Excel.
 - ✅ Update thay đổi proxy Tinsoft khi chạy tự động.
 - ✅ Thêm tính năng Login MyViettel để lấy thông tin thuê bao.
 - ✅ Thêm Local API: [ POST ] - http://localhost:11011/change-user-info-online
    ```sh
    const axios = require('axios');
    let data = JSON.stringify([
      {
        "phone": "356727530",
        // Cần phải truyền thêm thông số máy nếu trên Tool Viettel Utility chưa có dữ liệu
        "token": "4a08c973-198e-4995-a251-272e8a70689b-ODQzNzI0MjU1MDI=",
        "refreshToken": "0b1f0a01-efb7-43d8-90b6-c084e93a7ac6",
        "deviceId": "18a27c3c68f71b63",
        "deviceName": "Samsung S7",
        "macAddress": "21:3B:C3:41:BF:A9"
      }
    ]);
    
    let config = {
      method: 'POST',
      url: 'localhost:11011/change-user-info-online',
      headers: { 
        'Content-Type': 'application/json'
      },
      data : data
    };
    
    axios.request(config)
    .then((response) => {
      console.log(JSON.stringify(response.data));
    })
    .catch((error) => {
      console.log(error);
    });
    ```
    ```sh
    {
      "message": "Success",
      "success": true
    }
    ```
    **Free Software, Hell Yeah!**
