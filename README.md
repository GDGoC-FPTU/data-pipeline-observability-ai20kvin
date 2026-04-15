[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=23574043&assignment_repo_type=AssignmentRepo)
# Day 10 Lab: Data Pipeline & Data Observability

**Student Email:** 26ai.ngocnt@vinuni.edu.vn
**Name:** Nguyễn Thị Ngọc 
**Student ID** 2A202600405

---

## Mo ta

(Mo ta ngan gon bai lab va nhung gi ban da lam)
Bài Lab này thực hiện xây dựng một ETL Pipeline cơ bản để xử lý dữ liệu sản phẩm từ định dạng JSON sang CSV, bao gồm các bước: Trích xuất (Extract), Kiểm định (Validate), Biến đổi (Transform) và Lưu trữ (Load). Ngoài ra, bài Lab còn thực hiện Stress Test để đánh giá ảnh hưởng của chất lượng dữ liệu đối với AI Agent.
---

## Cach chay (How to Run)

### Prerequisites
```bash
pip install pandas
```

### Chay ETL Pipeline
```bash
python solution.py
```

### Chay Agent Simulation (Stress Test)
```bash
# Mo ta cach ban chay thi nghiem Clean vs Garbage data
```
1. Chạy `python generate_garbage.py` để tạo dữ liệu rác.
2. Chạy `python agent_simulation.py` để so sánh kết quả giữa Clean vs Garbage data.
---

## Cau truc thu muc

```
├── solution.py              # ETL Pipeline script
├── processed_data.csv       # Output cua pipeline
├── experiment_report.md     # Bao cao thi nghiem
└── README.md                # File nay
```

---

## Ket qua

(Tom tat ket qua: bao nhieu records da xu ly, bao nhieu bi loai, v.v.)
Đã xử lý 5 bản ghi từ `raw_data.json`, trong đó 3 bản ghi hợp lệ được đưa vào `processed_data.csv`. Pipeline chạy không lỗi và kết quả đã được chuẩn hóa.
