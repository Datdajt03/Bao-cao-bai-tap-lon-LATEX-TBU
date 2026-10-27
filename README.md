# Mẫu Báo Cáo LaTeX — Trường Đại Học Tây Bắc (UTB)

Mẫu (template) báo cáo bài tập lớn, bài tập nhỏ, tiểu luận và đồ án môn học bằng LaTeX chuẩn định dạng dành riêng cho sinh viên **[Trường Đại học Tây Bắc](https://utb.edu.vn/)**.

- **Tác giả:** Lò Mạnh Đạt  
- **Website trường:** [https://utb.edu.vn/](https://utb.edu.vn/)  
- **Định dạng:** Căn lề chuẩn văn bản học thuật (Trái 3.0cm, Phải 1.5cm, Trên 2.0cm, Dưới 2.0cm), tự động tạo trang bìa, mục lục và danh sách thành viên 2 cột.

---

## 📁 Cấu Trúc Thư Mục

```text
├── main.tex                 # File chính điều khiển toàn bộ cấu hình báo cáo
├── tbu_report.sty           # Gói định dạng phong cách chuẩn Đại học Tây Bắc
├── tbu_logo.png             # Logo trường ĐH Tây Bắc dùng cho trang bìa
├── Gioithieu_danhmuc/       # Chứa các file mở đầu: lời cảm ơn, từ viết tắt, phân công
│   ├── loicamon.tex
│   ├── phancong.tex
│   └── tuviettat.tex
├── Noidungbaocao/           # Chứa nội dung chính các chương
│   ├── modau.tex
│   ├── chuong1.tex
│   ├── chuong2.tex
│   ├── chuong3.tex
│   └── ketluan.tex
└── tailieuthamkhao.bib      # File chứa danh mục tài liệu tham khảo
```

---

## ⚙️ 1. Hướng Dẫn Sửa Thông Tin Báo Cáo

Tất cả thông tin chung của bài báo cáo đều được chỉnh sửa tại phần đầu của file **`main.tex`** (từ dòng 7 đến 26):

```latex
\ministry{BỘ GIÁO DỤC VÀ ĐÀO TẠO}
\university{TRƯỜNG ĐẠI HỌC TÂY BẮC}
\faculty{KHOA CÔNG NGHỆ THÔNG TIN}
\reporttype{BÁO CÁO BÀI TẬP LỚN}   % Đổi thành: BÀI TẬP NHỎ / ĐỒ ÁN / TIỂU LUẬN
\title{TÊN ĐỀ TÀI CỦA BẠN}         % Tên đề tài bài tập
\courseclass{K64 ĐẠI HỌC CNTT}     % Lớp học phần / Niên khóa
\groupnumber{Nhóm 3}               % Nhóm thực hiện
\advisor{TS. Phạm Quốc Thắng}      % Tên giảng viên hướng dẫn
\location{SƠN LA}                  % Địa điểm
\reportdate{THÁNG 05/2026}         % Thời gian nộp

% Danh sách thành viên (tự động chia 2 cột đẹp mắt)
\addstudent[NT]{\textbf{Lò Mạnh Đạt}}  % [NT] là nhóm trưởng
\addstudent{Nguyễn Văn A}
\addstudent{Trần Thị B}
```

> **Sửa nội dung bài viết:** Bạn chỉ cần vào thư mục `Noidungbaocao/` và mở các file `modau.tex`, `chuong1.tex`, `chuong2.tex`, `ketluan.tex` để gõ nội dung.

---

## ➕ 2. Hướng Dẫn Thêm Một File / Chương Mới

Khi muốn bổ sung thêm chương mới hoặc mục mới, bạn chỉ cần thực hiện 2 bước đơn giản:

### Bước 1: Tạo file `.tex` mới
Tạo một file mới trong thư mục `Noidungbaocao/` (ví dụ đặt tên là `chuong4.tex`) với nội dung như sau:

```latex
\chapter{TÊN CHƯƠNG MỚI}

\section{Tiêu đề mục con}
Nội dung của chương mới viết ở đây...
```

### Bước 2: Nối file vào `main.tex` bằng lệnh `\input`
Mở file **`main.tex`**, tìm đến phần `5. NỘI DUNG CHÍNH CỦA BÁO CÁO` và thêm dòng `\input{...}` vào vị trí bạn muốn hiển thị:

```latex
\input{Noidungbaocao/modau.tex}
\input{Noidungbaocao/chuong1.tex}
\input{Noidungbaocao/chuong2.tex}
\input{Noidungbaocao/chuong3.tex}
\input{Noidungbaocao/chuong4.tex}   % <-- THÊM DÒNG NÀY ĐỂ GỌI CHƯƠNG MỚI
\input{Noidungbaocao/ketluan.tex}
```

---

## 🔨 3. Cách Biên Dịch (Compile)

- Mở dự án bằng **TeXstudio**, **VS Code** (cài extension *LaTeX Workshop*) hoặc nén zip tải lên **Overleaf**.
- Chọn file chính là **`main.tex`**.
- Biên dịch bằng **pdfLaTeX** hoặc **XeLaTeX** để xuất ra file PDF hoàn chỉnh.

---

*Người tạo mẫu: **Lò Mạnh Đạt** — [Trường Đại học Tây Bắc](https://utb.edu.vn/)*
