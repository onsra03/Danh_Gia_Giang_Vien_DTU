# Auto Điền Đánh Giá Giảng Viên Đại Học Duy Tân

## Giới Thiệu:
Repo này hướng dẫn cách tự động điền đánh giá giảng viên tại Đại học Duy Tân. Tiết kiệm thời gian cho những người lười ví dụ như mình :)))

## Hướng Dẫn Sử Dụng:
#### Bước 1: Vào môn học cần đánh giá giảng viên:
![image](https://github.com/onsra03/Danh_Gia_Giang_Vien_DTU/assets/85748567/ee6dff0c-7406-4078-9af8-d70e4e63bf5f)


#### Bước 2:
Copy đoạn code sau:
```js
function autoInput() {
    const textareaIds = ['R48', 'R49', 'R50', 'R51', 'R52'];

    textareaIds.forEach(textareaId => {
        const textarea = document.getElementById(textareaId);

        if (textarea) {
            textarea.value = 'Không có';
        }
    });
}

function autoChoose() {
    for (let sectionIndex = 0; sectionIndex < 49; sectionIndex++) {
        const radioButtonId = `R${sectionIndex}A`;

        const radioButton = document.getElementById(radioButtonId);
        if (radioButton) {
            radioButton.click();
        }
    }
}
autoInput();
autoChoose();
```
#### Bước 3:
Tại trang đánh giá nhấn phím F12 (hoặc chuột phải chọn `Inspect`) sẽ thấy xuất hiện DevTools, sau đó chọn qua tab Console:
![image](https://github.com/onsra03/Danh_Gia_Giang_Vien_DTU/assets/85748567/ee01d507-4b63-4c40-b68a-62b89ea59012)

#### Bước 4:
Dán đoạn code trên xuống console, sau đó nhấn Enter:
![image](https://github.com/onsra03/Danh_Gia_Giang_Vien_DTU/assets/85748567/8adf9f31-12ca-472d-829e-27a8be44bc5f)
![image](https://github.com/onsra03/Danh_Gia_Giang_Vien_DTU/assets/85748567/0564f47e-e41e-4ac7-aff4-b99edfcecd5e)


Cuối cùng thì chỉ cần điền CAPTCHA mã xác nhận rồi gửi thôi :v 

## Thay đổi đánh giá:
Đoạn code trên mình auto đánh giá `Tốt` và ý kiến `Không có`, nếu bạn nào muốn sửa đổi thì theo cách sau:
```
const radioButtonId = `R${sectionIndex}A`;
```
->
```
const radioButtonId = `R${sectionIndex}B`;
```
Đổi chữ A thành các ký tự B,C,.., tương đương với chọn dòng 2 hoặc 3,...
```
1. Tốt
2. Khá
3. Trung bình
4. Trung bình Yếu
5. Yếu
6. Kém
```
Đối với các ô ý kiến, các bạn thay đổi dòng theo nội dung các bạn muốn:
```
textarea.value = 'Không có';
```
