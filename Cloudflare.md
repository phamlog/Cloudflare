![](https://cdn.hashnode.com/uploads/covers/67b5e145f6ce52ab1df147c6/2cf6fa03-1377-4160-b4a2-80258c380c73.jpg align="center")

## TỔNG QUAN

Cloudflare là một công ty bảo mật được thành lập vào tháng 7 năm 2009. Họ cung cấp CDN, WAF, DNS/ Email security, phòng chống tấn công DDoS và SASE cho các doanh nghiệp, tổ chức phi lợi nhuận, nhà phát triển và người tiêu dùng. Trụ sở chính của họ ở San Francisco, California, Bắc Mỹ, với khoảng hơn 3000 nhân viên. Cloudflare có mạng lưới toàn cầu của riêng họ, có thể truy cập trên 300 thành phố ở hơn 100 quốc gia trên toàn thế giới, bao gồm cả những khu vực khó tiếp cận như Trung Quốc. Hơn 12.500 mạng đã kết nối với Cloudflare với tổng dung lượng lên tới hơn 209Tbps, mang đến khả năng truy cập các trung tâm dữ liệu đặt tại Châu Âu, Bắc Mỹ, Trung Quốc đại lục, Châu Mỹ Latinh, Châu Đại Dương, Châu Á, Châu Phi và Caribê. Cloudflare cung cấp dịch vụ cho mọi loại hình tổ chức/ doanh nghiệp như thương mại điện tử, hành chính công, SaaS, dịch vụ tài chính, chăm sóc sức khỏe, trò chơi, giáo dục, truyền thông và giải trí.

Ngày nay, các mối đe dọa bảo mật ứng dụng ngày càng gia tăng. Năm 2020, National Vulnerability Database (NVD) ghi nhận hơn 18.000 lỗ hổng, trong đó hơn 10.000 ở mức nghiêm trọng hoặc cao. Đáng chú ý, nhiều lỗ hổng bị khai thác là lỗ hổng đã biết và đã có bản vá, nhưng doanh nghiệp vẫn chậm xử lý (trung bình mất 16 ngày để vá).

Ngoài ra, rủi ro không chỉ đến từ lỗ hổng phần mềm mà còn từ:

*   API (chiếm hơn 50% lưu lượng truy cập)
    
*   Bot (chiếm khoảng 40% Internet traffic)
    
*   Mã bên thứ ba (tiềm ẩn tấn công chuỗi cung ứng)
    

→ Tổng thể, việc chậm vá lỗi và phụ thuộc vào hệ thống bên ngoài khiến ứng dụng dễ bị tấn công hơn.

**Các chủ sở hữu ứng dụng hiện nay phải đối mặt với 6 mối quan tâm bảo mật cấp bách nhất:**

1.  **Lỗ hổng ứng dụng:** Những kẻ tấn công liên tục khai thác các lỗ hổng zero-day hoặc các lỗ hổng đã biết nhưng chưa được vá. Thực tế, 83% ứng dụng có ít nhất một lỗi bảo mật, khiến hệ thống rất dễ bị xâm nhập.
    
2.  **Tấn công API:** Khi API chiếm hơn 50% lưu lượng truy cập mạng, việc lạm dụng API đang trở thành nguyên nhân hàng đầu dẫn đến vi phạm dữ liệu cho các ứng dụng web.
    
3.  **Tấn công Botnet:** Bot chiếm tới 40% lưu lượng Internet. Kẻ xấu sử dụng mạng thiết bị bị chiếm quyền điều khiển (botnet) để thực hiện các hành vi như nhồi nhét thông tin xác thực (chiếm đoạt tài khoản) hoặc cào dữ liệu trái phép.
    
4.  **Tấn công chuỗi cung ứng:** Kẻ tấn công không đánh trực tiếp vào máy chủ mà lây nhiễm mã độc qua các nguồn bên thứ ba (như tập lệnh JavaScript tích hợp trên trang). Ví dụ điển hình là các vụ tấn công Magecart chặn thu thập thông tin thẻ tín dụng của người dùng cuối.
    
5.  **Tấn công DDoS:** Kẻ tấn công sử dụng luồng lưu lượng rác khổng lồ nhằm làm quá tải và đánh sập ứng dụng. Đáng chú ý, Việt Nam là một trong những nguồn phát sinh tấn công DDoS Layer 3/4 lớn nhất toàn cầu.
    
6.  **Tấn công trên đường đi (On-path attacks):** Còn gọi là tấn công trung gian, trong đó kẻ xấu chặn liên lạc giữa trình duyệt và máy chủ (như chiếm quyền điều khiển DNS hoặc email) để mạo danh và đánh cắp thông tin nhạy cảm.
    

Cloudflare giải quyết 6 vấn đề này bằng cách triển khai mọi lớp phòng thủ trực tiếp trên một nền tảng mạng biên đám mây (Cloud Edge Network) toàn cầu. Cụ thể như sau:

1.  **Lỗ hổng ứng dụng:** Tường lửa WAF sử dụng các bộ quy tắc OWASP và quy tắc được quản lý (Managed Rules) để "vá ảo" lỗ hổng, tự động chặn các payload tấn công đã biết.
    
2.  **Tấn công API:** API Shield áp dụng mô hình bảo mật tích cực bằng cách xác thực lược đồ (schema validation), lập tức chặn mọi request không tuân thủ chính xác cấu trúc API dự kiến.
    
3.  **Tấn công Botnet:** Bot Management dùng Máy học (Machine Learning) để gán điểm rủi ro (Bot Score) cho từng request, giúp phân biệt và chặn đứng các bot xấu mà không làm phiền người dùng thật.
    
4.  **Tấn công chuỗi cung ứng:** Page Shield hoạt động ở phía máy khách để giám sát các tập lệnh bên thứ 3 (như JavaScript), cảnh báo và ngăn chặn ngay nếu phát hiện mã bị sửa đổi để thu thập dữ liệu trái phép.
    
5.  **Tấn công DDoS và Quá tải hệ thống:** Hệ thống DDoS tự trị luôn bật sẽ phân tích và chặn các luồng dữ liệu rác khổng lồ ngay tại biên mạng chỉ trong dưới 3 giây. Song song đó, **Cân bằng tải (Load Balancing)** sẽ chịu trách nhiệm phân phối thông minh lượng truy cập hợp lệ (hoặc các đợt tăng vọt traffic đột ngột) rải đều qua nhiều máy chủ khác nhau, tối đa hóa hiệu suất và đảm bảo ứng dụng luôn sẵn sàng hoạt động (availability).
    
6.  **Tấn công trên đường đi:** Ngăn chặn việc đánh cắp dữ liệu bằng cách ép buộc mã hóa toàn bộ kết nối thông qua SSL/TLS và HSTS.
    

Sau đây, ta sẽ tìm hiểu về giải pháp bảo mật của Cloudflare theo 4 nhóm:

*   **SASE & Workspace Security:** Bảo mật truy cập và không gian làm việc hiện đại theo mô hình Zero Trust
    
*   **Application Security:** Bảo vệ ứng dụng toàn diện trước các mối đe dọa và tấn công mạng
    
*   **Application Performance:** Tối ưu hiệu suất và khả năng phân phối ứng dụng
    
*   **Networking:** Xây dựng hạ tầng mạng an toàn, linh hoạt và hiệu quả
    

## **SASE & Workspace Security**

### **Zero Trust (ZTNA)**

**Mô hình:** Thay thế VPN truyền thống bằng cách không còn tin tưởng mặc định bất kỳ ai trong mạng.

**Cách hoạt động :**  
Khi nhân viên muốn truy cập hệ thống nội bộ, họ **không được vào toàn bộ mạng** như VPN. Thay vào đó:

*   Hệ thống sẽ **xác minh danh tính** (tài khoản, MFA, thiết bị…)
    
*   Sau khi xác thực, người dùng chỉ được **truy cập đúng 1 ứng dụng cụ thể** (ví dụ: hệ thống HR, CRM…)
    
*   Không thể “đi lan” sang các tài nguyên khác trong mạng
    
*   **Cơ chế bảo mật phía server:**
    
    *   Máy chủ nội bộ cài **Cloudflare Tunnel**
        
    *   Máy chủ **chủ động kết nối ra ngoài (outbound)** tới Cloudflare
        
    *   Không cần mở port → server gần như **ẩn hoàn toàn trên Internet**
        

> **Cloudflare Tunnel** là một cơ chế giúp **kết nối an toàn từ hệ thống nội bộ ra Internet mà không cần mở cổng (port)**.
> 
> Hiểu đơn giản
> 
> Thay vì:
> 
> *   Mở port (80, 443…) trên server → dễ bị scan, tấn công
>     
> 
> Cloudflare Tunnel sẽ:
> 
> *   Cho server **chủ động kết nối ra Cloudflare (outbound)**
>     
> *   Người dùng truy cập → đi qua Cloudflare → được chuyển vào server qua “đường hầm” này
>     
> 
> Server **không lộ IP, không cần public ra Internet**

**Với VPN truyền thống:** Khi kết nối thành công, nhân viên này giống như được cấp "chìa khóa vạn năng" để đi vào toàn bộ mạng nội bộ. Nếu máy tính của họ vô tình bị nhiễm mã độc, mã độc đó có thể tự do quét và lây lan sang các hệ thống khác (như máy chủ nhân sự hay kho mã nguồn). Hơn nữa, VPN buộc mọi luồng dữ liệu phải đi đường vòng về một thiết bị trung tâm (choke point), tạo ra điểm nghẽn và làm kết nối rất chậm.

**Với Cloudflare ZTNA:** Hệ thống chỉ cấp quyền cho nhân viên đó vào **duy nhất ứng dụng thanh toán** (đặc quyền tối thiểu). Họ hoàn toàn không thể nhìn thấy hay chạm vào các hệ thống khác trong mạng. Đồng thời, thay vì mở cổng mạng công khai chờ kết nối, máy chủ sử dụng đường hầm (Cloudflare Tunnel) để kết nối ngược ra ngoài, giúp máy chủ hoàn toàn "tàng hình" trước các tin tặc trên Internet. Việc xác thực cũng được thực hiện ngay tại máy chủ biên gần người dùng nhất thay vì kéo về trung tâm, mang lại tốc độ truy cập cực nhanh

### **Secure Web Gateway – SWG**

**Mô hình:** Trạm kiểm soát lưu lượng **đi ra Internet (outbound)** của người dùng.

**Cách hoạt động (giải thích dễ hiểu):**  
Khi nhân viên truy cập web hoặc SaaS:

*   Toàn bộ lưu lượng (DNS, HTTP/HTTPS) sẽ **đi qua SWG trước**
    
*   SWG sẽ **kiểm tra và lọc** nội dung theo chính sách bảo mật
    
*   Chỉ những truy cập an toàn mới được phép đi tiếp ra Internet
    

**Những gì SWG làm:**

*   Chặn website độc hại, chứa malware
    
*   Ngăn chặn phishing (trang giả mạo)
    
*   Kiểm soát tải lên/xuống để tránh rò rỉ dữ liệu
    
*   Áp dụng policy (ví dụ: cấm truy cập web không liên quan công việc)
    

### **Network-as-a-Service / SD-WAN (Cloudflare WAN)**

**Mô hình:** Thay thế mạng WAN truyền thống bằng hạ tầng mạng **cloud hiện đại, linh hoạt**.

**Cách hoạt động (giải thích dễ hiểu):**  
Thay vì kết nối các chi nhánh bằng MPLS hoặc VPN phức tạp:

*   Các văn phòng, data center, cloud **kết nối trực tiếp vào mạng của Cloudflare**
    
*   Cloudflare trở thành **“bộ định tuyến trung tâm”**
    
*   Toàn bộ lưu lượng giữa các địa điểm sẽ đi qua mạng này
    

**Những gì hệ thống này làm:**

*   **Định tuyến thông minh**: chọn đường đi nhanh và ổn định nhất
    
*   **Firewall-as-a-Service**: lọc traffic, chặn tấn công
    
*   **Tối ưu hiệu suất** giữa các chi nhánh và cloud
    
*   Kết nối qua **Network Interconnect** tốc độ cao
    

### **Email Security**

**Mô hình:** Lá chắn bảo vệ hệ thống email (đặc biệt là email cloud như Google Workspace, Microsoft 365).

**Cách hoạt động:**

*   Tất cả email **đến và đi** đều được kiểm tra trước khi vào hộp thư
    
*   Hệ thống sẽ **phân tích nội dung, link, file đính kèm và người gửi**
    
*   Nếu phát hiện nguy cơ → **chặn, cảnh báo hoặc cách ly email**
    

**Những gì Email Security làm:**

*   Ngăn chặn phishing (email giả mạo ngân hàng, công ty…)
    
*   Phát hiện malware trong file đính kèm
    
*   Chống giả mạo domain thông qua **DMARC**
    
*   Kiểm soát luồng email để tránh rò rỉ dữ liệu
    

## **Application Security**

### **Tường lửa ứng dụng web (WAF)**

WAF tạo ra một lá chắn giữa ứng dụng web và Internet để lọc lưu lượng độc hại. WAF của Cloudflare kết hợp sức mạnh của công nghệ Máy học (ML) và các bộ quy tắc (như OWASP Top 10 và các quy tắc do Cloudflare quản lý) để tự động chặn các phương thức tấn công nguy hiểm như SQL Injection hay XSS. Nó cũng có khả năng kiểm tra thông tin xác thực bị rò rỉ (Exposed Credentials Check) để chặn các nỗ lực đăng nhập trái phép.

Cách hoạt động (trong Cloudflare)

1.  Người dùng gửi request tới website
    
2.  Request đi vào mạng Cloudflare (edge gần nhất)
    
3.  WAF tiến hành:
    
    *   Phân tích request (IP, header, payload, hành vi)
        
    *   So sánh với **rule + ML model**
        
4.  Cloudflare quyết định:
    
    *   Cho phép (Allow)
        
    *   Chặn (Block)
        
    *   Thử thách (CAPTCHA / JS Challenge)
        

**Các thành phần chính**

1.  Managed Rules: Dựa trên tiêu chuẩn như OWASP Top 10 Cloudflare tự cập nhật liên tục. Chặn các lỗ hổng phổ biến: SQL Injection XSS Remote Code Execution
    
2.  Machine Learning (ML) Cloudflare dùng ML để: Nhận diện traffic bất thường Phát hiện bot/tấn công mới chưa có rule. Giảm false positive (chặn nhầm user thật)
    
3.  Exposed Credentials Check :So sánh username/password với các dữ liệu bị rò rỉ .Nếu trùng → chặn đăng nhập.Ngăn:Credential stuffing Account takeover
    
4.  Custom Rules: Chặn IP / quốc gia. Giới hạn request (rate limiting). Bảo vệ endpoint nhạy cảm (/login, /api)
    
5.  Bot Management (liên kết với WAF) Phân biệt bot tốt và bot xấu Tự động: Block bot độc hại Cho phép bot hợp lệ (Google, Bing…)
    

### **Bot Management**

Giải pháp này phân tích và gán Điểm Bot (Bot Score) từ 1 đến 99 cho mọi yêu cầu truy cập (1 là bot tự động, 99 là con người). Bằng cách sử dụng công nghệ ML, phát hiện điểm bất thường và trích xuất dấu vân tay trình duyệt, hệ thống sẽ tự động chặn các bot xấu (chuyên dò mật khẩu hoặc cào dữ liệu) mà vẫn cho phép người dùng thật và các bot tốt (như GoogleBot) đi qua.

Cloudflare phân biệt người và máy bằng cách đánh giá mọi yêu cầu truy cập và gán một **Bot Score (Điểm Bot)** từ 1 đến 99.

*   **Điểm 1** có nghĩa là chắc chắn do máy (bot) tự động thực hiện.
    
*   **Điểm 99** có nghĩa là chắc chắn do con người thao tác.
    

Để chấm được số điểm này một cách chính xác mà không làm chậm trang web, Cloudflare đưa dữ liệu qua 5 công cụ kiểm tra song song:

1.  **Máy học (Machine Learning):** Đây là "bộ não" chính. Nó học hỏi từ hàng nghìn tỷ yêu cầu trên toàn mạng lưới Cloudflare mỗi ngày để nhận diện các hành vi tinh vi, từ đó chấm điểm từ 2 đến 99.
    
2.  **Dò tìm tĩnh (Heuristics):** So khớp nhanh với cơ sở dữ liệu các signature bot độc hại đã biết. Nếu khớp, nó lập tức chấm điểm 1.
    
3.  **Phát hiện bất thường (Anomaly Detection):** Ghi nhận mức truy cập bình thường của trang web và lập tức chấm điểm 1 cho các luồng truy cập tăng vọt một cách vô lý.
    
4.  **Phát hiện qua JavaScript (JSD):** Kiểm tra ngầm ở phía máy khách để lật tẩy các "trình duyệt ảo" (headless browser) thường được hacker sử dụng để ngụy trang.
    
5.  **Bot được xác minh (Verified Bots):** Nhận diện và cho phép các bot "tốt" có ích (như GoogleBot phục vụ tìm kiếm SEO) đi qua an toàn.
    

### **API Shield**

Vì API thường là mục tiêu dễ bị tấn công nhất, API Shield áp dụng mô hình "bảo mật tích cực". Thông qua cơ chế Xác thực lược đồ (Schema Validation), nó kiểm tra mọi luồng dữ liệu và lập tức chặn bất kỳ yêu cầu nào không tuân thủ chính xác 100% cấu trúc API đã được định nghĩa từ trước. Đồng thời, nó giám sát dữ liệu trả về để ngăn chặn rò rỉ thông tin nhạy cảm (API DLP).

Hiện nay, các tính năng cao cấp cung cấp cho API Security của Cloudlfare sẽ bao gồm:

• API Discovery: Cho phép phát hiện, mapping các API, phân tích tích bề mặt tấn công.

• Volumetric Abuse Detection: Cho phép rate limit thích ứng đối với API.

• Sequence Analytics: cho phép lọc ra các chuỗi request API quan trọng được tìm thấy trong toàn bộ API traffic theo thời gian

• Sequence Mitigation: Cho phép thực thi các mẫu request đối với các ứng dụng đã xác thực giao tiếp với API.

• GraphQL malicious query protection: Bảo vệ cho API sử dụng GraphQL

• JSON Web Tokens Validation: JSON Web Tokens Validation của API Shield ngăn chặn các cuộc tấn công phát lại JWT và giả mạo JWT bằng cách xác minh bằng mật mã các JWT đến trước khi chúng được chuyển đến nguồn gốc API.

• Mutual TLS (mTLS): Xác thực TLS chung (mTLS) sử dụng cert để đảm bảo lưu lượng truy cập giữa client và server được bảo mật và tin cậy hai chiều.

• Schema Validation: Schema Validation cho phépkiểm tra xem lưu lượng truy cập đến có tuân thủ cấu trúc Schema cho trước hay không. Khi quản trị viên cung cấp Schema API cho Cloudflare, API Shield sẽ tạo các rulesets cho lưu lượng truy cập đến từ các định nghĩa từ trước. Các rulesets này xác định lưu lượng nào được phép và lưu lượng nào được ghi lại hoặc bị chặn.

Cơ chế Xác thực lược đồ (Schema Validation) của API Shield hoạt động như một "người gác cổng" tuân thủ hợp đồng tuyệt đối.

Nó hoạt động dựa trên mô hình **bảo mật tích cực (Positive Security)** — nghĩa là "chặn tất cả, chỉ cho phép những dữ liệu đã biết là an toàn đi qua". Cách thức cụ thể như sau:

*   **Cung cấp bản thiết kế:** Quản trị viên tải lên hệ thống Cloudflare một bản định nghĩa cấu trúc API (thường dùng định dạng OpenAPI hoặc Swagger). Bản này mô tả chính xác API được phép nhận phương thức gì, trường dữ liệu nào, độ dài bao nhiêu.
    
*   **Tự động tạo luật chặn:** API Shield tự động dịch bản thiết kế đó thành các bộ quy tắc (rulesets) hoạt động tại máy chủ biên.
    
*   **Chặn đứng tức thì:** Khi một request gửi đến, hệ thống sẽ đối chiếu với bộ quy tắc này. Bất kỳ request nào sai định dạng, thiếu hoặc thừa tham số so với cấu trúc đã khai báo đều sẽ bị chặn ngay lập tức, triệt tiêu nguy cơ tin tặc chèn mã độc.
    

### **Bảo vệ DDoS Layer 7**

Hệ thống luôn ở trạng thái bật để tự động rà soát và đánh chặn các cuộc tấn công ngập lụt ứng dụng (như HTTP flood) nhằm làm cạn kiệt tài nguyên máy chủ. Nó sở hữu khả năng bảo vệ thích ứng (Adaptive DDoS protection), tự động học hỏi hành vi và phân phối các quy tắc chặn lưu lượng rác chỉ trong vài giây mà không làm chậm ứng dụng.

**Cách thức hoạt động:** Hệ thống lấy mẫu và phân tích luồng dữ liệu một cách độc lập (ngoài luồng), rà soát kỹ các siêu dữ liệu của HTTP request (như User Agent, đường dẫn, tỷ lệ yêu cầu) và số liệu phản hồi từ máy chủ (như mã lỗi). Khi phát hiện tấn công, nó lập tức tạo ra một "dấu vân tay" (signature) theo thời gian thực để chặn đứng luồng dữ liệu rác mà vẫn cho phép người dùng hợp lệ đi qua.

**Hai vũ khí cốt lõi của giải pháp:**

1.  **Bộ quy tắc được quản lý (HTTP DDoS Attack Protection managed ruleset):** Đây là lá chắn luôn bật (Always-ON) chứa các mẫu nhận diện tấn công đã biết. Nó tự động dập tắt các cuộc tấn công phổ biến như HTTP flood, Slowloris, hay các đợt càn quét từ mạng botnet Mirai.
    
2.  **Bảo vệ DDoS thích ứng (Adaptive DDoS protection):** Tính năng này thông minh hơn nhờ khả năng tự động học hỏi hành vi truy cập của trang web trong 7 ngày gần nhất (sử dụng bách phân vị thứ 95 để loại trừ các khoảng nhiễu dữ liệu). Kết hợp cùng Machine Learning, nó cung cấp 3 lớp phân tích sâu:
    
    *   *Nhận biết nguồn gốc (Origin-aware):* Chặn nguồn luồng dữ liệu làm tăng vọt tỷ lệ lỗi bất thường trên máy chủ gốc.
        
    *   *Nhận biết User-agent:* Chặn các request có thông tin trình duyệt/ứng dụng (User Agent) bất thường so với dữ liệu chung toàn cầu.
        
    *   *Nhận biết vị trí (Location-aware):* Đánh chặn lưu lượng đến từ các khu vực địa lý hoàn toàn sai lệch so với hồ sơ phân phối thông thường của ứng dụng.
        

## **Application Performance**

### **Load Balancing**

Không giống như các bộ cân bằng tải phần cứng truyền thống, Load Balancing của Cloudflare hoạt động trên mạng lưới toàn cầu ở Lớp 7 (Lớp ứng dụng). Hệ thống sẽ liên tục giám sát tình trạng (Active monitoring) của các máy chủ gốc. Khi phát hiện một máy chủ bị sập hoặc quá tải, nó lập tức chuyển hướng (failover) lưu lượng sang máy chủ khỏe mạnh khác, đảm bảo người dùng không bị gián đoạn. Ngoài ra, nó định tuyến truy cập rất thông minh dựa trên độ trễ, vị trí địa lý (Geo), hoặc máy chủ nào đang rảnh rỗi nhất. Nó cũng hỗ trợ Session Affinity (duy trì phiên) để giữ khách hàng kết nối với cùng một máy chủ trong lúc họ đang thực hiện giao dịch mua sắm.Hệ thống này còn có khả năng **Định tuyến thích ứng (Adaptive Routing)**, tự động thử gửi lại yêu cầu sang một máy chủ khỏe mạnh khác nếu máy chủ ban đầu gặp sự cố và trả về mã lỗi.

Intelligent routing: Chọn xem phân phối các request dựa trên độ trễ của máy chủ, khu vực địa lý của khách truy cập hay thậm chí là tọa độ GPS của khách truy cập. Khi các request đến bộ cân bằng tải của khách hàng, nó sẽ phân phối chúng trên các pool và origin của khách hàng theo ba yếu tố:

*   Pool and origin health: Các quyết định về lưu lượng truy cập bắt đầu với việc nhóm và nguồn gốc nào có sẵn và sẽ nhận được lưu lượng truy cập.
    
*   Traffic steering: Các chính sách được đặt trên bộ cân bằng tải của khách hàng định tuyến lưu lượng truy cập đến các nhóm được đính kèm và có sẵn. Các chính sách chỉ đạo lưu lượng quyết định cách bộ cân bằng tải định tuyến lưu lượng truy cập đến các pool chạy ổn định
    
*   Standard: Các chính sách tiêu chuẩn bao gồm Off - Failover (bằng cách xác định mức độ ưu tiên của từng Origin) và Random (bằng cách định tuyến failover đến các pool ngẫu nhiên).
    
*   Dynamic: sử dụng dữ liệu Health monitor để xác định pool nhanh nhất đối với Cloudflare Region hoặc trung tâm dữ liệu nhất định.
    
*   Proximity: Chỉ dẫn khoảng cách định tuyến khách truy cập hoặc dịch vụ nội bộ đến trung tâm dữ liệu vật lý gần nhất.
    
*   Least Outstand Requests: cho phép khách hàng định tuyến lưu lượng truy cập đến các pool đang có số lượng yêu cầu chưa xử lý ít nhất.
    

**Origin steering:** Đây là các chính sách được đặt trên mỗi pool định tuyến lưu lượng truy cập đến các máy chủ origin. Các chính sách này được xây dựng trên hai yếu tố gồm policy và weight.

*   Random: các origin có weight bằng 1 và các request sẽ được gửi đeến ngẫu nhiên các origin này.
    
*   Hash: tỷ lệ request được gửi đến các origin sẽ thay đổi dựa trên phân phối IP của các request.
    
*   Least Outstand Requests: cho phép định tuyến lưu lượng truy cập đến các origin đang có số lượng yêu cầu chưa xử lý ít nhất.
    

**Local Traffic Management**: Local Traffic Management cho phép khách hàng cân bằng tải lưu lượng truy cập trong trung tâm dữ liệu giữa các máy chủ của khách hàng, loại bỏ nhu cầu về thiết bị phần cứng và cho phép di chuyển cơ sở hạ tầng sang đám mây để hưởng lợi từ khả năng mở rộng đàn hồi và độ tin cậy. Quản lý lưu lượng cục bộ có khả năng hỗ trợ virtual IP, private IP và public IP làm giá trị gốc trong trung tâm dữ liệu của khách hàng

**Session affinity**: Khi bạn kích hoạt tính năng này, bộ cân bằng tải của bạn sẽ hướng tất cả các yêu cầu từ một người dùng cuối cụ thể đến một máy chủ gốc cụ thể. Tính liên tục này lưu giữ thông tin về phiên người dùng - chẳng hạn như các mặt hàng trong giỏ hàng của họ - thông tin này có thể bị mất nếu các yêu cầu được trải ra giữa nhiều máy chủ. Tính năng này cũng có thể giúp giảm yêu cầu mạng, dẫn đến tiết kiệm cho khách hàng với thanh toán dựa trên mức sử dụng.

**Adaptive routing**: tính năng này kiểm soát các tính năng sửa đổi định tuyến của các request đến pool và origin để đáp ứng các điều kiện động, chẳng hạn như trong khoảng thời gian giữa các yêu cầu giám sát tình trạng hoạt động. Nếu có một origin hoạt động ổn định khác trong cùng một nhóm, yêu cầu sẽ được thử lại một lần đối với origin này khi nhận được HTTP response code 521, 522 và 523.

### **CDN**

Cloudflare tận dụng mạng lưới máy chủ biên khổng lồ đặt tại hơn 300 thành phố trên toàn thế giới để lưu trữ bản sao (cache) nội dung trang web của bạn. Khi người dùng truy cập, nội dung tĩnh sẽ được gửi trực tiếp từ máy chủ gần họ nhất thay vì phải chạy một chặng đường dài về máy chủ gốc. Điều này giúp tốc độ tải trang nhanh hơn đáng kể, đồng thời giảm tải và tiết kiệm chi phí băng thông cho máy chủ của bạn.

Các cơ chế quan trọng

Edge Caching

*   Nội dung được lưu tại **data center gần user**
    
*   Giảm khoảng cách → giảm latency
    

Anycast Routing

*   Một IP duy nhất nhưng nhiều location
    
*   Request luôn được định tuyến đến **edge gần nhất**
    

Cache Invalidation (Purge)

*   Xóa cache khi nội dung thay đổi
    
*   Có thể:
    
    *   Xóa toàn bộ
        
    *   Xóa theo URL
        

Tiered Caching

*   Edge không lấy trực tiếp từ origin
    
*   Mà lấy từ **edge cấp cao hơn (regional cache)**
    

\->Giảm tải origin mạnh hơn nữa

### **DNS**

Cloudflare cung cấp dịch vụ DNS doanh nghiệp và hệ thống DNS 1.1.1.1 có tốc độ cực kỳ nhanh chóng và an toàn. Bằng cách phân giải tên miền ngay tại các máy chủ biên trên toàn cầu gần người dùng nhất, nó mang lại hiệu suất xuất sắc và giảm độ trễ đáng kể. Các bài kiểm tra hiệu năng thậm chí cho thấy DNS của Cloudflare phản hồi nhanh gấp 10 lần so với một số đối thủ cùng ngành.

### **Smart Routing (Định tuyến thông minh)**

Hệ thống này hoạt động như một ứng dụng bản đồ giao thông cho luồng dữ liệu Internet. Nó liên tục phân tích tình trạng mạng lưới để tìm ra và tự động chuyển hướng dữ liệu đi qua các tuyến đường nhanh nhất, ít tắc nghẽn nhất. Điều này giúp tránh được các điểm nghẽn cáp quang hay sự cố đứt cáp, đảm bảo ứng dụng luôn mượt mà.

## Network

### **L3/4 DDoS protection**

Cung cấp khả năng đánh chặn các cuộc tấn công ngập lụt lớp mạng. Các giải pháp tiêu biểu bao gồm **Magic Transit** (sử dụng giao thức BGP và đường hầm GRE để bảo vệ toàn bộ trung tâm dữ liệu) và **Spectrum** (bảo vệ các ứng dụng dùng giao thức TCP/UDP).

Cách hoạt động (đi sâu)

1.  Hấp thụ lưu lượng tại edge Traffic đi vào mạng Cloudflare toàn cầu Các data center sẽ: Phân tán và hấp thụ lưu lượng lớn Tránh việc dồn vào một điểm. Giống như “trải đều áp lực” trên toàn cầu
    
2.  Phân tích packet (packet-level inspection): Cloudflare kiểm tra: IP source Protocol (TCP/UDP/ICMP) Flags bất thường (SYN flood, UDP flood…)
    
3.  Lọc và chặn tấn công Traffic bất thường bị: Drop ngay tại edge Rate limit Traffic hợp lệ: Được forward về hệ thống
    

Để đi sâu hơn vào bước 2 (Phân tích) và bước 3 (Lọc) mà bạn vừa nêu, Cloudflare thực chất vận hành 3 "cỗ máy" tự trị (autonomous) được xây dựng trên nền tảng Linux để xử lý:

1.  **dosd (Hệ thống phi tập trung):** Phần mềm này chạy độc lập trên mọi máy chủ ở tất cả các trung tâm dữ liệu biên. Nó liên tục phân tích các trường của gói tin (IP, cổng, cờ TCP) và lập tức tạo ra các quy tắc chặn rác cục bộ với tốc độ siêu nhanh.
    
2.  **Gatebot (Hệ thống tập trung):** Đóng vai trò là tổng chỉ huy. Khi một đợt tấn công DDoS phân tán với khối lượng khổng lồ diễn ra trên toàn cầu, Gatebot sẽ tổng hợp mẫu dữ liệu từ các trạm, phân tích và tự động gửi chỉ thị đánh chặn đồng loạt.
    
3.  **flowtrackd (Theo dõi trạng thái luồng):** Đây là hệ thống chuyên đối phó với các đợt tấn công TCP ngẫu nhiên và phức tạp nhất. Nó theo dõi trạng thái của từng kết nối TCP và lập tức vứt bỏ (drop) các gói tin không thuộc về một phiên hợp lệ.
    

Sau khi rác bị loại bỏ ở bước 3, lưu lượng sạch sẽ được chuyển tiếp (forward) an toàn về hạ tầng gốc của bạn.

**Cloudflare Spectrum** hoạt động như một hệ thống proxy ngược (reverse-proxy) chuyên dụng ở Lớp 4 (L4), giúp bảo vệ và tăng tốc các ứng dụng không phải web chạy trên giao thức TCP và UDP (như máy chủ game, email, hệ thống SSH).

Cách thức bảo vệ của Spectrum dựa trên hai cơ chế chính:

1.  **Ẩn danh máy chủ gốc (IP Masking):** Spectrum thay thế địa chỉ IP thực của máy chủ gốc bằng địa chỉ IP của Cloudflare. Đối với người dùng và tin tặc trên Internet, ứng dụng của bạn trông như đang được phát ra từ Cloudflare. Điều này khiến tin tặc không thể tìm ra địa chỉ IP thật để tấn công trực tiếp vào máy chủ gốc của bạn.
    
2.  **Hấp thụ tấn công ngập lụt (Volumetric):** Do toàn bộ lưu lượng TCP/UDP đều bị ép đi vòng qua mạng lưới máy chủ biên của Cloudflare trước, hệ thống sẽ tận dụng sức mạnh mạng lưới khổng lồ để lọc và hấp thụ hoàn toàn các đợt tấn công DDoS quy mô lớn, chỉ cho phép lưu lượng sạch đi vào hạ tầng của bạn.
    

Giải pháp **Magic Transit** hoạt động bằng cách đặt mạng lưới Cloudflare làm "cửa trước" đánh chặn cho toàn bộ hạ tầng mạng IP của doanh nghiệp.

Cơ chế hoạt động cụ thể qua 3 bước như sau:

*   **Bước 1 - Thu hút lưu lượng bằng BGP:** Cloudflare sử dụng giao thức Border Gateway Protocol (BGP) để thay mặt bạn thông báo dải địa chỉ IP của công ty lên Internet toàn cầu. Nhờ công nghệ Anycast, bất kỳ lưu lượng nào hướng đến trung tâm dữ liệu của bạn cũng sẽ tự động được hút về máy chủ biên Cloudflare gần người dùng đó nhất.
    
*   **Bước 2 - Lọc rác tại biên:** Ngay khi dữ liệu chạm vào mạng Cloudflare, hệ thống sẽ tiến hành kiểm tra, phân tích và chặn đứng các đợt tấn công DDoS (như UDP flood hay SYN flood) ngay tại rìa mạng.
    
*   **Bước 3 - Truyền dữ liệu sạch qua đường hầm GRE:** Lưu lượng hợp lệ (sạch) sau đó sẽ được đóng gói và vận chuyển an toàn về trung tâm dữ liệu gốc của bạn thông qua các đường hầm Anycast GRE (Generic Routing Encapsulation) hoặc thông qua các kết nối mạng vật lý trực tiếp (CNI).
    

**Sự khác biệt chính giữa bảo vệ DDoS Lớp 3/4 và Lớp 7 nằm ở mục tiêu nhắm đến, loại hình tấn công và giải pháp đánh chặn:**

*   **Mục tiêu bảo vệ:** Lớp 3/4 (Mạng và Giao vận) bảo vệ toàn bộ hạ tầng mạng IP và các ứng dụng chạy trên TCP/UDP (như máy chủ game, email, SSH). Trong khi đó, Lớp 7 (Ứng dụng) tập trung bảo vệ các trang web và API hoạt động qua giao thức HTTP/HTTPS.
    
*   **Loại hình tấn công:** Tấn công Lớp 3/4 thường là các đợt ngập lụt dữ liệu (volumetric) nhằm làm cạn kiệt băng thông hoặc tài nguyên mạng cục bộ, ví dụ như UDP flood, SYN flood hay ICMP flood. Tấn công Lớp 7 tinh vi hơn, chúng mô phỏng các yêu cầu truy cập hợp lệ (như HTTP GET/POST flood, Slowloris) để đánh sập tài nguyên xử lý của máy chủ web.
    
*   **Giải pháp của Cloudflare:** Để chặn DDoS Lớp 3/4, Cloudflare dùng **Magic Transit** (thu hút lưu lượng qua BGP, lọc rác và trả về qua đường hầm GRE) và **Spectrum** (proxy ngược cho ứng dụng TCP/UDP). Để chặn DDoS Lớp 7, hệ thống dựa vào phân tích siêu dữ liệu HTTP thông qua các bộ quy tắc cấu hình sẵn (HTTP DDoS managed rulesets) và công nghệ bảo vệ thích ứng (Adaptive DDoS).
    

### **Firewall-as-a-service**

Đóng vai trò như một chốt chặn trên đám mây, giúp nhận, kiểm tra và xử lý các gói tin IP trước khi xuất chúng vào hạ tầng gốc của bạn.

Thay vì phải mua, cấu hình và bảo trì các thiết bị tường lửa phần cứng đắt tiền tại trung tâm dữ liệu cục bộ, Cloudflare tích hợp sẵn tường lửa Lớp 3 (L3 Firewall) ngay trên mạng lưới Anycast toàn cầu của họ.

Cơ chế này mang lại những ưu điểm vượt trội:

*   **Bảo vệ ngay tại biên (Edge):** Mọi gói tin IP hướng đến mạng của bạn đều phải đi qua các máy chủ biên của Cloudflare. Tại đây, chúng được kiểm tra cặn kẽ và áp dụng các quy tắc lọc (cho phép, chặn hoặc ghi log) trước khi được định tuyến an toàn về máy chủ gốc.
    
*   **Loại bỏ điểm nghẽn (Choke points):** Với tường lửa phần cứng truyền thống, toàn bộ lưu lượng thường bị dồn về một thiết bị vật lý gây ra tình trạng thắt cổ chai. Tường lửa đám mây giải quyết triệt để vấn đề này bằng cách phân tán luồng xử lý trên hàng trăm trung tâm dữ liệu toàn cầu, đảm bảo hiệu suất tối đa.
    
*   **Quản lý đồng nhất:** Quản trị viên chỉ cần một bảng điều khiển duy nhất để thiết lập và thực thi các chính sách bảo mật nhất quán cho toàn bộ các văn phòng, chi nhánh hay trung tâm dữ liệu của công ty.
    

### **Network Interconnect**

Cho phép doanh nghiệp thiết lập kết nối vật lý hoặc ảo (CNI) trực tiếp, an toàn từ trung tâm dữ liệu của họ vào mạng lưới Cloudflare, mang lại tốc độ cao hơn và bảo mật tốt hơn so với việc định tuyến qua Internet công cộng.

### **Smart Routing**

Sử dụng các công nghệ (như Argo Smart Routing) để liên tục phân tích và tự động chuyển hướng lưu lượng dữ liệu đi qua các tuyến đường mạng nhanh nhất, đáng tin cậy nhất.

# Conclusion

Cloudflare là một nền tảng toàn diện kết hợp **bảo mật, hiệu suất và mạng lưới toàn cầu** trong một hệ sinh thái duy nhất. Thông qua các công nghệ như Zero Trust, WAF, DDoS Protection, CDN, DNS và Smart Routing, Cloudflare không chỉ bảo vệ ứng dụng trước các mối đe dọa ngày càng tinh vi mà còn tối ưu tốc độ và độ ổn định khi truy cập.

Điểm mạnh cốt lõi của Cloudflare nằm ở việc triển khai mọi dịch vụ **ngay tại edge (biên mạng)**, giúp xử lý lưu lượng gần người dùng nhất, từ đó giảm độ trễ, tăng hiệu suất và ngăn chặn tấn công trước khi chúng chạm đến hệ thống gốc. Đồng thời, khả năng tự động hóa, học máy và thích ứng theo thời gian thực giúp Cloudflare luôn theo kịp sự thay đổi của môi trường Internet.