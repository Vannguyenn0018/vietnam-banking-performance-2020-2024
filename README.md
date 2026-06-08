# Vietnam Banking Sector Analysis (2020 - 2024): Performance, Risk & Viability

![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)
![Pandas](https://img.shields.io/badge/Data_Manipulation-Pandas-150458.svg)
![Machine Learning](https://img.shields.io/badge/Machine_Learning-Scikit_Learn_|_XGBoost-orange.svg)
![BI](https://img.shields.io/badge/Dashboard-Power_BI_|_Tableau-yellow.svg)

## Bối cảnh & Bài toán kinh doanh (Business Context)
Dự án này được xây dựng nhằm đánh giá hiệu quả hoạt động và tiềm năng tăng trưởng của hệ thống Ngân hàng Thương mại tại Việt Nam trong giai đoạn **2020 - 2024**. Đây là một chu kỳ kinh tế đặc biệt, đánh dấu sự ảnh hưởng nặng nề của đại dịch COVID-19, những biến động vĩ mô phức tạp và quá trình phục hồi bứt tốc hậu đại dịch.

**Mục tiêu cốt lõi:**
1. Phân loại hệ thống ngân hàng theo các chỉ tiêu tài chính trọng yếu.
2. Nhận diện các ngân hàng có mô hình kinh doanh hiệu quả, tiềm năng tăng trưởng bền vững.
3. Cảnh báo sớm các ngân hàng đang đối mặt với rủi ro tài chính hoặc suy giảm chất lượng tài sản.

---

## 📂 Hệ sinh thái Dữ liệu (Data Ecosystem)
Dự án tận dụng hệ thống dữ liệu vi mô của các ngân hàng kết hợp cùng các chỉ báo kinh tế vĩ mô, bao gồm:
* **Micro-data (Báo cáo tài chính):** Balance Sheet (Bảng cân đối kế toán), Income Statement (Báo cáo KQKD), Notes (Thuyết minh BCTC).
* **Macro-data (Kinh tế vĩ mô):** Tăng trưởng GDP, Dòng vốn FDI, Tổng mức bán lẻ, Chỉ số PMI, Cung tiền M2, Tăng trưởng tín dụng và Tỷ giá (USD/VND, EUR/USD...).

---

## ⚙️ Luồng Phân tích & Cấu trúc Dự án (Thematic Analytical Workflow)
Dự án được chia thành 4 phân hệ nghiên cứu độc lập (Thematic Analysis), tương ứng với 4 tệp Jupyter Notebook. Dữ liệu thô được làm sạch tập trung qua một 파ipeline duy nhất trước khi đưa vào phân tích.

### 1. `banking_performance_landscape.ipynb` | Bức tranh Toàn cảnh & Khả năng sinh lời
* **Nhiệm vụ:** Phân tích xu hướng biến động của Tổng tài sản, Tăng trưởng tín dụng và Lợi nhuận. 
* **Key Metrics:** ROA, ROE, NIM.
* **Focus:** Đánh giá quỹ đạo phục hồi của các nhóm ngân hàng (Quốc doanh vs. Cổ phần) xuyên suốt các giai đoạn: Trước, Trong và Sau COVID-19.

### 2. `macroeconomic_impact_shift.ipynb` | Tác động Vĩ mô đến Thu nhập
* **Nhiệm vụ:** Lượng hóa mức độ nhạy cảm của hệ thống ngân hàng trước các cú sốc vĩ mô.
* **Phương pháp:** Phân tích tương quan (Correlation) và Hồi quy tuyến tính (OLS Regression).
* **Focus:** Giải mã cách tỷ giá biến động, chính sách tiền tệ (Cung tiền M2) và dòng vốn FDI định hình đà tăng trưởng thu nhập của từng nhóm ngân hàng.

### 3. `operational_efficiency_scale.ipynb` | Phân lớp Ngân hàng & Tối ưu Vận hành
* **Nhiệm vụ:** Phân cụm khách quan hệ thống ngân hàng và đánh giá hiệu suất vận hành.
* **Phương pháp:** Ứng dụng **PCA (Principal Component Analysis)** để giảm chiều dữ liệu tài chính, kết hợp thuật toán **K-Means Clustering** để gom cụm ngân hàng theo đặc điểm kinh doanh.
* **Focus:** Đánh giá Tỷ lệ chi phí trên thu nhập (CIR) và hiệu quả sử dụng vốn của từng cụm (ví dụ: Nhóm bán lẻ, Nhóm bán buôn, Nhóm quy mô lớn/nhỏ).

### 4. `credit_risk_viability.ipynb` | Đánh giá Rủi ro & Chất lượng Tài sản
* **Nhiệm vụ:** Nhận diện các nguyên nhân cốt lõi dẫn đến sự suy giảm chất lượng tài sản.
* **Phương pháp:** Xây dựng mô hình cây quyết định (Random Forest / XGBoost) để phân tích tầm quan trọng của các biến số (Feature Importance) tác động đến Nợ xấu.
* **Focus:** Phân tích Nợ xấu (NPL), Nợ nhóm 2, Nhóm 3 và chiến lược trích lập dự phòng (LLR) của các ngân hàng.

---

## 💡 Đề xuất Giải pháp (Strategic Recommendations)

Dựa trên các phát hiện từ dữ liệu (Data-driven Insights), dự án đề xuất các định hướng chiến lược sau:
1. **Chiến lược tối ưu hóa nguồn vốn & Sinh lời:** Cải thiện NIM thông qua việc cơ cấu lại tỷ trọng CASA và đa dạng hóa nguồn thu ngoài lãi (Non-interest income) cho cụm ngân hàng có quy mô vừa.
2. **Kiểm soát chi phí vận hành:** Đề xuất chiến lược chuyển đổi số sâu rộng cho nhóm ngân hàng có tỷ lệ CIR cao, tập trung vào tự động hóa quy trình (RPA) để giảm thiểu chi phí nhân sự.
3. **Quản trị rủi ro tín dụng:** Định hướng xây dựng các bộ đệm dự phòng (LLR) an toàn cho nhóm ngân hàng có mức độ nhạy cảm cao với biến động tỷ giá và có tỷ lệ nợ nhóm 2 đang phình to.
4. **Phân hóa chiến lược theo cụm:** * *Nhóm tăng trưởng nhanh:* Tiếp tục mở rộng thị phần tín dụng xanh, tiêu dùng.
   * *Nhóm rủi ro cao:* Tái cơ cấu danh mục cho vay, kiểm soát chặt dòng vốn vào các lĩnh vực nhạy cảm (Bất động sản).

---

##  Trực quan hóa Dữ liệu (Final Deliverable)
Toàn bộ dữ liệu sạch (Master Dataset) và các Insights cốt lõi nhất được hệ thống hóa trên Dashboard tương tác. 

---
