# Data_Visualization_DS105
ĐÁNH GIÁ CÁC YẾU TỐ CÁCH HƯỞNG ĐẾN RATING CỦA MỘT ĐẦU SÁCH.
-**Mô tả bài báo cáo :**
    - Đề tài của chúng tôi là Đánh giá các yếu tố ảnh hưởng đến rating của một đầu sách trên bộ dữ liệu tự thu thập từ trang Goodread.com  và từ đó xây dựng một mô hình dự đoán rating của người dùng với một đầu sách trên trang web này. Bộ dữ liệu có hơn 8000 đầu sách được thu thập từ list Best Books of the 21st Century: The best books published during the 21st century (January 1st, 2001 through December 31st, 2100).

- **Mô tả các file :**
    - **Báo cáo.docx** : File word báo cáo môn học. 
    -	**Crawl_books.ipynb** : File jupyternotebook để lấy dữ liệu từ trang web, sử dụng thư viện **BeautifulSoup**.
    -	**Data_clean.csv** : File lưu giữ thông tin của từng cuốn sách 
    -	**DS105_Preprocessing.ipynb** : File xử lý dữ liệu ban đầu thành dữ liệu hoàn chỉnh, xử lý null, rút trích thông tin, chuẩn hóa dữ liệu , sử dụng các thứ viện như : **matplotlib.pyplot**,**scipy.stats**,**numpy**,**pandas**.
    -	**DS105_EDA.ipynb** : File EDA dữ liệu để chọn ra các thuộc tính phục vụ cho model, ở file này sẽ có chi tiết quá tình trức quan hóa dữ liệu sử dụng các thư viện như : **seaborn**,**xgboost**,**display**,...
    -	**DS105_Model.ipynb** : File xây dựng các mô hình dự đoán rating từ những thuộc tính tìm được từ quá trình EDA.

- ** Kết luận :**
    -Trong đồ án này, nhóm chúng tôi đã sử dụng thư viện BeautifulSoup của Python thu thập được bộ dữ liệu thô chứa các thông tin về các đầu sách trên Goodreads.com. Khi đã có bộ dữ liệu thô nhóm chúng tôi tiếp tục tiền xử lý và chuẩn hóa lại dữ liệu, quá trình chuẩn hóa này bao gồm cả chuẩn hóa tự động và thực hiện chuẩn hóa thủ công một thuộc tính có độ phức tạp cao. Sau khi có được bộ dữ liệu hoàn thiện, nhóm đã tiến hành phân tích và tìm được 3 thuộc tính quan trọng là genre, description và awards. 
Nhóm chúng tôi sử dụng module Pickle chuyển các thuộc tính phân loại thành kiểu thuộc tính số để xây dựng được 3 mô hình dự đoán rating dựa vào 9 thuộc tính trong đó bao gồm 3 thuộc tính insights đã tìm được trước đó. Tuy nhiên, mô hình xây dựng có độ chính không được cao vì các nguyên nhân: trong thực người đọc có xu hướng đánh giá cuốn sách dựa vào nội dung của nó, vì vậy việc huấn luyện mô hình dự đoán rating trên các biến thông tin là không khả quan; thứ hai là nguồn dữ liệu thu thập từ trang Goodreads có một số hạn chế, như việc thuộc tính genre (thể loại) không phải hoàn toàn chính xác vì thể loại của sách được quyết định bằng cách thu thập dữ liệu người dùng, bên cạnh đó các thuộc tính rating_count và review_count cần thời gian để có một lượng người dùng đánh giá và bình luận, điều này khiến việc dự đoán rating các cuốn sách mới, sách bị khuyết 2 thuộc tính này trở nên khó khăn, làm giảm hiệu suất của mô hình.

