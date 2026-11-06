# Báo cáo cá nhân — Day 01: Lọc tin nhắn rác bằng ML, DL, Embedding và LLM

> Đổi tên file này thành `MSSV_HoTen.md` của bạn, ví dụ `2A20260000_NguyenVanAn.md`, rồi điền từng mục. Xoá các dòng hướng dẫn in nghiêng khi xong.

- **MSSV:2A202603718**
- **Họ và tên:Nguyễn Thế Hoàng**
- **SEED** (in ở ô đầu notebook):1864

## 1. Bằng chứng

| Tệp | Có? |
| --- | --- |
| [`day01_lab.ipynb`](day01_lab.ipynb) — notebook đã chạy, còn output | ☐ |
| [`lab1_report.json`](lab1_report.json) — do ô "Báo cáo cuối" sinh ra | ☐ |
| [`hand_calc.jpg`](hand_calc.jpg) — ảnh tính tay có các bước | ☐ |

## 2. Kết quả chính

                                 F1 test thường (SUB)  F1 50 case khó  \
1. BoW + LogReg                                0.919           0.286   
2. BoW + MLP                                   0.947           0.410   
3a. Emb + kNN                                  0.950           0.750   
3b. Emb + LogReg                               0.976           0.654   
3c. Emb + MLP head                             1.000           0.600   
4a. LLM nhỏ zero-shot                          0.000           0.000   
4d. LLM nhỏ + prompt phòng thủ                 0.000           0.000   

                                acc 50 case khó  
1. BoW + LogReg                            0.50  
2. BoW + MLP                               0.54  
3a. Emb + kNN                              0.72  
3b. Emb + LogReg                           0.64  
3c. Emb + MLP head                         0.60  
4a. LLM nhỏ zero-shot                      0.42  
4d. LLM nhỏ + prompt phòng thủ             0.42  

#T_1fe66_row0_col0, #T_1fe66_row0_col5, #T_1fe66_row0_col6, #T_1fe66_row1_col2, #T_1fe66_row4_col2, #T_1fe66_row4_col3, #T_1fe66_row4_col4, #T_1fe66_row5_col0, #T_1fe66_row5_col1, #T_1fe66_row5_col5, #T_1fe66_row5_col6, #T_1fe66_row6_col2, #T_1fe66_row6_col5, #T_1fe66_row6_col6 {
  background-color: #08306b;
  color: #f1f1f1;
}
#T_1fe66_row0_col1 {
  background-color: #084a91;
  color: #f1f1f1;
}
#T_1fe66_row0_col2, #T_1fe66_row0_col3, #T_1fe66_row0_col4 {
  background-color: #2e7ebc;
  color: #f1f1f1;
}
#T_1fe66_row1_col0 {
  background-color: #deebf7;
  color: #000000;
}
#T_1fe66_row1_col1, #T_1fe66_row1_col4, #T_1fe66_row5_col2 {
  background-color: #c6dbef;
  color: #000000;
}
#T_1fe66_row1_col3 {
  background-color: #9dcae1;
  color: #000000;
}
#T_1fe66_row1_col5, #T_1fe66_row1_col6, #T_1fe66_row2_col0, #T_1fe66_row2_col5, #T_1fe66_row2_col6, #T_1fe66_row3_col5, #T_1fe66_row3_col6 {
  background-color: #f7fbff;
  color: #000000;
}
#T_1fe66_row2_col1 {
  background-color: #e3eef9;
  color: #000000;
}
#T_1fe66_row2_col2, #T_1fe66_row2_col4 {
  background-color: #b7d4ea;
  color: #000000;
}
#T_1fe66_row2_col3 {
  background-color: #94c4df;
  color: #000000;
}
#T_1fe66_row3_col0, #T_1fe66_row3_col1, #T_1fe66_row4_col5, #T_1fe66_row4_col6 {
  background-color: #d6e6f4;
  color: #000000;
}
#T_1fe66_row3_col2, #T_1fe66_row3_col3, #T_1fe66_row3_col4, #T_1fe66_row4_col1, #T_1fe66_row6_col0, #T_1fe66_row6_col1, #T_1fe66_row6_col3, #T_1fe66_row6_col4 {
  background-color: #105ba4;
  color: #f1f1f1;
}
#T_1fe66_row4_col0 {
  background-color: #3787c0;
  color: #f1f1f1;
}
#T_1fe66_row5_col3, #T_1fe66_row5_col4, #T_1fe66_row7_col0 {
  background-color: #6aaed6;
  color: #f1f1f1;
}
#T_1fe66_row7_col1 {
  background-color: #5da5d1;
  color: #f1f1f1;
}
#T_1fe66_row7_col2 {
  background-color: #2979b9;
  color: #f1f1f1;
}
#T_1fe66_row7_col3 {
  background-color: #3e8ec4;
  color: #f1f1f1;
}
#T_1fe66_row7_col4 {
  background-color: #4a98c9;
  color: #f1f1f1;
}
#T_1fe66_row7_col5, #T_1fe66_row7_col6 {
  background-color: #8cc0dd;
  color: #000000;
}


  % đoán ĐÚNG theo nhóm case (càng đậm càng tốt)
  
    
       
      1. BoW + LogReg
      2. BoW + MLP
      3a. Emb + kNN
      3b. Emb + LogReg
      3c. Emb + MLP head
      4a. LLM nhỏ zero-shot
      4d. LLM nhỏ + prompt phòng thủ
    
  
  
    
      Tưởng spam nhưng không phải
      100%
      90%
      70%
      70%
      70%
      100%
      100%
    
    
      Thao túng / lừa đảo
      12%
      25%
      100%
      38%
      25%
      0%
      0%
    
    
      Spam giọng tự nhiên
      0%
      10%
      30%
      40%
      30%
      0%
      0%
    
    
      Né từ khoá
      17%
      17%
      83%
      83%
      83%
      0%
      0%
    
    
      Prompt injection
      67%
      83%
      100%
      100%
      100%
      17%
      17%
    
    
      Nói về spam
      100%
      100%
      25%
      50%
      50%
      100%
      100%
    
    
      Tin giao dịch hợp lệ
      83%
      83%
      100%
      83%
      83%
      100%
      100%
    
    
      TỔNG (50 case)
      50%
      54%
      72%
      64%
      60%
      42%
      42%
    
  



## 3. Dự đoán và thực tế

dự đoán mô hình llm nhỏ sẽ tệ hơn mô hình lớn và few_shot sẽ làm tốt hơn nhưng sai

## 4. Phân tích 50 case khó

BoW + LogReg  và BoW + MLP tụt nhiều nhất. Spam giọng tự nhiên lừa được nhiều nhất

## 5. Thử thách cá nhân

*Đề theo SEED của bạn, cách làm, kết quả, giải thích.*

## 6. Phương án cho sản phẩm thật

*Với yêu cầu p95 < 50 ms/tin cho 10 triệu SMS/ngày: chọn phương án nào, dẫn số liệu nào, chấp nhận đánh đổi gì.*

## 7. AI log và điều đã học

dùng AI để hiểu thêm về embedding và lý thuyết các mô hình và gợi ý về code 
