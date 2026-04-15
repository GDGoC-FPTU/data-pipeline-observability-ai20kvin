# Experiment Report: Data Quality Impact on AI Agent

**Student ID:** 2A202600405
**Name:** Nguyễn Thị Ngọc   
**Date:** 2026-04-15

---

## 1. Ket qua thi nghiem

Chay `agent_simulation.py` voi 2 bo du lieu va ghi lai ket qua:

| Scenario | Agent Response | Accuracy (1-10) | Notes |
|----------|----------------|-----------------|-------|
| Clean Data (`processed_data.csv`) | Based on my data, the best choice is Laptop at $1200 | 10 | Dữ liệu sạch, gợi ý đúng sản phẩm tốt nhất. |
| Garbage Data (`garbage_data.csv`) | Based on my data, the best choice is Nuclear Reactor at $999999 | 2 | Gợi ý sai do Outlier (giá cực lớn không thực tế). |

---

## 2. Phan tich & nhan xet

**Student ID:** 2A202600405
**Name:** Nguyễn Thị Ngọc   
**Date:** 2026-04-15

---

## 1. Ket qua thi nghiem

Chay `agent_simulation.py` voi 2 bo du lieu va ghi lai ket qua:

| Scenario | Agent Response | Accuracy (1-10) | Notes |
|----------|----------------|-----------------|-------|
| Clean Data (`processed_data.csv`) | Agent: Based on my data, the best choice is Laptop at $1200.0. | 10 | Dữ liệu sạch, gợi ý đúng sản phẩm tốt nhất. |
| Garbage Data (`garbage_data.csv`) | Agent: Based on my data, the best choice is Nuclear Reactor at $999999. | 2 | Gợi ý sai do Outlier (giá cực lớn không thực tế). |

---

## 2. Phan tich & nhan xet

### Tai sao Agent tra loi sai khi dung Garbage Data?

Agent trả lời sai khi dùng Garbage Data vì nó thiếu khả năng tự kiểm chứng chất lượng dữ liệu đầu vào. 

Các vấn đề chính bao gồm:
- **Outliers**: Sản phẩm "Nuclear Reactor" có giá $999,999 làm sai lệch thuật toán tìm sản phẩm tốt nhất (idxmax).
- **Duplicate IDs**: Gây nhầm lẫn thông tin giữa Laptop và Banana, làm mất tính toàn vẹn của dữ liệu.
- **Wrong Data Types**: Mặc dù trong trường hợp này Agent không crash nhưng nếu query vào "Broken Chair" với giá là chuỗi ký tự "ten dollars", Agent sẽ gặp lỗi tính toán (Agent Error).
- **Null values**: Khiến Agent không thể lọc được thông tin theo category hoặc trả về kết quả rỗng.

Dữ liệu rác "đầu độc" kiến thức của Agent, dẫn đến những câu trả lời vô lý hoặc sai lệch hoàn toàn so với thực tế.

---

## 3. Ket luan

**Quality Data > Quality Prompt?** Đồng ý.

Cho dù Prompt có hay đến đâu, nếu dữ liệu đầu vào (Knowledge Base) bị sai lệch hoặc không được làm sạch qua pipeline (như bước `validate` và `transform` trong `solution.py`), AI Agent sẽ luôn đưa ra kết quả không đáng tin cậy. Quy trình ETL và Data Observability là yếu tố then chốt để đảm bảo AI hoạt động chính xác. | | |

---

## 2. Phan tich & nhan xet

### Tai sao Agent tra loi sai khi dung Garbage Data?

(Viet nhan xet cua ban o day — it nhat 50 tu)

(Hay phan tich cac van de nhu Duplicate IDs, wrong data types, outliers, null values
va giai thich tai sao chung anh huong den ket qua cua Agent.)

---

## 3. Ket luan

**Quality Data > Quality Prompt?** (Dong y hay khong? Giai thich ngan gon.)

(Viet ket luan cua ban o day)