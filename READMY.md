-chuẩn seo trong 1 trang chỉ có 
1 thẻ H1
3-5 thẻ H2
.btn:link,
.btn:visited
:link là thẻ bình thường khi chưa dc user click
:visited là thẻ khi được user click -visited áp dụng cho liên kết đã được truy cập
:action là trong quá trình người dùng click nhưng chưa nhả ra
::after{} : là sau đó nó sẽ thực hiện việc gì đó
sử dụng với button thì sẽ tạo ra 1 button giống hệt nằm bên dưới button gốc
animation-iteration-count: infinite; số lần lặp lại
--------------------------------
-Bài:10 BEM(Block Element Modifier)
+ suy nghĩ về cách tổ chức code
+ đặt tên class có cấu trúc
+ chia nhỏ các thành phần css thành các file nhỏ 1 cách logic
BEM:Block Element Modifier
+ Block: là tên của component mô tả tổng thể của component đó
+ Element: để đặt tên cho các thành phần bổ trợ cho component đó
+ Modifier: các biến thể khác của Block và Elment
SASS: hỗ trợ ta trong việc chia code css thành các folders hoặc các file chứa css
- project này chúng ta sẽ chia làm 7 folders và 1 file main.sass chính improt tất cả các files trong các folder để compile thành css
+1 Base chứa các cn setting ban đầu
+2 Components chứa các bộ phận nhỏ dễ tái sử dụng như button,card...
+3 Layout chứa footer, navbar
+4 pages chứa tên các page nếu project web của bạn có nhiều page khác nhau vd: home, login
+5 Abstracts chứa animation, các function ,mixin khi sử dụng sass
+6 Themes chứa các mẫu có sẵn
+7 Vendors code css bên ngoài như bootstrap
-variables
-nesting
-mixins
-function
-extend
------------
Bài 13+14: Variables, Nesting, Mixin, function, extend
VD: Mixin
C1
@mixin CSSLink{
    color: red;
    text-decoration: none
}

.list__link{
    @include cssLink;
}
C2:
@mixin CSSLink($color,$status){
    color: red;
    text-decoration: none
}

.list__link{
    @include cssLink(red,none);
}
function
@function calMargin($a,$b){
    @return $a*$b
}

.list{
    margin: calMargin(2,5)*1px
}
extend
%CSSLink($color,$status){
    color: red;
    text-decoration: none
}

.list__link{
    extend %cssLink;
}
Bài 15: Setup Node-SASS