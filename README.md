# Recommendation-Systems

## 1. Giới thiệu về hệ thống khuyến nghị - Recommendation systems

<p align="justify"> &nbsp;&nbsp;&nbsp;&nbsp; Hệ thống gợi ý (Recommender systems hoặc Recommendation systems, Recommender platform, Recommender engine) là một dạng của hệ hỗ trợ ra quyết định, cung cấp giải pháp mang tính cá nhân hóa mà không phải trải qua quá trình tìm kiếm phức tạp. Hệ thống gợi ý học từ người dùng và gợi ý các sản phẩm tốt nhất trong số các sản phẩm phù hợp. Recommender System (RS) là một lớp con của filtering system với ý tưởng là dự đoán “xếp hạng” hay “sở thích” của người dùng.
  </p>
<p align="justify"> &nbsp;&nbsp;&nbsp;&nbsp; <b>Ví dụ:</b>
  <ul align="justify">
    <li>Youtube tự động chuyển các clip liên quan đến clip bạn đang xem. Youtube cũng tự gợi ý những clip mà có thể bạn sẽ thích.</li>
    <li>Khi bạn mua một món hàng trên một trang web bán hàng online, hệ thống sẽ tự động gợi ý “Frequently bought together”, hoặc nó biết bạn có thể thích món hàng nào dựa trên lịch sử mua hàng của bạn.</li>
  </ul>
</p>
<p align="justify"> &nbsp;&nbsp;&nbsp;&nbsp; Vì tính hữu ích và được mệnh danh là cánh tay phải đắc lực trong vấn đề kinh doanh (đặc biệt là thương mại online ngày càng phát triển hiện nay) nên các nhà thương mại điện tử lớn như Amazon hoặc Netflix, Facebook. Cụ thể, đối với Amazon:
  <ul align="justify">
  <li>Dựa vào dữ liệu quá khứ của khách hàng như dữ liệu về điểm mà họ đã đánh giá trên từng sản phẩm, thời gian duyệt trên từng sản phẩm, số lần click vào sản phẩm,…để có thể nắm bắt được việc những mặt hàng nào mà khách hàng của họ yêu thích.</li>
  <li>Từ đó, Amazon có thể dự đoán được khách hàng có thể sẽ thích những sản phẩm nào khác và đưa ra gợi ý thích hợp.</li>
  </ul>
</p>

## 2. Các phương pháp thường dùng

### *2.1 Phương pháp lọc dựa trên nội dung (Content-based filter)* 
<p align="justify"> &nbsp;&nbsp;&nbsp;&nbsp; Phương pháp lọc dựa trên nội dung là một giải thuật nghiên cứu về lọc thông tin, phương pháp lọc dựa trên nội dung ước lượng hàm đánh giá R(u,i) của item i với user u được thiết lập dựa trên cơ sở đánh giá R(u,i’) của cùng user u cho item i’ mà trong đó i và i’ là tương tự nhau về mặt nội dung.
  </p>

### *2.2 Phương pháp lọc cộng tác (Collaboration filter)* 
<p align="justify"> &nbsp;&nbsp;&nbsp;&nbsp; Phương pháp lọc cộng tác là phương pháp tập hợp các đánh giá hoặc các quan điểm của khách hàng, nhận dạng sự tương đồng giữa các khách hàng trên cơ sở các đánh giá hoặc quan điểm của họ và phát sinh ra những tư vấn mới cho khách hàng.
  </p>
<p align="justify"> &nbsp;&nbsp;&nbsp;&nbsp; Bản chất của phương pháp này chính là hình thức tư vấn truyền miệng tự động. Trong phương pháp này, hệ thống sẽ so sánh, tính toán độ tương tự nhau giữa những người dùng hay sản phẩm, từ đó người dùng sẽ được tư vấn những thông tin, sản phẩm được ưa chuộng nhất bởi những người dùng có cùng thị hiếu. Trong phương pháp này, hệ thống thường xây dựng các ma trận đánh giá bởi người dùng lên các sản phẩm, bản tin, từ đó tính toán độ tương tự giữa họ.
  </p>
<p align="justify"> &nbsp;&nbsp;&nbsp;&nbsp; Các hệ tư vấn dựa trên lọc cộng tác không yêu cầu quá nặng vào việc tính toán, do đó nó có thể đưa ra những tư vấn có độ chính xác cao và nhanh chóng cho một số lượng lớn người dùng. Hơn nữa, hệ tư vấn này không yêu cầu mô tả nội dung tưởng mình mà chỉ sử dụng đánh giá của người dùng để ước lượng, do đó những hệ này có khả năng tư vấn phong phú và thường tạo ra những tư vấn bất ngờ cho người dùng.
  </p>
<p align="justify"> &nbsp;&nbsp;&nbsp;&nbsp; Phương pháp lọc cộng tác có các vấn đề như:
  <ul align="justify">
    <li>Sự thưa thớt</li>
    <li>Vấn đề sản phẩm mới</li>
    <li>Vấn đề khách hàng mới</li>
  </ul>
</p>

## 3. Thành phần của một hệ gợi ý

### *3.1 Dữ liệu*
<p align="justify"> &nbsp;&nbsp;&nbsp;&nbsp; Dữ liệu (thường là các dữ liệu về user, items, feedback): mà hệ thống quan tâm để lấy các dữ liệu xác định sở thích của đối tượng phục vụ cho việc dự đoán và đưa ra gợi ý. Trong đó:
  <ul align="justify">
    <li>users là danh sách người dùng</li>
    <li>items là danh sách sản phẩm, đối tượng của hệ thống. Ví dụ như các bài viết trên trang viblo, các video trên youtube,… Và mỗi item có thể kèm theo thông tin mô tả.</li>
    <li>feedback là lịch sử tương tác của user với mỗi item, có thể là đánh giá của mỗi user với một item, số ratings, hoặc comment, việc user click, view hoặc mua sản phẩm,…</li>
  </ul>
</p>

### *3.2 Ma trận user-item: Utility matrix*
<p align="center"> <img src ="https://user-images.githubusercontent.com/74041962/116260527-f6abeb00-a7a0-11eb-91bf-90c844761920.png"width="40%"/>
<p align="justify"> &nbsp;&nbsp;&nbsp;&nbsp; Đây là ma trận biểu diễn mức độ quan tâm (rating) của user với mỗi item. Ma trận này được xây dựng từ dữ liệu (1). Những ma trận này có rất nhiều các giá trị miss. Nhiệm vụ của Hệ gợi ý chính là dựa vào các ô đã có giá trị trong ma trận trên (dữ liệu thu được từ trong quá khứ), thông qua mô hình đã được xây dựng, dự đoán các ô còn trống (của user hiện hành), sau đó sắp xếp kết quả dự đoán (ví dụ, từ cao xuống thấp) và chọn ra Top-N items theo thứ tự rating giảm dần, từ đó gợi ý chúng cho người dùng.
 
### *3.3 Phương pháp*
<p align="justify"> &nbsp;&nbsp;&nbsp;&nbsp;Có 2 phương pháp gợi ý chính, thường được sử dụng để xây dựng hệ gợi ý, đó là:
  <ul align="justify">
    <li>Content-based Filtering: </li>
    <p align="justify"> &nbsp;&nbsp;&nbsp;&nbsp; Gợi ý các item dựa vào hồ sơ (profiles) của người dùng hoặc dựa vào nội dung/thuộc tính (attributes) của những item tương tự như item mà người dùng đã chọn trong quá khứ.
      <p align="center"> <img src ="https://user-images.githubusercontent.com/74041962/116261502-e8aa9a00-a7a1-11eb-858f-4baa8fa1b93b.png"width="50%"/>
    <li>Collaborative Filtering: </li>
    <p align="justify"> &nbsp;&nbsp;&nbsp;&nbsp; Gợi ý các items dựa trên sự tương quan (similarity) giữa các users và/hoặc items. Có thể hiểu rằng đây là cách gợi ý tới một user dựa trên những users có hành vi tương tự.
      <p align="center"> <img src ="https://user-images.githubusercontent.com/74041962/116261512-e9dbc700-a7a1-11eb-9371-6bb5687bf870.png"width="50%"/>
  </ul>
  
## Tài liệu tham khảo

&nbsp;&nbsp;&nbsp;&nbsp; 1. https://tailieu.vn/doc/luan-van-thac-si-ung-dung-he-thong-tu-van-recommender-systems-trong-linh-vuc-thuong-mai-dien-tu-1602259.html

&nbsp;&nbsp;&nbsp;&nbsp; 2.	https://itzone.com.vn/vi/article/tim-hieu-ve-content-based-filtering-phuong-phap-goi-y-dua-theo-noi-dung-phan-1/
