---
title: Vì sao chạy nhiều shop TikTok Shop cùng lúc lại bị khóa hàng loạt
slug: vi-sao-chay-nhieu-shop-tiktok-shop-cung-luc-lai-bi-khoa-hang-loat
date: 2026-10-30T05:48:45.000Z
updated: 2026-10-30T06:02:31.000Z
draft: false
feature_image: __GHOST_URL__/content/images/2026/10/collabstr-0Vk7HEjWLDE-unsplash--2--3.jpg
---

Shop không sập vì một đơn hàng lỗi. Nó sập cùng lúc với hai shop khác, vào khoảng 9 giờ sáng, không có email cảnh báo, và trong Seller Center dòng lý do chỉ ghi "vi phạm chính sách" hoặc để trống.

Điểm chung của những vụ khóa hàng loạt thường không nằm ở sản phẩm. Nó nằm ở chỗ các shop đó được vận hành từ cùng một chỗ, bởi cùng một người, trên cùng một thiết bị.

## **TikTok đối chiếu thứ gì khi bạn mở shop thứ hai**

Phần lớn người bán nghĩ rằng đổi IP là xong. IP chỉ là một trong bốn nhóm tín hiệu, và nó không phải nhóm khó xử lý nhất.

**Cookie và bộ nhớ trình duyệt.** TikTok gắn vào trình duyệt của bạn một loạt định danh: ttwid, msToken, s\_v\_web\_id, cộng thêm dữ liệu trong localStorage. Những giá trị này tồn tại độc lập với tài khoản bạn đang đăng nhập. Đăng xuất shop A rồi đăng nhập shop B trong cùng một cửa sổ Chrome, ttwid vẫn là một. Nó giống như đổi tên trên cùng một căn cước.

**Fingerprint thiết bị.** Canvas hash, chuỗi WebGL renderer, danh sách font, độ phân giải màn hình, múi giờ, ngôn ngữ, số lõi CPU. Trên một chiếc laptop, tổ hợp này gần như không đổi giữa các lần mở trình duyệt, kể cả chế độ ẩn danh. Nếu năm shop cùng cho ra một canvas hash và một chuỗi renderer giống hệt nhau, gần như chắc chắn chúng đang nằm trong cùng một cụm vận hành.

**Thông tin thanh toán và định danh.** Tên chủ tài khoản ngân hàng, số tài khoản, CCCD, số điện thoại, địa chỉ lấy hàng. Đây là nhóm tín hiệu mạnh nhất và cũng là nhóm người bán khó né nhất, vì nó xuất phát từ nhu cầu kinh doanh thật: một chủ doanh nghiệp mở ba shop thì đương nhiên dùng chung một pháp nhân và một tài khoản nhận tiền.

**Hành vi vận hành.** Giờ đăng nhập, nhịp xử lý đơn, ảnh sản phẩm bị nén lại từ cùng một file gốc, mẫu câu trả lời khách. Nhóm này yếu hơn ba nhóm trên nhưng lại là thứ hay bị bỏ qua nhất, vì nó không nằm trong cài đặt nào cả.

TikTok không công bố trọng số của từng tín hiệu. Cách các nhóm trên được mô tả ở đây là suy luận từ kiến trúc chung của hệ thống chống gian lận thương mại điện tử, không phải tài liệu chính thức của TikTok.

## **Ba kiểu vận hành hay làm sập cả cụm**

Kiểu phổ biến nhất: một chiếc máy, ba shop, chuyển qua lại bằng cách đăng xuất rồi đăng nhập. Người làm nghĩ mình đã tách vì mỗi lần chỉ có một tài khoản trên màn hình. Nhưng cookie ttwid không bị xóa khi đăng xuất, và fingerprint thì không đổi chút nào. Cách này chỉ tạo cảm giác an toàn, không tạo ra môi trường mới. Nó còn tệ hơn ở một điểm: ba shop có chung lịch sử đăng nhập trên cùng một máy, nên khi một shop bị gắn cờ, hai shop còn lại nằm sẵn trong cùng một cụm dữ liệu.

Kiểu thứ hai là dùng nhiều laptop nhưng chung một đường mạng. Router ở nhà hay ở kho phát ra một IP công cộng cho tất cả thiết bị. Bốn cái máy, một IP, một ASN. Người bán đã bỏ tiền mua thêm thiết bị mà vẫn ở trong cùng một nhóm.

Kiểu thứ ba xảy ra ở shop có nhân viên: một máy tính dùng chung cho ca sáng và ca tối, mỗi người đăng nhập một shop khác nhau. Đến lúc nghỉ việc, người sau vào ca bằng đúng profile đó.

Trong ba kiểu này, tôi sẽ xử lý kiểu thứ ba trước, vì nó là kiểu duy nhất mà người vận hành không nhìn thấy bằng mắt — không ai ngồi cạnh để biết người trước đã làm gì trên máy đó.

## **Kiểm tra trước khi mở shop tiếp theo**

Bốn bước dưới đây làm được trong khoảng hai mươi phút, và nên làm trước khi đăng ký shop mới chứ không phải sau khi bị khóa.

Mở hai cửa sổ trình duyệt khác nhau, lần lượt vào browserleaks.com/canvas và browserleaks.com/webgl. So sánh hai chuỗi hash. Nếu giống nhau, hai cửa sổ đó là một thiết bị dưới mắt nền tảng, và mọi thứ bạn làm trong đó sẽ được gộp.

Kiểm tra IP ở ipinfo.io. Cần xem cả IP lẫn ASN, không chỉ IP. Hai shop nằm trên hai dải mạng khác nhau của cùng một nhà cung cấp vẫn có thể bị coi là gần nhau nếu ASN trùng và IP thuộc cùng một khối /24.

Mở DevTools, vào Application, mục Cookies, tìm ttwid. Ghi lại giá trị này cho từng shop. Nếu hai shop cho ra cùng một ttwid, mọi thứ khác bạn làm đều vô nghĩa — đó là cùng một trình duyệt.

Về phía giấy tờ: mỗi shop đăng ký bằng CCCD cá nhân sẽ có giới hạn riêng, còn mở nhiều shop dưới một pháp nhân thì cần hồ sơ doanh nghiệp và tài khoản nhận tiền tương ứng. Phần này không phải mẹo kỹ thuật, nó là điều kiện để shop tồn tại về lâu dài. Dùng chung một tài khoản ngân hàng cho nhiều shop là cách nhanh nhất để hệ thống nối chúng lại với nhau, và cũng là chỗ hay bị yêu cầu giải trình nhất khi có tranh chấp.

Cuối cùng, ghi lại một bảng đơn giản: shop nào, profile nào, IP nào, ai vận hành, ngày bắt đầu. Khi có sự cố, bảng này là thứ duy nhất cho biết cái gì đã thay đổi.

## **Khi số lượng shop vượt quá số máy**

Ba đến năm shop thì tách bằng tay vẫn kiểm soát được: một cửa sổ Chrome riêng cho mỗi shop, một proxy riêng, một dòng trong bảng theo dõi. Từ mười shop trở lên, cách đó bắt đầu vỡ, và lúc này chỉ có vài hướng.

Mua thêm máy là hướng tốn tiền nhất, và nó không giải quyết được gì nếu tất cả vẫn cắm chung một router. Dựng máy ảo cho từng shop rẻ hơn, nhưng máy ảo trên cùng một host thường chia sẻ GPU và driver, nên canvas hash vẫn có thể trùng nhau — phải chạy lại đúng hai bước kiểm tra ở trên trước khi tin là đã tách.

Hướng còn lại là chạy nhiều profile trình duyệt độc lập trên một máy, mỗi profile giữ cookie, fingerprint và proxy riêng. Việc này tự làm được bằng cách mở Chrome với --user-data-dir khác nhau, chỉ có điều cách đó không đổi fingerprint và không gắn proxy theo từng profile. Một số team dùng công cụ có sẵn như ***Bitbrowser*** để khỏi tự dựng phần đó.

Với ba đến năm shop, đừng mua gì cả. Tách bằng tay, ghi bảng theo dõi, và chỉ tính đến công cụ khi số shop vượt quá số người có thể nhớ hết.

## **Những thứ không nằm trong môi trường trình duyệt**

Tách được môi trường không có nghĩa là shop sẽ sống. Một shop bán hàng vi phạm chính sách vẫn bị khóa, và nếu các shop chung pháp nhân hoặc chung chủ tài khoản, việc khóa có thể lan sang cả cụm.

Thứ mà một môi trường tách biệt trả lời được chỉ là câu hỏi "shop này có đang chạy cùng chỗ với shop kia không". Câu hỏi còn lại — sản phẩm có trùng nội dung với shop khác không, giá có đang phá nhau không, dòng tiền có đủ để chờ đối soát không — vẫn phải trả lời bằng tay.

Và nếu bạn đang vận hành nhiều shop chỉ để thử nghiệm danh mục, hãy thử trước ở quy mô hai shop với hai môi trường tách hẳn. Chi phí bỏ ra nhỏ, và nó cho biết ngay vấn đề của bạn nằm ở môi trường hay ở sản phẩm.
