# AI-Pacman-Project2
![alt](https://web.stanford.edu/class/archive/cs/cs221/cs221.1196/assignments/pacman/pacman_multi_agent.png)
1. Reflex Agent 
* Tính khoảng cách lặp đi lặp lại giữa thức ăn và vị trí pacman được thêm vào list
* Để pacman không gặp ma:
  Khoảng cách ma tối bằng 1 thì trả về một giá trị âm lớn để pacman không chọn hướng đó
Trả về score + nghịch đảo của giá trị nhỏ nhất trong list trên
2. Minimax
* Sử dụng đệ quy hàm miniMax:
   * Vòng for sẽ chạy cho đến khi return giá trị minimax
   * Mỗi lần chạy thì tại từng depth sẽ chạy hết các agent
   * Sau đó tăng depth lên đến self.depth 
   * Cứ như thế sẽ rẽ nhanh các node con 
   * Tiến hành đánh giá max và min để trả về kết quả
3. Alpha-Beta Pruning
* Sử dụng đệ quy hàm AB:
   * Vòng for sẽ chay cho đến khi return giá trị minimax
   * Mỗi lần chạy thì tại từng depth sẽ chạy hết các agent
   * Sau đó tăng depth lên đến self.depth 
   * Cứ như thế sẽ rẽ nhanh các node con 
   * Kiểm tra xem giá trị minMax có tốt hơn giá trị a,b không-->không cần kiểm tra các node tiếp theo
   * Tiến hành đánh giá max và min để trả về kết quả   
4.  Expectimax
* Sử dụng hàm đệ quy expectiMax
   *  Vòng for sẽ chay cho đến khi return giá trị minimax
   * Mỗi lần chạy thì tại từng depth sẽ chạy hết các agent
   * Sau đó tăng depth lên đến self.depth 
   * Cứ như thế sẽ rẽ nhanh các node con 
   * Có thêm tính xác suất 1 / tổng số hành động pháp lý 
   * Tiến hành đánh giá max, min và nodes cơ hội để trả về kết quả
