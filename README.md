# Sass Guideline

*Nguồn: https://sass-guidelin.es/*

*Gitpage: https://dinhtienn.github.io/sass-guideline/*

## Hướng dẫn sử dụng Sass chuẩn mực, có khả năng bảo trì và mở rộng (mang quan điểm cá nhân).

### Dự án Sass Guidelines được dịch sang nhiều ngôn ngữ bởi [những người đóng góp](https://github.com/HugoGiraudel/sass-guidelines/issues/96).

## Về tác giả

Tên tôi là [Hugo Giraudel](http://hugogiraudel.com/), Tôi là một front-end developer người Pháp, có trụ sở tại Berlin (Đức) từ năm 2015, hiện đang làm việc tại [N26](https://n26.com/).

Tôi đã viết Sass được vài năm nay và tôi là tác giả của nhiều dự án liên quan đến Sass như [SassDoc](http://sassdoc.com/), [SitePoint Sass Reference](http://sitepoint.com/sass-reference/) và [Sass-Compatibility](http://sass-compatibility.github.io/). Nếu bạn quan tâm nhiều hơn đến những đóng góp của tôi cho cộng đồng Sass, hãy xem qua [danh sách này](http://github.com/HugoGiraudel/awesome-sass).

Tôi cũng là tác giả của một cuốn sách về CSS (bằng tiếng Pháp) có tựa đề [CSS3 Pratique du Design Web](http://css3-pratique.fr/) (phiên bản *Eyrolles*), cũng như một cuốn sách về Sass (bằng Tiếng Anh) có tên [Jump Start Sass](https://learnable.com/books/jump-start-sass) (phiên bản *Learnable*).

## Đóng góp

Sass Guidelines là một dự án miễn phí mà tôi duy trì trong thời gian rảnh rỗi. Không cần phải nói, đó là một khối công việc khá lớn để giữ cho mọi thứ được cập nhật, được dẫn chứng và thích hợp. Rất may, tôi nhận được sự đóng góp của rất nhiều người tuyệt vời đặc biệt là việc duy trì hàng tá các bản dịch khác nhau. Hãy chắc chắn cảm ơn họ nhé!

Nếu bạn muốn đóng góp vào dự án, vui lòng tweet về nó, truyền bá hoặc sửa từng lỗi đánh máy nhỏ bằng cách mở ra một issue hoặc pull-request trên [GitHub repository](https://github.com/HugoGiraudel/sass-guidelines) sẽ là rất tuyệt vời!

Cuối cùng nhưng không kém phần quan trọng trước khi ta bắt đầu: Nếu bạn thích tài liệu này hoặc nó hữu ích cho bạn hoặc team của bạn, vui lòng xem xét việc hỗ trợ để tôi có thể tiếp tục làm việc với nó!

## Về Sass

Đây là cách [Sass](http://sass-lang.com/) được mô tả trong [documentation](http://sass-lang.com/documentation/file.SASS_REFERENCE.html) của nó:

> Sass là một phần mở rộng của CSS tăng thêm sức mạnh và sự thanh lịch tới ngôn ngữ cơ bản.

Mục tiêu cuối cùng của `Sass` là sửa những thiếu xót của CSS. CSS, như chúng ta đã biết, không phải là ngôn ngữ tốt nhất trên thế giới [cần dẫn nguồn]. Mặc dù rất đơn giản để học, nó có thể nhanh chóng trở nên khá lộn xộn, đặc biệt là trong các dự án lớn.

Đó là lý do Sass xuất hiện, như một meta-language, để cải thiện cú pháp của CSS nhằm cung cấp các tính năng bổ sung và các công cụ tiện dụng. Trong khi đó, Sass muốn bảo tồn về ngôn ngữ CSS.

Điều này không biến Css trở thành một ngôn ngữ lập trình đầy đủ tính năng; Sass chỉ muốn giúp đỡ những nơi CSS thất bại. Chính về điều này, khởi đầu với Sass không khó hơn việc học Css, nó đơn giản là thêm một vài [tính năng bổ sung](http://sitepoint.com/sass-reference/) trên đầu của nó.

Điều đó nghĩa rằng, có nhiều cách để sử dụng những tính năng này. Một vài chỗ tốt, một vài chỗ tệ, một số bất bình thường. Các hướng dẫn này nhằm cung cấp cho bạn một cách tiếp cận nhất quán và được dẫn chứng rõ ràng để viết code Sass.

### *Ruby Sass hay LibSass*

[Commit đầu tiên của Sass](https://github.com/hcatlin/sass/commit/fa5048ba405619273e474a50400c7243fbff54fe), trở lại vào cuối năm 2016, hơn 10 năm trước. Không cần phải nói nó đã đi một chặng đường dài kể từ đó. Ban đầu được phát triển trên Ruby, các port khác nhau xuất hiện ở đây đó. Phiên bản thành công nhất, [LibSass](http://webdesign.tutsplus.com/articles/getting-to-know-libsass--cms-23114) (được viết bằng C/C++) hiện đã gần như tương thích hoàn toàn với phiên bản Ruby gốc.

Vào năm 2014, [các team Ruby Sass và LibSass đã quyết định chờ đợi cả hai phiên bản đồng bộ hoá trước khi chuyển tiếp](https://github.com/sass/libsass/wiki/The-LibSass-Compatibility-Plan). Kể từ đó, LibSass đã tích cực phát hành các phiên bản để có tính năng tương đương với các phiên bản cũ hơn của nó. Những mâu thuẫn còn lại của nó được tôi thu thập và liệt kê tại dự án [Sass-Compatibility](http://sass-compatibility.github.io/). Nếu bạn nhận thấy sự không tương thích giữa hai phiên bản mà không được liệt kê, vui lòng mở ra một issue.

Quay trở lại chọn trình biên dịch. Trên thực tế, tất cả đều phụ thuộc vào dự án của bạn. Nếu nó là một dự án Ruby on Rails, tốt nhất bạn nên sử dụng Ruby Sass là hoàn toàn phù hợp. Ngoài ra, hãy lưu ý rằng Ruby Sass sẽ luôn là bản triển khai tham chiếu và sẽ luôn dẫn đầu LibSass về các tính năng. Và nếu bạn đang tìm cách [chuyển từ Ruby Sass sang LibSass](http://www.sitepoint.com/switching-ruby-sass-libsass/), bài viết này là dành cho bạn.

Trong các dự án không phải Ruby cần tích hợp quy trình làm việc, LibSass có lẽ là một ý tưởng tốt hơn vì nó chủ yếu dành riêng cho việc được bao bọc. Vì vậy, nếu bạn muốn sử dụng, cùng nói về Node.js [node-sass](https://github.com/sass/node-sass) đều được chọn.

### *Sass hay SCSS*

Có khá nhiều nhầm lẫn về ngữ nghĩa của cái tên *Sass*, và câu trả lời xác đáng nhất: Sass mang nghĩa là cả bộ tiền xử lý và cú pháp của chính nó. Có vẻ nó không thích hợp lắm phải không?

Bạn thấy đấy, Sass ban đầu mô tả một cú pháp trong đó sự hạn chế riêng biệt chính là sự nhạy cảm lõm vào của nó. Ngay sau đó, những người duy trì Sass đã quyết định thu hẹo khoảng cách giữa Sass và CSS bằng cách cung cấp một cú pháp thân thiện với CSS có tên là *SCSS* nghĩa là *Sassy CSS*. Phương châm của nó là: nếu CSS hợp lệ, SCSS cũng hợp lệ.

Kể từ đó, Sass (bộ tiền xử lý) đã cung cấp [hai cú pháp khác nhau](http://www.sitepoint.com/whats-difference-sass-scss/): Sass (not all-caps, [please](http://sassnotsass.com/)), còn được gọi là *cú pháp thụt lề*, và SCSS. Sử dụng cái nào là tuỳ thuộc vào bạn vì cả hai đều tương đương nhau về tính năng. Nó chỉ là vấn đề thẩm mỹ tại thời điểm này.

Cú pháp nhạy cảm với khoảng trắng của Sass, dựa vào thụt lề để loại bỏ dấu ngoặc, dấu chấm phẩy và các ký hiệu dấu chấm câu khác, dẫn đến cú pháp gọn và ngắn hơn. Trong khi đó, SCSS dễ học hơn vì nó chủ yếu là một số bit thừa nhỏ trên CSS.

Cá nhân tôi, thích SCSS hơn Sass vì nó gần với CSS hơn và thân thiện hơn với hầu hết các nhà phát triển. Do đó, SCSS là cú pháp mặc địch trong suốt hướng dẫn này. Bạn có thể chuyển sang cú pháp thụt lề Sass trong bảng điều khiển bên.

### *Các bộ tiền xử lý khác*

Sass là một tiền xử lý trong số khác. Đối thủ nặng ký nhất của nó là [Less](http://lesscss.org/), một bộ tiền xử lý dựa trên Node.js đã trở nên khá phổ biến nhờ khung CSS nổi tiếng [Bootstrap](http://getbootstrap.com/) sử dụng nó (cho đến phiên bản 4). Ngoài ra còn có [Stylus](http://learnboost.github.io/stylus/), một bộ tiền xử lý rất dễ được chấp nhận và linh hoạt tuy nhiên hơi khó sử dụng và với một cộng đồng nhỏ hơn.

*Tại sao lại chọn Sass hơn bất kỳ bộ tiền xử lý nào khác?* vẫn là một câu hỏi xác đáng ngày nay. Cách đây không lâu, chúng tôi đã từng đề xuất Sass cho các dự án dựa trên Ruby vì nó lần đầu tiên được tạo ra trong Ruby và kết hợp tốt với Ruby on Rails. Hiện tại LibSass đã bắt kịp (chủ yếu) với Sass ban đầu, đây không còn là lời khuyên thích hợp.

Những gì tôi thích ở Sass là cách tiếp cận bảo toàn của nó với CSS. Thiết kế của Sass dựa trên các nguyên tắc mạnh mẽ: phần lớn phương pháp thiết kế xuất phát tự nhiên từ niềm tin của các team cốt lõi rằng thêm các tính năng bổ sung có chi phí phức tạp cần được chứng minh bằng tính hữu dụng và về những gì một block style cho trước đang làm bằng cách chỉ nhìn vào riêng khối đó. Ngoài ra, Sass có sự chú ý sắc nét hơn nhiều so với các bộ tiền xử lý khác. theo tôi, có thể nói rằng các nhà thiết kế cốt lõi quan tâm sâu sắc đến việc hỗ trợ mọi trường hợp tương thích CSS và đảm bảo mọi hành vi chung đều nhất quán. Nói cách khác, Sass là một phần mềm nhằm giải quyết các vấn đề thực tế, giúp cung cấp chức năng hữu ích cho những thiếu xót của CSS.

Bỏ qua các bộ tiền xử lý, chúng ta cũng nên đề cập đến các công cụ như [PostCSS](https://github.com/postcss/postcss) và [cssnext](https://cssnext.github.io/) đã tiếp xúc đáng kể trong vài tháng qua.

PostCSS thường được gọi là (và không chính xác) một “bộ xử lý hậu kỳ”. Giả định, kết hợp với cái tên rủi ro, là PostCSS phân tích cú pháp qua CSS đã được xử lý bởi một bộ xử lý trước. Mặc dù nó có thể hoạt động theo cách này, nhưng nó không phải là một yêu cầu, vì vậy PostCSS thực sự chỉ là một "bộ xử lý".

Nó cho phép bạn truy cập vào các “token” trong các stylesheets của bạn (như selectors, properties hay values), xử lý chúng với Javascript để thực hiện một số thao tác dưới mọi hình thức và biên dịch kết quả thành CSS. Ví dụ, thư viện tiền tố phổ biến [Autoprefixer](https://github.com/postcss/autoprefixer) được xây dựng bằng PostCSS. Nó phân tích mọi quy tắc để xem có cần tiền tố vendor hay không bằng cách tham khảo công cụ hỗ trợ trình duyệt [CanIUse](http://caniuse.com/), sau đó xoá và thêm tiền tố vendor cần thiết

Điều này cực kỳ mạnh mẽ và tuyệt vời để xây dựng các thư viện hoạt động với bất kỳ bộ tiền xử lý nào (cũng như vanilla CSS), nhưng PostCSS không hề đặc biệt dễ sử dụng. Bạn phải biết một chút Javascript để xây dựng bất cứ thứ gì với nó và API của nó đôi khi có thể gây nhầm lẫn. Mặc dù Sass chỉ cung cấp quyền truy cập trực tiếp vào CSS AST (*cây cú pháp trừu tượng*) và Javascript.

Tóm lại, Sass có phần dễ dàng và sẽ giải quyết hầu hết vấn đề của bạn. Mặc khác, PostCSS có thể khó để nắm bắt (nếu như bạn không giỏi với Javascript) nhưng hoá ra lại vô cùng mạnh mẽ. Không có lý do gì để bạn có thể sử dụng cả hai cách khác nhau. Trong thực tế, PostCSS cung cấp một trình phân tích cú pháp SCSS chính thức cho điều này.

<blockquote class="note"><p>Gửi lời cảm ơn đến <a href="https://github.com/corysimmons">Cory Simmons</a> bởi sự giúp đỡ của anh ấy và chuyên môn về phần này.</p></blockquote>

## Giới thiệu

### *Tại sao lại là một Styleguide*

Một styleguide không chỉ là một tài liệu dễ chịu để đọc, hình dung một trạng thái lý tưởng cho code của bạn. Đây là một tài liệu quan trọng trong sự sống của dự án, mô tả cách thức và lý do nên viết code. Nó có thể trông giống như hơi thừa thãi cho các dự án nhỏ, nhưng nó giúp ích rất nhiều trong việc giữ cho codebase được sạch sẽ, có khả năng mở rộng và dễ bảo trì.

Không cần phải nói, càng có nhiều developer tham gia vào một dự án, thì càng cần nhiều hướng dẫn về code. Dọc theo cùng một dòng, dự án càng lớn càng cần phải có một styleguide.

[Harry Roberts](http://csswizardry.com/) nói rất rõ trong [CSS Guidelines](http://cssguidelin.es/#the-importance-of-a-styleguide):

> Một styleguide về code (ghi chú không phải là một styleguide trực quan) là một công cụ có giá trị cho các team:
>
> - Xây dựng và bảo trì sản phẩm trong một khoảng thời gian hợp lý;
> - Có các developer với các khả năng về chuyên môn khác nhau;
> - Có một số developer khác nhau làm việc trên một sản phẩm tại bất kỳ thời điểm nào;
> - Nhân viên mời tham gia dự án;
> - Có một số codebases mà các developer nhúng vào và bỏ đi.

### *Cho những người không đồng tình*

Điều đầu tiên: **đây không phải là một CSS styleguide**. Tài liệu này sẽ không thảo luận về các quy ước đặt tên cho các lớp CSS, các mẫu module và câu hỏi về ID trong thế giới CSS. Những hướng dẫn này chỉ nhằm mục đích xử lý nội dung dành riêng cho Sass.

Ngoài ra, đây là styleguide của riêng tôi và do đó nó **rất opinionated**. Hãy nghĩ về nó như một bộ sưu tập các phương pháp và lời khuyên mà tôi đã đánh bóng và đưa ra trong nhiều năm. Nó cũng cho tôi cơ hội liên kết với một số ít tài nguyên sâu sắc, vì vậy hãy chắc chắn kiểm tra qua *bài đọc thêm*.

Rõ ràng, đây chắc chắn không phải là cách duy nhất để làm việc, và nó có thể có hoặc không phù hợp với dự án của bạn. Hãy chọn từ nó những thứ thích ứng với nhu cầu của bạn. Như ta vẫn thường nói *your mileage may vary*.

### *Những nguyên tắc chủ chốt*

Sau cùng, nếu có một điều gì đó tôi muốn bạn nhận được từ toàn bộ styleguide này, đó chính là **Sass nên được giữ đơn giản nhất có thể**.

Nhờ những thử nghiệm ngớ ngẩn của tôi như [bitwise operators](https://github.com/HugoGiraudel/SassyBitwise), [iterators and generators](https://github.com/HugoGiraudel/SassyIteratorsGenerators) và [a JSON parser](https://github.com/HugoGiraudel/SassyJSON) trong Sass, tất cả chúng ta đều biết rõ những gì người ta có thể làm với bộ tiền xử lý này.

Trong khi đó, CSS là một ngôn ngữ đơn giản. Sass, được tạo ra để viết CSS, không nên phức tạp hơn nhiều so với CSS thông thường. [KISS principle](http://en.wikipedia.org/wiki/KISS_principle) (Giữ nó đơn giản đến mức ngu ngốc) là chìa khoá ở đây và thậm chí có thể được ưu tiên hơn [DRY principle](http://en.wikipedia.org/wiki/Don't_repeat_yourself) (Đừng lặp lại chính mình) trong một số trường hợp.

Đôi khi, tốt hơn hết là nên lặp lại một chút để giữ cho code có thể duy trì được, thay vì xây dựng một hệ thống phức tạp nặng về, khó sử dụng, sự phức tạp không cần thiết vì nó quà phức tạp.

Ngoài ra, để tôi trích dẫn [Harry Roberts](https://csswizardry.com/) lại một lần nữa, **chủ nghĩ thực dụng hơn hẳn sự hoàn hảo**. Tại một số điểm, bạn có thể sẽ thấy mình đi ngược lại các quy tắc được mô tả ở đây. Nếu nó có ý nghĩa, nếu cảm thấy đúng, làm điều đó. Code chỉ là một phương tiện, không phải là tất cả.

### *Mở rộng Guidelines*

Một phần lớn của styleguide này được đánh giá cao. Tôi đã đọc và viết Sass trong vài năm nay, đến mức bây giờ tôi có rất nhiều nguyên tắc khi viết các stylesheet một cách sạch sẽ. Tôi hiểu rằng nó có thể không làm hài lòng cũng không phù hợp với tất cả mọi người, và điều này là hoàn toàn bình thường.

Mặc dù, tôi tin rằng các hướng dẫn được thực hiện để được mở rộng. Việc mở rộng Sass Guideline có thể đơn giản như việc có một tài liệu nói rằng code đang tuân theo các nguyên tắc từ styleguide kiểu này ngoại trừ một vài thứ; trong trường hợp đó, các quy tắc cụ thể sẽ được giải thích bên dưới.

Một ví dụ về tiện ích mở rộng styleguide có thể được tìm thấy trên [SassDoc repository](https://github.com/SassDoc/sassdoc/blob/master/GUIDELINES.md):

> Đây là một phần mở rộng cho [Node Styleguide](https://github.com/felixge/node-style-guide) của Felix Geisendörfer. Bất cứ điều gì từ tài liệu này đều ghi đè lên những gì có thể được nói trong Node Styleguide.

## Syntax & Formatting

Nếu bạn hỏi tôi, chắc chắn điều đầu tiên mà một styleguide nên làm là mô tả cách chúng ta muốn code của mình trông như thế nào.

Khi nhiều developer tham gia viết CSS trên cùng một dự án, vấn đề chỉ còn là thời gian trước khi một trong số họ bắt đầu thực hiện mọi thứ theo cách riêng của họ. Các nguyên tắc code thúc đẩy tính nhất quán không chỉ ngăn chặn điều này mà còn giúp ích khi đọc và cập nhật code.

Một cách áp đặt, chúng ta sẽ muốn (lấy cảm hứng bởi [CSS Guidelines](http://cssguidelin.es/#syntax-and-formatting)):

- Hai (2) khoảng trắng để thụt lề, không có tab;
- Mỗi dòng không quá 80 ký tự;
- Viết CSS trên nhiều dòng một cách đúng đắn;
- Sử dụng khoảng trắng một cách ý nghĩa.

```scss
// Yep
.foo {
  display: block;
  overflow: hidden;
  padding: 0 1em;
}

// Nope
.foo {
    display: block; overflow: hidden;

    padding: 0 1em;
}
```

### *Strings*

Dù bạn có tin hay không, chuỗi đóng vai trò khá lớn trong cả hệ sinh thái CSS và Sass. Hầu hết các giá trị CSS là độ dài hoặc số nhận dạng, vì vậy thực sự rất quan trọng để tuân theo một số nguyên tắc khi xử lý chuỗi trong Sass.

###### ENDCODING

Để tránh bất kỳ vấn đề tiềm ẩn nào với mã hoá ký tự (endcoding), thật sự nên đặt bắt buộc mã hoá [UTF-8](http://en.wikipedia.org/wiki/UTF-8) bên trong [main stylesheet](https://sass-guidelin.es/#main-file) sử dụng chỉ thị `@charset`. Hãy chắc chắn rằng đó là yếu tố đầu tiên của stylesheet và không có bất kỳ ký tự nào trước nó.

```scss
@charset 'utf-8';
```

###### QUOTES

CSS không yêu cầu các chuỗi được trích dẫn (quote), ngay cả những chuỗi chứa khoảng trắng. Lấy tên font-family chẳng hạn: không vấn đề gì nếu bạn bọc chúng trong dấu ngoặc kép cho trình phân tích cú pháp CSS.

Chính vì điều này, Sass *cũng* không yêu cầu trích dẫn các chuỗi. Thậm chí tốt hơn (và *may mắn là*, bạn sẽ thừa nhận), một chuỗi được trích dẫn hoàn toàn tương đương với chính nó khi không được trích dẫn (ví dụ: `'abc'` hoàn toàn tương đương với `abc`).

Vẫn là vấn đề đó, các ngôn ngữ không yêu cầu chuỗi được trích dẫn chắc chắn là thiểu số và bởi vậy **chuỗi phải luôn được đặt trong dấu nháy đơn** (`'`) trong Sass (dấu nháy đơn dễ gõ hơn gấp đôi trên bàn phím *qwerty*). Bên cạnh tính nhất quán với các ngôn ngữ khác, bao gồm Javascript, có một số lý do cho sự lựa chọn này:

- Tên màu được coi là màu khi không được trích dẫn, có thể dẫn đến các vấn đề nghiêm trọng;
- Hầu hết các công cụ highlight cú pháp sẽ bị chói trên các chuỗi không được trích dẫn;
- Nó giúp dễ đọc;
- Chẳng có lý do nào để không trích dẫn chuỗi.

```scss
// Yep
$direction: 'left';

// Nope
$direction: left;
```

<blockquote class="note"><p>Theo đặc tả CSS, chỉ thị <code>@charset</code> phải được khai báo trong dấu nháy kép để <a href="http://www.w3.org/TR/css3-syntax/#charset-rule">được coi là hợp lệ</a>. Tuy nhiên, Sass quan tâm đến điều này khi biên dịch sang CSS để nguyên tắc này không có tác động đến kết quả cuối cùng, ngay cả đối với <code>@charset</code>.</p></blockquote>

###### STRINGS AS CSS VALUE

Các giá trị CSS cụ thể (mã địch danh) như `initial` hoặc `sans-serif` yêu cầu không được trích dẫn. Thật vậy, khai báo `font-family: 'sans-serif'` sẽ âm thầm thất bại vì CSS đang mong đợi một mã định danh, không phải là một chuỗi trích dẫn. Vì điều này, chúng tôi không trích dẫn những giá trị đó.

```scss
// Yep
$font-type: sans-serif;

// Nope
$font-type: 'sans-serif';

// Okay I guess
$font-type: unquote('sans-serif');
```

Do đó, ta có thể phân biệt giữa các chuỗi dự định được sử dụng làm giá trị CSS (số nhận dạng CSS) như trong ví dụ trước và chuỗi khi dính vào loại dữ liệu Sass, ví dụ như các map key.

###### STRINGS CONTAINING QUOTES

Nếu một chuỗi chứa một hoặc một vài dấu nháy đơn, người ta có thể xem xét việc bọc chuỗi bằng dấu nháy kép ( " ) thay vào đó, để tránh mất các ký tự trong chuỗi.

```scss
// Okay
@warn 'You can\'t do that.';

// Okay
@warn "You can't do that.";
```

###### URLS

```scss
// Yep
.foo {
  background-image: url('/images/kittens.jpg');
}

// Nope
.foo {
  background-image: url(/images/kittens.jpg);
}
```

### *NUMBERS*

Trong Sass, số là một loại dữ liệu bao gồm mọi thứ, từ số đơn vị đến độ dài, thời lượng, tần số, góc và hơn thế nữa. Điều này cho phép tính toán được chạy trên các biện pháp như vậy.

###### ZEROS

Các số sẽ hiển thị số 0 đứng đầu trước một giá trị thập phân nhỏ hơn 1. Không bao giờ chỉ hiển thị số đó.

```scss
// Yep
.foo {
  padding: 2em;
  opacity: 0.5;
}

// Nope
.foo {
  padding: 2.0em;
  opacity: .5;
}
```

<blockquote class="note"><p>Trong Sublime Text và các trình soạn thảo khác cung cấp việc search và replace biểu thứ chính quy, rất dễ dàng để thêm một số 0 đứng đầu. Chỉ cần thay thế <code>\s+\.(\d+)</code> bằng <code>\ 0.$1</code>. Đừng quên khoảng trống trước <code>0</code>.</p></blockquote>

###### UNITS

Khi xử lý độ dài, giá trị `0` sẽ không bao giờ có đơn vị.

```scss
// Yep
$length: 0;

// Nope
$length: 0em;
```

<blockquote class="note"><p>Hãy cẩn thận, ví dụ này chỉ nên giới hạn về độ dài. Không có đơn vị cho 0 ở một thuộc tính thời gian như <code>transition-delay</code> là không được phép. Về mặt lý thuyết, nếu một số 0 đơn vị được chỉ định trong một khoảng thời gian, khai báo được coi là không hợp lệ và cần được loại bỏ. Không phải tất cả các trình duyệt đều nghiêm ngặt, ngoài một vài trong số đó. Tóm gọn vấn đề: chỉ bỏ qua đơn vị cho độ dài.</p></blockquote>

Lỗi phổ biến nhất tôi có thể nói về các con số trong Sass là nghĩ rằng các đơn vị chỉ là một vài chuỗi có thể được nối một cách an toàn vào một số. Trong khi điều đó nghe có vẻ  đúng nhưng thật sự đó chắc chắn không phải là cách các đơn vị làm việc. Hãy nghĩ về các đơn vị như các ký tự đại số. Chẳng hạn, trong thế giới thực, nhân 5 inch với 5 inch cho bạn 25 inch vuông. Logic tương tự áp dụng cho Sass.

Để thêm một đơn vị vào một số, bạn phải nhân số này với *1 đơn vị*.

```scss
$value: 42;

// Yep
$length: $value * 1px;

// Nope
$length: $value + px;
```

Lưu ý rằng việc thêm *0 vào đơn vị đó* cũng hoạt động, nhưng tôi muốn giới thiệu phương pháp đã nói ở trên vì việc thêm *0 đơn vị* có thể hơi khó hiểu. Thật vậy, khi cố gắng chuyển đổi một số sang một đơn vị tương thích khác, việc thêm 0 sẽ không thực hiện được. Đọc thêm về điều đó [trong bài viết này](http://css-tricks.com/snippets/sass/correctly-adding-unit-number/).

```scss
$value: 42 + 0px;
// -> 42px

$value: 1in + 0px;
// -> 1in

$value: 0px + 1in;
// -> 96px
```

Sau cùng, nó thực sự phụ thuộc vào những gì bạn đang cố gắng để đạt được. Chỉ cần lưu ý rằng việc thêm đơn vị dưới dạng chuỗi không phải là một cách tốt nhất để tiến hành.

Để xoá đơn vị của một giá trị, bạn phải chia nó cho *một đơn vị thuộc cùng loại*.

```scss
$length: 42px;

// Yep
$value: $length / 1px;

// Nope
$value: str-slice($length + unquote(''), 1, 2);
```

Việc thêm một đơn vị dưới dạng một chuỗi vào một số dẫn đến một chuỗi, ngăn chặn mọi hoạt động bổ sung trên giá trị. Cắt phần số của một số bằng một đơn vị cũng dẫn đến một chuỗi. Đây không phải điều bạn mong muốn. [Sử dụng độ dài, thay vì chuỗi](http://hugogiraudel.com/2013/09/03/use-lengths-not-strings/).

###### CALCULATIONS

**Các phép tính số cấp cao nhất phải luôn được bọc trong ngoặc đơn**. Yêu cầu này không chỉ cải thiện đáng kể khả năng đọc, nó còn ngăn chặn một số trường hợp ưu tiên bằng cách buộc Sass phải đánh giá nội dung của dấu ngoặc đơn.

```scss
// Yep
.foo {
  width: (100% / 3);
}

// Nope
.foo {
  width: 100% / 3;
}
```

###### MAGIC NUMBERS

“Magic number” là một thuật ngữ [old school programming](http://en.wikipedia.org/wiki/Magic_number_(programming)#Unnamed_numerical_constants) dành cho *những hằng số không được đặt tên*. Về cơ bản, nó chỉ là một số ngẫu nhiên xảy ra với  *just work*™ mà không bị ràng buộc bởi bất kỳ lời giải thích hợp lý nào.

Không cần phải nói **magic number là một "bệnh dịch" và nên tránh bằng mọi giá**. Khi bạn không thể quản lý để tìm một lời giải thích hợp lý cho lý do tại sao một số tồn tại và hoạt động như thế nào, hãy thêm một nhận xét mở rộng giải thích cách bạn dùng nó và tại sao bạn nghĩ rằng nó hoạt động. Việc thừa nhận bạn không biết tại sao một cái gì đó hoạt động vẫn hữu ích hơn cho các developer tiếp theo hơn là họ phải tìm hiểu những gì diễn ra từ đầu

```scss
/**
 * 1. Magic number. This value is the lowest I could find to align the top of
 * `.foo` with its parent. Ideally, we should fix it properly.
 */
.foo {
  top: 0.327em; /* 1 */
}
```

Về chủ đề này, CSS-Tricks có [một bài viết tuyệt vời](http://css-tricks.com/magic-numbers-in-css/) về các magic number trong CSS mà tôi khuyến khích các bạn nên đọc nó.

### *Colors*

Màu sắc chiếm một vị trí quan trọng trong CSS. Đương nhiên, Sass trở nên hữu ích khi thao túng màu sắc, chủ yếu bằng cách cung cấp một số [powerful functions](http://sass-lang.com/documentation/Sass/Script/Functions.html).

Sass rất hữu ích khi xử lý màu sắc mà các bài viết đã phát triển mạnh mẽ trên Internet về chính chủ đề này. Tôi sẽ giới thiệu một vài bài đọc:

- [How to Programmatically Go From One Color to Another](http://thesassway.com/advanced/how-to-programtically-go-from-one-color-to-another-in-sass)
- [Using Sass to Build Color Palettes](http://www.sitepoint.com/using-sass-build-color-palettes/)
- [Dealing with Color Schemes in Sass](http://www.sitepoint.com/dealing-color-schemes-sass/)

###### COLOR FORMATS

Để làm cho màu sắc đơn giản nhất có thể, lời khuyên của tôi là hãy tôn trọng thứ tự ưu tiên sau đây cho các định dạng màu:

1. [HSL notation](http://en.wikipedia.org/wiki/HSL_and_HSV);
2. [RGB notation](http://en.wikipedia.org/wiki/RGB_color_model);
3. Hexadecimal notation (chữ thường và viết tắt).

Từ khóa CSS color không nên được sử dụng, trừ khi tạo mẫu nhanh. Thật vậy, chúng là những từ tiếng Anh và một trong số chúng hoạt động khá tệ trong việc mô tả màu sắc mà chúng đại diện, đặc biệt là đối với những người không phải là người bản xứ. Trên hết, các từ khóa không phải là ngữ nghĩa hoàn hảo; ví dụ `grey` thực sự tối hơn` darkgrey` và sự nhầm lẫn giữa` grey` và` gray` có thể dẫn đến việc sử dụng màu sắc không nhất quán này.

Đại diện HSL không chỉ dễ hiểu nhất đối với bộ não con người [cần dẫn nguồn], nó còn giúp những người viết stylesheet dễ dàng điều chỉnh màu sắc bằng cách điều chỉnh sắc thái, độ bão hòa và độ sáng riêng lẻ.

RGB vẫn có lợi ích hiển thị ngay lập tức nếu màu sắc nhiều hơn màu xanh lam, xanh lục hoặc đỏ. Do đó, nó có thể tốt hơn HSL trong một số tình huống, đặc biệt là khi mô tả màu đỏ, xanh lá cây hoặc xanh lam thuần khiết. Mặc dù không làm cho nó dễ dàng để xây dựng một màu từ ba phần.

Cuối cùng, thập lục phân gần với không thể giải mã được cho tâm trí con người. Sử dụng nó chỉ là phương sách cuối cùng nếu bạn bắt buộc phải làm vậy.

```scss
// Yep
.foo {
  color: hsl(0, 100%, 50%);
}

// Also yep
.foo {
  color: rgb(255, 0, 0);
}

// Meh
.foo {
  color: #f00;
}

// Nope
.foo {
  color: #FF0000;
}

// Nope
.foo {
  color: red;
}
```

Khi sử dụng ký hiệu HSL hoặc RGB, luôn luôn thêm một khoảng trắng sau dấu phẩy (`,`) và không có khoảng trắng giữa dấu ngoặc đơn (`(`, `)`) và nội dung.

```scss
// Yep
.foo {
  color: rgba(0, 0, 0, 0.1);
  background: hsl(300, 100%, 100%);
}

// Nope
.foo {
  color: rgba(0,0,0,0.1);
  background: hsl( 300, 100%, 100% );
}
```

###### COLORS AND VARIABLES

Khi sử dụng một màu nhiều lần, lưu trữ nó trong một biến có tên có ý nghĩa đại diện cho màu.

```scss
$sass-pink: hsl(330, 50%, 60%);
```

Bây giờ bạn có thể tự do sử dụng biến này bất cứ nơi nào bạn muốn. Tuy nhiên, nếu việc sử dụng của bạn được liên kết chặt chẽ với một theme, tôi sẽ khuyên bạn không nên sử dụng biến như hiện tại. Thay vào đó, lưu trữ nó trong một biến khác với một tên giải thích cách sử dụng nó.

```scss
$main-theme-color: $sass-pink;
```

Làm điều này sẽ ngăn việc thay đổi theme tạo ra một cái gì đó như `$sass-Pink: blue`. [Bài viết này](http://davidwalsh.name/sass-color-variables-dont-suck) thực hiện tốt để giải thích lý do tại sao đặt tên biến ý nghĩa cho màu của bạn là quan trọng.

###### LIGHTENING AND DARKENING COLORS

Cả hàm [`lighten`](http://sass-lang.com/documentation/Sass/Script/Fiances.html#lighten-instance_method) và [` darken`](http://sass-lang.com/documentation/ Các hàm Sass / Script / Function.html # darken-instance_method) đều điều khiển độ sáng của màu trong không gian HSL bằng cách thêm hoặc bớt đi độ sáng trong không gian HSL. Về cơ bản, chúng không là gì ngoài các bí danh cho tham số `$lightness` của hàm [`adjust-color`](http://sass-lang.com/documentation/Sass/Script/Fiances.html#adjust_color-instance_method).

Vấn đề là, những chức năng đó thường không cung cấp kết quả như mong đợi. Mặt khác, hàm [`mix`](http://sass-lang.com/documentation/Sass/Script/Fiances.html#mix-instance_method) là một cách hay để làm sáng hoặc làm tối màu bằng cách trộn nó với `white` hoặc `black`.

Lợi ích của việc sử dụng `mix` thay vì một trong hai chức năng đã nói ở trên là nó sẽ dần dần chuyển sang màu đen (hoặc trắng) khi bạn giảm tỷ lệ màu, trong khi` darken` và` lighten` sẽ nhanh chóng làm mất màu tất cả các con đường tạo ra black hoặc white.

<figure role="group" style="text-align: center"> <img data-proofer-ignore="" alt="Illustration of the difference between lighten/darken and mix by KatieK " sizes="100vw" srcset="https://d33wubrfki0l68.cloudfront.net/0e167d952ec2ef84b901bbd9359fe0f435df731d/ab9d2/assets/images/lighten-darken-mix_small.png 540w, https://d33wubrfki0l68.cloudfront.net/2823b2267df2e182238c6a7b794e686091e479b8/10273/assets/images/lighten-darken-mix_medium.png 900w, https://d33wubrfki0l68.cloudfront.net/647b61db27c04e41d5ceaadacf7b32c8fc340a76/1d675/assets/images/lighten-darken-mix_large.png 1200w, https://d33wubrfki0l68.cloudfront.net/61202ec6c279f628010a14f25445ce99a0004f5e/9d157/assets/images/lighten-darken-mix_huge.png 1590w"><figcaption>Minh hoạ về sự khác biệt giữa <code class="highlighter-rouge">lighten</code>/<code class="highlighter-rouge">darken</code> và <code class="highlighter-rouge">mix</code> bởi <a href="http://codepen.io/KatieK2/pen/tejhz/">KatieK</a></figcaption></figure>

Nếu bạn không muốn viết hàm `mix` nhiều lần, bạn có thể tạo ra hai hàm dễ sử dụng `tint` và `shade` (cũng là một phần của [Compass](http://compass-style.org/reference/compass/helpers/colors/#shade)) để làm điều tương tự.

```scss
/// Slightly lighten a color
/// @access public
/// @param {Color} $color - color to tint
/// @param {Number} $percentage - percentage of `$color` in returned color
/// @return {Color}
@function tint($color, $percentage) {
  @return mix(white, $color, $percentage);
}

/// Slightly darken a color
/// @access public
/// @param {Color} $color - color to shade
/// @param {Number} $percentage - percentage of `$color` in returned color
/// @return {Color}
@function shade($color, $percentage) {
  @return mix(black, $color, $percentage);
}
```

<blockquote class="note"><p>Hàm <a href="http://sass-lang.com/documentation/Sass/Script/Functions.html#scale_color-instance_method"><code>scale-color</code></a> được thiết kế để chia tỷ lệ các thuộc tính dễ dàng hơn bằng cách tính đến mức độ cao hay thấp của chúng. Nó sẽ cung cấp kết quả tốt như <code>mix</code> nhưng với quy ước rõ ràng hơn. Mặc dù các yếu tố tỷ lệ là hoàn toàn giống nhau.</p></blockquote>

### *Lists*

Lists trong Sass tương đương với array. list là một cấu trúc dữ liệu phẳng (không giống như [map](https://sass-guidelin.es/#maps)) nhằm lưu trữ các giá trị thuộc bất kỳ loại nào (bao gồm cả list, hay nested list)

Lists cần tôn trọng các nguyên tắc sau:

- Hoặc nội tuyến hoặc đa dòng;
- Nhất thiết phải trên đa dòng nếu quá dài để phù hợp với dòng 80 ký tự;
- Luôn được phân tách bằng dấu phẩy, trừ khi được sử dụng cho mục đích CSS;
- Luôn được gói trong ngoặc đơn;
- Phải có dấu phẩy cuối nếu trên đa dòng, không cần nếu là nội tuyến.

```scss
// Yep
$font-stack: ('Helvetica', 'Arial', sans-serif);

// Yep
$font-stack: (
  'Helvetica',
  'Arial',
  sans-serif,
);

// Nope
$font-stack: 'Helvetica' 'Arial' sans-serif;

// Nope
$font-stack: 'Helvetica', 'Arial', sans-serif;

// Nope
$font-stack: ('Helvetica', 'Arial', sans-serif,);
```

Khi thêm các mục mới vào list, luôn sử dụng API được cung cấp. Đừng cố thêm các mục mới bằng tay.

```scss
$shadows: (0 42px 13.37px hotpink);

// Yep
$shadows: append($shadows, $shadow, comma);

// Nope
$shadows: $shadows, $shadow;
```

Trong [bài viết này](http://hugogiraudel.com/2013/07/15/understanding-sass-lists/), tôi có thử qua rất nhiều thủ thuật và mẹo để xử lý và thao tác list chính xác trong Sass.

### *Maps*

Với Sass, những người viết stylesheet có thể định nghĩa các map - thuật ngữ Sass cho các associative array, hash hoặc thậm chí các JavaScript object. Map là cấu trúc dữ liệu liên kết các khóa với các giá trị. Cả khóa và giá trị có thể thuộc bất kỳ loại dữ liệu nào, kể cả map mặc dù tôi không khuyến nghị sử dụng các loại dữ liệu phức tạp làm khóa của map, nếu chỉ vì mục đích chuẩn mực.

Map nên được viết như sau:

- Space sau dấu hai chấm (`:`);
- Dấu ngoặc mở (`(`) trên cùng dòng với dấu hai chấm (`:`);
- **Các khóa được trích dẫn** nếu chúng là các chuỗi (đại diện cho 99% các trường hợp);
- Mỗi cặp khóa / giá trị trên dòng mới của chính nó;
- Dấu phẩy (`,`) ở cuối mỗi khóa / giá trị;
- **Dấu phẩy cuối** (`,`) trên mục cuối cùng để dễ dàng thêm, xóa hoặc sắp xếp lại các mục;
- Dấu đóng dấu ngoặc (`)`) trên dòng mới của chính nó;
- Không có khoảng trắng hoặc dòng mới giữa dấu ngoặc nhọn (`)`) và dấu chấm phẩy (`;`).

Minh họa:

```scss
// Yep
$breakpoints: (
  'small': 767px,
  'medium': 992px,
  'large': 1200px,
);

// Nope
$breakpoints: ( small: 767px, medium: 992px, large: 1200px );
```

Các bài viết về Map Sass được đưa ra thường xuyên cho tính năng này. Dưới đây là 3 bài tôi khuyên bạn nên đọc: [Using Sass Maps](http://www.sitepoint.com/using-sass-maps/), [Extra Map functions in Sass](http://www.sitepoint.com/extra-map-functions-sass/), [Real Sass, Real Maps](http://blog.grayghostvisuals.com/sass/real-sass-real-maps/).

### CSS Ruleset

Tại thời điểm này, điều này chủ yếu là sửa đổi những gì mọi người biết, nhưng đây là cách viết một quy tắc CSS (ít nhất là theo hầu hết các hướng dẫn, nó bao gồm [CSS Guidelines](http://cssguidelin.es/#anatomy-of-a-ruleset)):

- Các selector liên quan trên cùng một dòng; selector không liên quan trên các dòng mới;
- Dấu ngoặc mở (`{`) cách nhau từ selector cuối cùng bởi một khoảng trắng;
- Mỗi thuộc tính trên dòng mới của riêng mình;
- Một khoảng trắng sau dấu hai chấm (`:`);
- Dấu chấm phẩy (`;`) ở cuối tất cả các khai báo;
- Dấu ngoặc nhọn (`}`) trên dòng mới của chính nó;
- Một dòng mới sau dấu ngoặc đóng `}`.

Minh họa:

```scss
// Yep
.foo, .foo-bar,
.baz {
  display: block;
  overflow: hidden;
  margin: 0 auto;
}

// Nope
.foo,
.foo-bar, .baz {
    display: block;
    overflow: hidden;
    margin: 0 auto }
```

Thêm vào các hướng dẫn liên quan đến CSS, tôi muốn chú ý đến:

- Các biến cục bộ được khai báo trước bất kỳ khai báo nào, sau đó cách nhau từ các khai báo bằng một dòng mới;
- Các lần gọi mixin không có `@content` đến trước bất kỳ thuộc tính nào;
- Selector lồng nhau luôn đến sau một dòng mới;
- Mixin gọi với `@content` đến sau bất kỳ selector lồng nhau nào;
- Không có dòng mới trước dấu ngoặc nhọn (`}`).

Minh họa:

```scss
.foo, .foo-bar,
.baz {
  $length: 42em;

  @include ellipsis;
  @include size($length);
  display: block;
  overflow: hidden;
  margin: 0 auto;

  &:hover {
    color: red;
  }

  @include respond-to('small') {
    overflow: visible;
  }
}
```

### *Declaration Sorting*

Tôi không thể nghĩ ra nhiều chủ đề trong đó các ý kiến được phân chia như chúng liên quan đến việc sắp xếp khai báo trong CSS. Cụ thể, có hai trường phái ở đây:

- Bám sát thứ tự chữ cái;
- Khai báo thứ tự theo loại (vị trí, hiển thị, màu sắc, phông chữ, linh tinh).

Có những ưu và nhược điểm cho cả hai cách. Một mặt, thứ tự chữ cái là phổ quát (ít nhất là đối với các ngôn ngữ sử dụng bảng chữ cái Latinh) vì vậy không có tranh luận về việc sắp xếp một thuộc tính này trước một thuộc tính khác. Tuy nhiên, nó có vẻ cực kỳ kỳ lạ đối với tôi khi thấy các thuộc tính như `bottom` và` top` không nằm ngay cạnh nhau. Tại sao hình ảnh động nên xuất hiện trước loại màn hình? Có rất nhiều điều kỳ lạ với thứ tự chữ cái.

```scss
.foo {
  background: black;
  bottom: 0;
  color: white;
  font-weight: bold;
  font-size: 1.5em;
  height: 100px;
  overflow: hidden;
  position: absolute;
  right: 0;
  width: 100px;
}
```

Mặt khác, sắp xếp các thuộc tính theo loại có ý nghĩa hoàn hảo. Mỗi khai báo liên quan đến phông chữ được thu thập, `top` và` bottom` được hợp nhất và đọc một loại quy tắc cảm giác giống như đọc một câu chuyện ngắn. Nhưng trừ khi bạn tuân theo một số quy ước như [Idiomatic CSS](https://github.com/necolas/idiomatic-css), có rất nhiều chỗ để diễn giải theo cách làm việc này. `white-space` sẽ đi đâu: phông chữ hoặc display? Trường hợp nào `overflow` chính xác? Thứ tự thuộc tính trong một nhóm (nó có thể được sắp xếp theo thứ tự abc, ôi thật trớ trêu)?

```scss
.foo {
  height: 100px;
  width: 100px;
  overflow: hidden;
  position: absolute;
  bottom: 0;
  right: 0;
  background: black;
  color: white;
  font-weight: bold;
  font-size: 1.5em;
}
```

Ngoài ra còn có một loại cây con thú vị khác về thứ tự thuộc tính được gọi là [Concentric CSS](https://github.com/brandon-rhodes/Concentric-CSS), dường như cũng khá phổ biến. Về cơ bản, CSS tập trung dựa vào box-model để xác định thứ tự: bắt đầu bên ngoài, di chuyển vào trong.

```scss
.foo {
  width: 100px;
  height: 100px;
  position: absolute;
  right: 0;
  bottom: 0;
  background: black;
  overflow: hidden;
  color: white;
  font-weight: bold;
  font-size: 1.5em;
}
```

Tôi phải nói rằng tôi không thể tự quyết định. Một [cuộc thăm dò gần đây về CSS-Tricks](http://css-tricks.com/poll-results-how-do-you-order-your-css-properties/) đã xác định rằng hơn 45% developer đặt hàng khai báo theo loại chống lại 14% theo thứ tự abc. Ngoài ra, có 39% hoàn toàn ngẫu nhiên, bao gồm cả bản thân tôi.

<figure role="group" style="text-align: center"> <img width="700" height="308" alt="Chart showing how developers order their CSS declarations " src="https://d33wubrfki0l68.cloudfront.net/189c15208fdc614be2ca324c26ec14350f591a30/56132/assets/images/css-order-chart.png"><figcaption>Biểu đồ cho thấy cách các developer đặt hàng khai báo CSS của họ</figcaption></figure>

Because of this, I will not impose a choice in this styleguide. Pick the one you prefer, as long as you are consistent throughout your stylesheets (i.e. not the *random* option).

Chính vì điều này, tôi sẽ không áp đặt một sự lựa chọn trong styleguide này. Chọn cái bạn thích, miễn là bạn nhất quán trong suốt stylesheet của mình (nghĩa là không phải tùy chọn *ngẫu nhiên*).

<blockquote class="note"><p>Một <a href="http://peteschuster.com/2014/12/reduce-file-size-css-sorting/">nghiên cứu gần đây</a> cho thấy rằng sử dụng <a href="https://github.com/csscomb/csscomb.js">CSS Comb</a> (Sử dụng <a href="https://github.com/csscomb/csscomb.js/blob/master/config/csscomb.json">thứ tự kiểu</a>) để sắp xếp các khai báo CSS kết thúc việc rút ngắn kích thước tệp trung bình theo nén Gzip xuống 2,7%, so với 1,3% khi sắp xếp theo thứ tự bảng chữ cái.</p></blockquote>

### *Selector Nesting*

Một tính năng đặc biệt mà Sass cung cấp đang bị nhiều developer sử dụng quá mức là *selector lồng nhau*. Selector lồng nhau cung cấp một cách để những người viết stylesheet tính toán các selector dài bằng cách lồng các selector ngắn hơn trong nhau.

###### GENERAL RULE

Ví dụ, selector lồng nhau sau:

```scss
.foo {
  .bar {
    &:hover {
      color: red;
    }
  }
}
```

… sẽ tạo ra CSS trông như này:

```css
.foo .bar:hover {
  color: red;
}
```

Dọc theo cùng một dòng, kể từ Sass 3.3 ta có thể sử dụng tham chiếu selector hiện tại (`&`) để tạo các selector nâng cao. Ví dụ:

```scss
.foo {
  &-bar {
    color: red;
  }
}
```

… sẽ tạo ra CSS trông như này:

```scss
.foo-bar {
  color: red;
}
```

Phương pháp này thường được sử dụng cùng với [BEM naming conventions](http://csswizardry.com/2013/01/mindbemding-getting-your-head-round-bem-syntax/) để tạo ra `.block__element` và `.block--modifier` selector dựa trên selector ban đầu (i.e. `.block` trong trường hợp này).

<blockquote class="note"><p>Mặc dù có thể là chuyện nhỏ, việc tạo ra các selectors từ các tham chiếu selector hiện tại (<code>&amp;</code>) làm cho các selector đó không thể tìm kiếm được trong codebase vì chúng không tồn tại trên mỗi se.</p></blockquote>

Vấn đề với selector lồng nhau là cuối cùng nó làm cho code khó đọc hơn. Người ta phải tính toán nhẩm selector kết quả ra khỏi các mức indent; không phải lúc nào cũng rõ ràng CSS sẽ là gì.

Câu lệnh này trở nên chính xác hơn khi các selector dài hơn và các tham chiếu đến selector hiện tại (`&`) thường xuyên hơn. Đến một lúc nào đó, nguy cơ mất dấu vết và không thể hiểu được những gì đang diễn ra nữa là quá cao đến mức không đáng.

Để ngăn chặn những tình huống như vậy, chúng tôi đã nói rất nhiều về [the Inception rule](http://thesassway.com/beginner/the-inception-rule) vài năm trước. Nó khuyên rằng không nên làm lồng sâu hơn 3 cấp độ, như một tài liệu tham khảo cho bộ phim Inception từ Christopher Nolan. Tôi sẽ quyết liệt hơn và khuyên bạn nên **tránh việc chọn lồng nhau càng nhiều càng tốt**.

Mặc dù rõ ràng có một vài ngoại lệ cho quy tắc này như chúng ta sẽ thấy trong phần tiếp theo, ý kiến này dường như khá phổ biến. Bạn có thể đọc chi tiết hơn về nó trong  [Beware of Selector Nesting](http://www.sitepoint.com/beware-selector-nesting-sass/) và [Avoid nested selectors for more modular CSS](http://thesassway.com/intermediate/avoid-nested-selectors-for-more-modular-css).

###### EXCEPTIONS

Đối với người mới bắt đầu, nó được phép và thậm chí được khuyến nghị lồng các lớp giả và các phần tử giả trong selector ban đầu.

```scss
.foo {
  color: red;

  &:hover {
    color: green;
  }

  &::before {
    content: 'pseudo-element';
  }
}
```

Sử dụng selector lồng nhau cho các lớp giả và các phần tử giả không chỉ có ý nghĩa (vì nó liên quan đến các selector liên quan chặt chẽ), nó còn giúp giữ mọi thứ về một thành phần ở cùng một vị trí.

Ngoài ra, khi sử dụng các lớp trạng thái không biết thành phần như `.is-active`, việc lồng nó dưới selector thành phần để giữ mọi thứ gọn gàng là điều hoàn toàn tốt.

```scss
.foo {
  // …

  &.is-active {
    font-weight: bold;
  }
}
```

Cuối cùng nhưng không kém phần quan trọng, khi tạo kiểu cho một element vì nó được chứa trong một element cụ thể khác, cũng tốt khi sử dụng lồng nhau để giữ mọi thứ về thành phần đó ở cùng một vị trí.

```scss
.foo {
  // …

  .no-opacity & {
    display: none;
  }
}
```

Như với tất cả mọi thứ, các chi tiết cụ thể có phần không liên quan, tính nhất quán chính là chìa khóa. Nếu bạn cảm thấy hoàn toàn tự tin với selector lồng nhau, hãy sử dụng selector lồng nhau. Chỉ cần chắc chắn rằng toàn bộ team của bạn hoàn toàn ổn với điều đó.

## Naming Conventions

In this section, we will not deal with the best CSS naming conventions for maintainability and scale; not only is that up to you, it’s also out of the scope of a Sass styleguide. I suggest those recommended by [CSS Guidelines](http://cssguidelin.es/#naming-conventions).

There are a few things you can name in Sass, and it is important to name them well so the whole code base looks both consistent and easy to read:

- variables;
- functions;
- mixins.

Sass placeholders are deliberately omitted from this list since they can be considered as regular CSS selectors, thus following the same naming pattern as classes.

Regarding variables, functions and mixins, we stick to something very *CSS-y*: **lowercase hyphen-delimited**, and above all meaningful.

```scss
$vertical-rhythm-baseline: 1.5rem;

@mixin size($width, $height: $width) {
  // …
}

@function opposite-direction($direction) {
  // …
}
```

### *Constants*

If you happen to be a framework developer or library writer, you might find yourself dealing with variables that are not meant to be updated in any circumstances: constants. Unfortunately (or fortunately?), Sass does not provide any way to define such entities, so we have to stick to strict naming conventions to make our point.

As for many languages, I suggest all-caps snakerized variables when they are constants. Not only is this a very old convention, but it also contrasts well with usual lowercased hyphenated variables.

```scss
// Yep
$CSS_POSITIONS: (top, right, bottom, left, center);

// Nope
$css-positions: (top, right, bottom, left, center);
```

If you really want to play with the ideas of constants in Sass, you should read [this dedicated article](http://www.sitepoint.com/dealing-constants-sass/).

### *Namespace*

If you intend to distribute your Sass code, in the case of a library, a framework, a grid system or whatever, you might want to consider namespacing all your variables, functions, mixins and placeholders so it does not conflict with anyone else’s code.

For instance, if you work on a *Sassy Unicorn* project that is meant to be distributed, you could consider using `su-` as a namespace. It is specific enough to prevent any naming collisions and short enough not to be a pain to write.

```scss
$su-configuration: ( … );

@function su-rainbow($unicorn) {
  // …
}
```

[Kaelig](http://kaelig.fr/) has [a very insightful article about the global CSS namespace](http://blog.kaelig.fr/post/44554267597/please-respect-the-global-css-namespace), in case this topic is of any interest to you.

<blockquote class="note"><p>Note that automatic namespacing is definitely a design goal for the upcoming <code>@import</code> revamp from Sass 4.0. As that comes closer to fruition, it will become less and less useful to do manual namespacing; eventually, manually namespaced libraries may actually be harder to use.</p></blockquote>

## Commenting

CSS is a tricky language, full of hacks and oddities. Because of this, it should be heavily commented, especially if you or someone else intend to read and update the code 6 months or 1 year from now. Don’t let you or anybody else be in the position of *I-didn’t-write-this-oh-my-god-why*.

As simple as CSS can get, there is still a lot of room for comments. These could be explaining:

- the structure and/or role of a file;
- the goal of a ruleset;
- the idea behind a magic number;
- the reason for a CSS declaration;
- the order of CSS declarations;
- the thought process behind a way of doing things.

And I probably forgot a lot of other various reasons as well. Commenting takes very little time when done seamlessly along with the code so do it at the right time. Coming back at a piece of code to comment it is not only completely unrealistic but also extremely annoying.

### *Writing Comments*

Ideally, *any* CSS ruleset should be preceded by a C-style comment explaining the point of the CSS block. This comment also hosts numbered explanations regarding specific parts of the ruleset. For instance:

```scss
/**
 * Helper class to truncate and add ellipsis to a string too long for it to fit
 * on a single line.
 * 1. Prevent content from wrapping, forcing it on a single line.
 * 2. Add ellipsis at the end of the line.
 */
.ellipsis {
  white-space: nowrap; /* 1 */
  text-overflow: ellipsis; /* 2 */
  overflow: hidden;
}
```

Basically everything that is not obvious at first glance should be commented. There is no such thing as too much documentation. Remember that you cannot *comment too much*, so get on fire and write comments for everything that is worth it.

When commenting a Sass-specific section, use Sass inline comments instead of a C-style block. This makes the comment invisible in the output, even in expanded mode during development.

```scss
// Add current module to the list of imported modules.
// `!global` flag is required so it actually updates the global variable.
$imported-modules: append($imported-modules, $module) !global;
```

Note that this way of doing things is also supported by CSS Guidelines in its [Commenting](http://cssguidelin.es/#commenting) section.

### *Documentation*

Every variable, function, mixin and placeholder that is intended to be reused all over the codebase should be documented as part of the global API using [SassDoc](http://sassdoc.com/).

```scss
/// Vertical rhythm baseline used all over the code base.
/// @type Length
$vertical-rhythm-baseline: 1.5rem;
```

<blockquote class="note"><p>Three slashes (<code>/</code>) required.</p></blockquote>

SassDoc has two major roles:

- forcing standardized comments using an annotation-based system for everything that is part of a public or private API;
- being able to generate an HTML version of the API documentation by using any of the SassDoc endpoints (CLI tool, Grunt, Gulp, Broccoli, Node…).

<figure role="group" style="text-align: center"> <img data-proofer-ignore="" alt="Documentation generated by SassDoc " sizes="100vw" srcset="https://d33wubrfki0l68.cloudfront.net/68a6846edb356c44cb53dda05760797b2d1baf81/c2a92/assets/images/sassdoc-preview_small.png 540w, https://d33wubrfki0l68.cloudfront.net/97984b488095bfee6f2c6e47c500915b665cfe86/5aa53/assets/images/sassdoc-preview_medium.png 900w, https://d33wubrfki0l68.cloudfront.net/c5894fe21ae4828475ba1483a6fb1d94e151a3d5/4d6c5/assets/images/sassdoc-preview_large.png 1200w, https://d33wubrfki0l68.cloudfront.net/a73c466f7ea902521035603506888db0af2c8e3d/0aa5a/assets/images/sassdoc-preview_huge.png 1590w"><figcaption>Documentation generated by SassDoc</figcaption></figure>

Here is an example of a mixin extensively documented with SassDoc:

```scss
/// Mixin helping defining both `width` and `height` simultaneously.
///
/// @author Hugo Giraudel
///
/// @access public
///
/// @param {Length} $width - Element’s `width`
/// @param {Length} $height [$width] - Element’s `height`
///
/// @example scss - Usage
///   .foo {
///     @include size(10em);
///   }
///
///   .bar {
///     @include size(100%, 10em);
///   }
///
/// @example css - CSS output
///   .foo {
///     width: 10em;
///     height: 10em;
///   }
///
///   .bar {
///     width: 100%;
///     height: 10em;
///   }
@mixin size($width, $height: $width) {
  width: $width;
  height: $height;
}
```

## Architecture

Architecting a CSS project is probably one of the most difficult things you will have to do in a project’s life. Keeping the architecture consistent and meaningful is even harder.

Fortunately, one of the main benefits of using a CSS preprocessor is having the ability to split the codebase over several files without impacting performance (like the `@import` CSS directive would do). Thanks to Sass’s overload of the `@import` directive, it is perfectly safe (and actually recommended) to use as many files as necessary in development, all compiled into a single stylesheet when going to production.

On top of that, I cannot stress enough the need for folders, even on small scale projects. At home, you don’t drop every sheet of paper into the same box. You use folders; one for the house/flat, one for the bank, one for bills, and so on. There is no reason to do otherwise when structuring a CSS project. Split the codebase into meaningful separated folders so it is easy to find stuff later when you have to come back to the code.

There are [a lot of popular architectures](http://www.sitepoint.com/look-different-sass-architectures/) for CSS projects: [OOCSS](http://www.smashingmagazine.com/2011/12/12/an-introduction-to-object-oriented-css-oocss/), [Atomic Design](http://bradfrost.com/blog/post/atomic-web-design/), [Bootstrap](http://getbootstrap.com/)-like, [Foundation](http://foundation.zurb.com/)-like… They all have their merits, pros and cons.

I, myself, use an approach that happens to be quite similar to [SMACSS](https://smacss.com/) from [Jonathan Snook](http://snook.ca/), which focuses on keeping things simple and obvious.

<blockquote class="note"><p>I have learnt that architecture is most of the time very specific to the project. Feel free to discard completely or adapt the proposed solution so that you deal with a system that suits your needs.</p></blockquote>

### *Components*

There is a major difference between making it *work*, and making it *good*. Again, CSS is quite a messy language [citation needed]. The less CSS we have, the merrier. We don’t want to deal with megabytes of CSS code. To keep stylesheets short and efficient—and this will not be any surprise to you—it is usually a good idea to think of an interface as a collection of components.

Components can be anything, as long as they:

- do one thing and one thing only;
- are re-usable and re-used across the project;
- are independent.

For instance, a search form should be treated as a component. It should be reusable, at different positions, on different pages, in various situations. It should not depend on its position in the DOM (footer, sidebar, main content…).

Most of any interface can be thought of as little components and I highly recommend you stick to this paradigm. This will not only shorten the amount of CSS needed for the whole project, but also happens to be much easier to maintain than a chaotic mess where everything is flustered.

### *Component Structure*

Ideally, components should exist in their own Sass partial (within the `components/` folder, as is described in the [7-1 pattern](https://sass-guidelin.es/#the-7-1-pattern)), such as `components/_button.scss`. The styles described in each component file should only be concerned with:

- the style of the component itself;
- the style of the component’s variants, modifiers, and/or states;
- the styles of the component’s descendents (i.e. children), if necessary.

If you want your components to be able to be themed externally (e.g. from a theme inside the `themes/` folder), limit the declarations to only structural styles, such as dimensions (width/height), padding, margins, alignment, etc. Exclude styles such as colors, shadows, font rules, background rules, etc.

A component partial can include component-specific variables, placeholders, and even mixins and functions. Keep in mind, though, that you should avoid referencing (i.e. `@import`-ing) component files from other component files, as this can make your project’s dependency graph an unmaintainable tangled mess.

Here is an example of a button component partial:

```scss
// Button-specific variables
$button-color: $secondary-color;

// … include any button-specific:
// - mixins
// - placeholders
// - functions

/**
 * Buttons
 */
.button {
  @include vertical-rhythm;
  display: block;
  padding: 1rem;
  color: $button-color;
  // … etc.

  /**
   * Inlined buttons on large screens
   */
  @include respond-to('medium') {
    display: inline-block;
  }
}

/**
 * Icons within buttons
 */
.button > svg {
  fill: currentcolor;
  // … etc.
}

/**
 * Inline button
 */
.button--inline {
  display: inline-block;
}
```

<blockquote class="note"><p>Thanks to <a href="https://twitter.com/davidkpiano">David Khourshid</a> for his help and expertise on this section.</p></blockquote>

### *The 7-1 Pattern*

Back to architecture, shall we? I usually go with what I call the *7-1 pattern*: 7 folders, 1 file. Basically, you have all your partials stuffed into 7 different folders, and a single file at the root level (usually named `main.scss`) which imports them all to be compiled into a CSS stylesheet.

- `base/`
- `components/`
- `layout/`
- `pages/`
- `themes/`
- `abstracts/`
- `vendors/`

And of course:

- `main.scss`

<blockquote class="note"><p>If you are looking to use the 7-1 pattern, there is a <a href="https://github.com/HugoGiraudel/sass-boilerplate">boilerplate</a> ready on GitHub. It should contain everything you need to get started with this architecture.</p></blockquote>

<figure role="group" style="text-align: center"> <img data-proofer-ignore="" alt="Wallpaper by Julien He " sizes="100vw" srcset="https://d33wubrfki0l68.cloudfront.net/83050df0f35e960a4fc2bb0b0f8df68ee25ab80a/d4b00/assets/images/sass-wallpaper_small.jpg 540w, https://d33wubrfki0l68.cloudfront.net/6687589e656a32ecb7780d13fac82a67cd8c679d/e3e38/assets/images/sass-wallpaper_medium.jpg 900w, https://d33wubrfki0l68.cloudfront.net/c0f986a6a230f667e2b180436899ffe86c29f33c/03f50/assets/images/sass-wallpaper_large.jpg 1200w, https://d33wubrfki0l68.cloudfront.net/2cc0bf5eb77112d83166f6324013ba157139ae24/8e392/assets/images/sass-wallpaper_huge.jpg 1590w"><figcaption>Wallpaper by <a href="https://twitter.com/julien_he">Julien He</a></figcaption></figure>

Ideally, we can come up with something like this:

```scss
sass/
|
|– abstracts/
|   |– _variables.scss    # Sass Variables
|   |– _functions.scss    # Sass Functions
|   |– _mixins.scss       # Sass Mixins
|   |– _placeholders.scss # Sass Placeholders
|
|– base/
|   |– _reset.scss        # Reset/normalize
|   |– _typography.scss   # Typography rules
|   …                     # Etc.
|
|– components/
|   |– _buttons.scss      # Buttons
|   |– _carousel.scss     # Carousel
|   |– _cover.scss        # Cover
|   |– _dropdown.scss     # Dropdown
|   …                     # Etc.
|
|– layout/
|   |– _navigation.scss   # Navigation
|   |– _grid.scss         # Grid system
|   |– _header.scss       # Header
|   |– _footer.scss       # Footer
|   |– _sidebar.scss      # Sidebar
|   |– _forms.scss        # Forms
|   …                     # Etc.
|
|– pages/
|   |– _home.scss         # Home specific styles
|   |– _contact.scss      # Contact specific styles
|   …                     # Etc.
|
|– themes/
|   |– _theme.scss        # Default theme
|   |– _admin.scss        # Admin theme
|   …                     # Etc.
|
|– vendors/
|   |– _bootstrap.scss    # Bootstrap
|   |– _jquery-ui.scss    # jQuery UI
|   …                     # Etc.
|
`– main.scss              # Main Sass file
```

<blockquote class="note"><p>Files follow the same naming conventions described above: they are hyphen-delimited.</p></blockquote>

###### BASE FOLDER

The `base/` folder holds what we might call the boilerplate code for the project. In there, you might find the reset file, some typographic rules, and probably a stylesheet defining some standard styles for commonly used HTML elements (that I like to call `_base.scss`).

- `_base.scss`
- `_reset.scss`
- `_typography.scss`

<blockquote class="note"><p>If your project uses <em>a lot</em> of CSS animations, you might consider adding an <code>\_animations.scss</code> file in there containing the <code>@keyframes</code> definitions of all your animations. If you only use a them sporadically, let them live along the selectors that use them.</p></blockquote>

###### LAYOUT FOLDER

The `layout/` folder contains everything that takes part in laying out the site or application. This folder could have stylesheets for the main parts of the site (header, footer, navigation, sidebar…), the grid system or even CSS styles for all the forms.

- `_grid.scss`
- `_header.scss`
- `_footer.scss`
- `_sidebar.scss`
- `_forms.scss`
- `_navigation.scss`

<blockquote class="note"><p>The <code>layout/</code> folder might also be called <code>partials/</code>, depending on what you prefer.</p></blockquote>

###### COMPONENTS FOLDER

For smaller components, there is the `components/` folder. While `layout/` is *macro* (defining the global wireframe), `components/` is more focused on widgets. It contains all kind of specific modules like a slider, a loader, a widget, and basically anything along those lines. There are usually a lot of files in `components/` since the whole site/application should be mostly composed of tiny modules.

- `_media.scss`
- `_carousel.scss`
- `_thumbnails.scss`

<blockquote class="note"><p>The <code>components/</code> folder might also be called <code>modules/</code>, depending on what you prefer.</p></blockquote>

###### PAGES FOLDER

If you have page-specific styles, it is better to put them in a `pages/` folder, in a file named after the page. For instance, it’s not uncommon to have very specific styles for the home page hence the need for a `_home.scss` file in `pages/`.

- `_home.scss`
- `_contact.scss`

<blockquote class="note"><p>Depending on your deployment process, these files could be called on their own to avoid merging them with the others in the resulting stylesheet. It is really up to you.</p></blockquote>

###### THEMES FOLDER

On large sites and applications, it is not unusual to have different themes. There are certainly different ways of dealing with themes but I personally like having them all in a `themes/` folder.

- `_theme.scss`
- `_admin.scss`

<blockquote class="note"><p>This is very project-specific and is likely to be non-existent on many projects.</p></blockquote>

###### ABSTRACTS FOLDER

The `abstracts/` folder gathers all Sass tools and helpers used across the project. Every global variable, function, mixin and placeholder should be put in here.

The rule of thumb for this folder is that it should not output a single line of CSS when compiled on its own. These are nothing but Sass helpers.

- `_variables.scss`
- `_mixins.scss`
- `_functions.scss`
- `_placeholders.scss`

When working on a very large project with a lot of abstract utilities, it might be interesting to group them by topic rather than type, for instance typography (`_typography.scss`), theming (`_theming.scss`), etc. Each file contains all the related helpers: variables, functions, mixins and placeholders. Doing so can make the code easier to browse and maintain, especially when files are getting very long.

<blockquote class="note"><p>The <code>abstracts/</code> folder might also be called <code>utilities/</code> or <code>helpers/</code>, depending on what you prefer.</p></blockquote>

###### VENDORS FOLDER

And last but not least, most projects will have a `vendors/` folder containing all the CSS files from external libraries and frameworks – Normalize, Bootstrap, jQueryUI, FancyCarouselSliderjQueryPowered, and so on. Putting those aside in the same folder is a good way to say “Hey, this is not from me, not my code, not my responsibility”.

- `_normalize.scss`
- `_bootstrap.scss`
- `_jquery-ui.scss`
- `_select2.scss`

If you have to override a section of any vendor, I recommend you have an 8th folder called `vendors-extensions/` in which you may have files named exactly after the vendors they overwrite.

For instance, `vendors-extensions/_bootstrap.scss` is a file containing all CSS rules intended to re-declare some of Bootstrap’s default CSS. This is to avoid editing the vendor files themselves, which is generally not a good idea.

###### MAIN FILE

The main file (usually labelled `main.scss`) should be the only Sass file from the whole code base not to begin with an underscore. This file should not contain anything but `@import` and comments.

Files should be imported according to the folder they live in, one after the other in the following order:

1. `abstracts/`
2. `vendors/`
3. `base/`
4. `layout/`
5. `components/`
6. `pages/`
7. `themes/`

In order to preserve readability, the main file should respect these guidelines:

- one file per `@import`;
- one `@import` per line;
- no new line between two imports from the same folder;
- a new line after the last import from a folder;
- file extensions and leading underscores omitted.

```scss
@import 'abstracts/variables';
@import 'abstracts/functions';
@import 'abstracts/mixins';
@import 'abstracts/placeholders';

@import 'vendors/bootstrap';
@import 'vendors/jquery-ui';

@import 'base/reset';
@import 'base/typography';

@import 'layout/navigation';
@import 'layout/grid';
@import 'layout/header';
@import 'layout/footer';
@import 'layout/sidebar';
@import 'layout/forms';

@import 'components/buttons';
@import 'components/carousel';
@import 'components/cover';
@import 'components/dropdown';

@import 'pages/home';
@import 'pages/contact';

@import 'themes/theme';
@import 'themes/admin';
```

There is another way of importing partials that I deem valid as well. On the bright side, it makes the file more readable. On the other hand, it makes updating it slightly more painful. Anyway, I’ll let you decide which is best, it does not matter much. For this way of doing, the main file should respect these guidelines:

- one `@import` per folder;
- a linebreak after `@import`;
- each file on its own line;
- a new line after the last import from a folder;
- file extensions and leading underscores omitted.

```scss
@import
  'abstracts/variables',
  'abstracts/functions',
  'abstracts/mixins',
  'abstracts/placeholders';

@import
  'vendors/bootstrap',
  'vendors/jquery-ui';

@import
  'base/reset',
  'base/typography';

@import
  'layout/navigation',
  'layout/grid',
  'layout/header',
  'layout/footer',
  'layout/sidebar',
  'layout/forms';

@import
  'components/buttons',
  'components/carousel',
  'components/cover',
  'components/dropdown';

@import
  'pages/home',
  'pages/contact';

@import
  'themes/theme',
  'themes/admin';
```

### *About Globbing*

In computer programming, glob patterns specify sets of filenames with wildcard characters, such as `*.scss`. To a general extent, globbing means matching a set of files based on an expression instead of a list of filenames. When applied to Sass, it means importing partials into the [main file](https://sass-guidelin.es/#main-file) with a glob pattern rather than by listing them individually. This would lead to a main file looking like this:

```scss
@import 'abstracts/*';
@import 'vendors/*';
@import 'base/*';
@import 'layout/*';
@import 'components/*';
@import 'pages/*';
@import 'themes/*';
```

Sass does not support file globbing out of the box because it can be a dangerous feature as CSS is known to be order-dependant. When dynamically importing files (which usually goes in alphabetical order), one does not control the source order anymore, which can lead to hard to debug side-effects.

That being said, in a strict component-based architecture with extra care not to leak any style from one partial to the other, the order should not really matter anymore, which would allow for glob imports. This would make it easier to add or remove partials as carefully updating the main file would no longer be required.

When using Ruby Sass, there is a Ruby gem called [sass-globbing](https://github.com/chriseppstein/sass-globbing) that enables exactly that behavior. If running on node-sass, one can rely either on Node.js, or whatever build tool they use to handle the compilation (Gulp, Grunt, etc.).

### *Shame File*

There is an interesting concept that has been made popular by [Harry Roberts](http://csswizardry.com/), [Dave Rupert](http://daverupert.com/) and [Chris Coyier](http://css-tricks.com/) that consists of putting all the CSS declarations, hacks and things we are not proud of in a [shame file](http://csswizardry.com/2013/04/shame-css-full-net-interview/). This file, dramatically titled `_shame.scss`, would be imported after any other file, at the very end of the stylesheet.

```scss
/**
 * Nav specificity fix.
 *
 * Someone used an ID in the header code (`#header a {}`) which trumps the
 * nav selectors (`.site-nav a {}`). Use !important to override it until I
 * have time to refactor the header stuff.
 */
.site-nav a {
    color: #BADA55 !important;
}
```

## Responsive Web Design And Breakpoints

I do not think we still have to introduce Responsive Web Design now that it is everywhere. However you might ask yourself *why is there a section about RWD in a Sass styleguide?* Actually there are quite a few things that can be done to make working with breakpoints easier, so I thought it would not be such a bad idea to list them here.

### *Naming Breakpoints*

I think it is safe to say that media queries should not be tied to specific devices. For instance, this is definitely a bad idea to try targeting iPads or Blackberry phones specifically. Media queries should take care of a range of screen sizes, until the design breaks and the next media query takes over.

For the same reasons, breakpoints should not be named after devices but something more general. Especially since some phones are now bigger than tablets, some tablets bigger than some tiny screen computers, and so on…

```scss
// Yep
$breakpoints: (
  'medium': (min-width: 800px),
  'large': (min-width: 1000px),
  'huge': (min-width: 1200px),
);

// Nope
$breakpoints: (
  'tablet': (min-width: 800px),
  'computer': (min-width: 1000px),
  'tv': (min-width: 1200px),
);
```

At this point, [any naming convention](http://css-tricks.com/naming-media-queries/) that makes crystal clear that a design is not intimately tied to a specific device type will do the trick, as long as it gives a sense of magnitude.

```scss
$breakpoints: (
  'seed': (min-width: 800px),
  'sprout': (min-width: 1000px),
  'plant': (min-width: 1200px),
);
```

<blockquote class="note"><p>The previous examples uses nested maps to define breakpoints, however this really depends on what kind of breakpoint manager you use. You could opt for strings rather than inner maps for more flexibility (e.g. <code>'(min-width: 800px)'</code>).</p></blockquote>

### *Breakpoint Manager*

Once you have named your breakpoints the way you want, you need a way to use them in actual media queries. There are plenty of ways to do so but I must say I am a big fan of the breakpoint map read by a getter function. This system is both simple and efficient.

```scss
/// Responsive breakpoint manager
/// @access public
/// @param {String} $breakpoint - Breakpoint
/// @requires $breakpoints
@mixin respond-to($breakpoint) {
  $raw-query: map-get($breakpoints, $breakpoint);

  @if $raw-query {
    $query: if(
      type-of($raw-query) == 'string',
      unquote($raw-query),
      inspect($raw-query)
    );

    @media #{$query} {
      @content;
    }
  } @else {
    @error 'No value found for `#{$breakpoint}`. '
         + 'Please make sure it is defined in `$breakpoints` map.';
  }
}
```

<blockquote class="note"><p>Obviously, this is a fairly simplistic breakpoint manager. If you need a slightly more permissive one, may I recommend you do not reinvent the wheel and use something that has been proven effective such as <a href="https://github.com/sass-mq/sass-mq">Sass-MQ</a>, <a href="http://breakpoint-sass.com/">Breakpoint</a> or <a href="https://github.com/eduardoboucas/include-media">include-media</a>.</p><p>If you are looking to read more on how to approach Media Queries in Sass, both <a href="http://www.sitepoint.com/managing-responsive-breakpoints-sass/">SitePoint</a> (from yours, truly) and <a href="http://css-tricks.com/approaches-media-queries-sass/">CSS-Tricks</a> have nice articles on this.</p></blockquote>

### *Media Queries Usage*

Not so long ago, there was quite a hot debate about where media queries should be written: do they belong within selectors (as Sass allows it) or strictly dissociated from them? I have to say I am a fervent defender of the *media-queries-within-selectors* system, as I think it plays well with the ideas of *components*.

```scss
.foo {
  color: red;

  @include respond-to('medium') {
    color: blue;
  }
}
```

Leading to the following CSS output:

```css
.foo {
  color: red;
}

@media (min-width: 800px) {
  .foo {
    color: blue;
  }
}
```

You might hear that this convention results in duplicated media queries in the CSS output. That is definitely true. Although, [tests have been made](http://sasscast.tumblr.com/post/38673939456/sass-and-media-queries) and the final word is that it doesn’t matter once Gzip (or any equivalent) has done its thing:

> … we hashed out whether there were performance implications of combining vs scattering Media Queries and came to the conclusion that the difference, while ugly, is minimal at worst, essentially non-existent at best.
> — [Sam Richards, regarding Breakpoint](http://sasscast.tumblr.com/post/38673939456/sass-and-media-queries)

Now, if you really are concerned about duplicated media queries, you can still use a tool to merge them such as [this gem](https://github.com/aaronjensen/sass-media_query_combiner) however I feel like I have to warn you against possible side-effects of moving CSS code around. You are not without knowing that source order is important.

## Variables

Variables are the essence of any programming language. They allow us to reuse values without having to copy them over and over again. Most importantly, they make updating a value very easy. No more find and replace or manual crawling.

However CSS is nothing but a huge basket containing all our eggs. Unlike many languages, there are no real scopes in CSS. Because of this, we have to pay real attention when adding variables at the risk of witnessing conflicts.

My advice would be to only create variables when it makes sense to do so. Do not initiate new variables for the heck of it, it won’t help. A new variable should be created only when all of the following criteria are met:

- the value is repeated at least twice;
- the value is likely to be updated at least once;
- all occurrences of the value are tied to the variable (i.e. not by coincidence).

Basically, there is no point declaring a variable that will never be updated or that is only being used at a single place.

### *Scoping*

Variable scoping in Sass has changed over the years. Until fairly recently, variable declarations within rulesets and other scopes were local by default. However when there was already a global variable with the same name, the local assignment would change the global variable. Since version 3.4, Sass now properly tackles the concept of scopes and create a new local variable instead.

The docs talk about *global variable shadowing*. When declaring a variable that already exists on the global scope in an inner scope (selector, function, mixin…), the local variable is said to be *shadowing* the global one. Basically, it overrides it just for the local scope.

The following code snippet explains the *variable shadowing* concept.

```scss
// Initialize a global variable at root level.
$variable: 'initial value';

// Create a mixin that overrides that global variable.
@mixin global-variable-overriding {
  $variable: 'mixin value' !global;
}

.local-scope::before {
  // Create a local variable that shadows the global one.
  $variable: 'local value';

  // Include the mixin: it overrides the global variable.
  @include global-variable-overriding;

  // Print the variable’s value.
  // It is the **local** one, since it shadows the global one.
  content: $variable;
}

// Print the variable in another selector that does no shadowing.
// It is the **global** one, as expected.
.other-local-scope::before {
  content: $variable;
}
```

### *`!default` Flag*

When building a library, a framework, a grid system or any piece of Sass that is intended to be distributed and used by external developers, all configuration variables should be defined with the `!default` flag so they can be overwritten.

```scss
$baseline: 1em !default;
```

Thanks to this, a developer can define their own `$baseline` variable *before*importing your library without seeing their value redefined.

```scss
// Developer’s own variable
$baseline: 2em;

// Your library declaring `$baseline`
@import 'your-library';

// $baseline == 2em;
```

### *`!global` Flag*

The `!global` flag should only be used when overriding a global variable from a local scope. When defining a variable at root level, the `!global` flag should be omitted.

```scss
// Yep
$baseline: 2em;

// Nope
$baseline: 2em !global;
```

### *Multiple Variables Or Maps*

There are advantages of using maps rather than multiple distinct variables. The main one is the ability to loop over a map, which is not possible with distinct variables.

Another pro of using a map is the ability to create a little getter function to provide a friendlier API. For instance, consider the following Sass code:

```scss
/// Z-indexes map, gathering all Z layers of the application
/// @access private
/// @type Map
/// @prop {String} key - Layer’s name
/// @prop {Number} value - Z value mapped to the key
$z-indexes: (
  'modal': 5000,
  'dropdown': 4000,
  'default': 1,
  'below': -1,
);

/// Get a z-index value from a layer name
/// @access public
/// @param {String} $layer - Layer’s name
/// @return {Number}
/// @require $z-indexes
@function z($layer) {
  @return map-get($z-indexes, $layer);
}
```

## Extend

The `@extend` directive is a powerful feature that is frequently misunderstood. In general, it makes it possible to tell Sass to style a selector A as though it also matched selector B. Needless to say, this can be a valuable ally when writing modular CSS.

However, the true purpose of `@extend` is to maintain the relationships (constraints) within extended selectors between rulesets. What exactly does this mean?

- Selectors have *constraints* (e.g. `.bar` in `.foo > .bar` must have a parent `.foo`);
- These constraints are *carried over* to the extending selector (e.g. `.baz { @extend .bar; }` will produce `.foo > .bar, .foo > .baz`);
- The declarations of the extended selector will be shared with the extending selector.

Given that, it’s straightforward to see how extending selectors with lenient constraints can lead to selector explosion. If `.baz .qux` extends `.foo .bar`, the resulting selector can be `.foo .baz .qux` or `.baz .foo .qux`, as both `.foo` and `.baz` are general ancestors. They can be parents, grandparents, etc.

Always try to define relationships via [selector placeholders](http://www.sitepoint.com/sass-reference/placeholders/), not actual selectors. This will give you the freedom to use (and change) any naming convention you have for your selectors, and since relationships are only defined once inside the placeholders, you are far less likely to produce unintended selectors.

For inheriting styles, only use `@extend` if the extending `.class` or `%placeholder`selector *is a kind of* the extended selector. For instance, an `.error` is a kind of `.warning`, so `.error` can `@extend .warning`.

```scss
%button {
  display: inline-block;
  // … button styles

  // Relationship: a %button that is a child of a %modal
  %modal > & {
    display: block;
  }
}

.button {
  @extend %button;
}

// Yep
.modal {
  @extend %modal;
}

// Nope
.modal {
  @extend %modal;

  > .button {
    @extend %button;
  }
}
```

There are many scenarios where extending selectors are helpful and worthwhile. Always keep in mind these rules so you can `@extend` with care:

- Use extend on `%placeholders` primarily, not on actual selectors.
- When extending classes, only extend a class with another class, *never* a [complex selector](http://www.w3.org/TR/selectors4/#syntax).
- Directly extend a `%placeholder` as few times as possible.
- Avoid extending general ancestor selectors (e.g. `.foo .bar`) or general sibling selectors (e.g. `.foo ~ .bar`). This is what causes selector explosion.

<blockquote class="note"><p>It is often said that <code>@extend</code> helps with the file size since it combines selectors rather than duplicating properties. That is true, however the difference is negligible once <a href="http://en.wikipedia.org/wiki/Gzip">Gzip</a> has done its compression.</p><p>That being said, if you cannot use Gzip (or any equivalent) then switching to a <code>@extend</code> approach might be valuable, especially if stylesheet weight is your performance bottleneck.</p></blockquote>

### *Extend And Media Queries*

You should only extend selectors within the same media scope (`@media`directive). Think of a media query as another constraint.

```scss
%foo {
  content: 'foo';
}

// Nope
@media print {
  .bar {
    // This doesn't work. Worse: it crashes.
    @extend %foo;
  }
}

// Yep
@media print {
  .bar {
    @at-root (without: media) {
      @extend %foo;
    }
  }
}

// Yep
%foo {
  content: 'foo';

  &-print {
    @media print {
      content: 'foo print';
    }
  }
}

@media print {
  .bar {
    @extend %foo-print;
  }
}
```

Opinions seem to be extremely divided regarding the benefits and problems from `@extend` to the point where many developers including myself have been advocating against it, as you can read in the following articles:

- [What Nobody Told you About Sass Extend](http://www.sitepoint.com/sass-extend-nobody-told-you/)
- [Why You Should Avoid Extend](http://www.sitepoint.com/avoid-sass-extend/)
- [Don’t Over Extend Yourself](http://pressupinc.com/blog/2014/11/dont-overextend-yourself-in-sass/)

That being said and to sum up, I would advise to use `@extend` only for maintaining relationships within selectors. If two selectors are characteristically similar, that is the perfect use-case for `@extend`. If they are unrelated but share some rules, a `@mixin` might suit you better. More on how to choose between the two in this [write-up](http://csswizardry.com/2014/11/when-to-use-extend-when-to-use-a-mixin/).

<blockquote class="note"><p>Thanks to <a href="https://twitter.com/davidkpiano">David Khourshid</a> for his help and expertise on this section.</p></blockquote>

## Mixins

Mixins are one of the most used features from the whole Sass language. They are the key to reusability and DRY components. And for good reason: mixins allow authors to define styles that can be reused throughout the stylesheet without needing to resort to non-semantic classes such as `.float-left`.

They can contain full CSS rules and pretty much everything that is allowed anywhere in a Sass document. They can even take arguments, just like functions. Needless to say, the possibilities are endless.

But I feel I must warn you against abusing the power of mixins. Again, the keyword here is *simplicity*. It might be tempting to build extremely powerful mixins with massive amounts of logic. It’s called over-engineering and most developers suffer from it. Don’t over think your code, and above all keep it simple. If a mixin ends up being longer than 20 lines or so, then it should be either split into smaller chunks or completely revised.

### *Basics*

That being said, mixins are extremely useful and you should be using some. The rule of thumb is that if you happen to spot a group of CSS properties that always appear together for a reason (i.e. not a coincidence), you can put them in a mixin instead. The [micro-clearfix hack from Nicolas Gallagher](http://nicolasgallagher.com/micro-clearfix-hack/)deserves to be put in a (argumentless) mixin for instance.

```scss
/// Helper to clear inner floats
/// @author Nicolas Gallagher
/// @link http://nicolasgallagher.com/micro-clearfix-hack/ Micro Clearfix
@mixin clearfix {
  &::after {
    content: '';
    display: table;
    clear: both;
  }
}
```

Another valid example would be a mixin to size an element, defining both `width` and `height` at the same time. Not only would it make the code lighter to type, but also easier to read.

```scss
/// Helper to size an element
/// @author Hugo Giraudel
/// @param {Length} $width
/// @param {Length} $height
@mixin size($width, $height: $width) {
  width: $width;
  height: $height;
}
```

For more complex examples of mixins, have a look at [this mixin to generate CSS triangles](http://www.sitepoint.com/sass-mixin-css-triangles/), [this mixin to create long shadows](http://www.sitepoint.com/ultimate-long-shadow-sass-mixin/) or [this mixin to polyfill CSS gradients for old browsers](http://www.sitepoint.com/building-linear-gradient-mixin-sass/).

### *Argument-Less Mixins*

Sometimes mixins are used only to avoid repeating the same group of declarations over and over again, yet do not need any parameter or have sensible enough defaults so that we don’t necessarily have to pass arguments.

In such cases, we can safely omit the parentheses when calling them. The `@include` keyword (or `+` sign in indented-syntax) already acts as a indicator that the line is a mixin call; there is no need for extra parentheses here.

```scss
// Yep
.foo {
  @include center;
}

// Nope
.foo {
  @include center();
}
```

### *Arguments List*

When dealing with an unknown number of arguments in a mixin, always use an `arglist` rather than a list. Think of `arglist` as the 8th hidden undocumented data type from Sass that is implicitly used when passing an arbitrary number of arguments to a mixin or a function whose signature contains `...`.

```scss
@mixin shadows($shadows...) {
  // type-of($shadows) == 'arglist'
  // …
}
```

Now, when building a mixin that accepts a handful of arguments (understand 3 or more), think twice before merging them out as a list or a map thinking it will be easier than passing them all one by one.

Sass is actually pretty clever with mixins and function declarations, so much so that you can actually pass a list or a map as an arglist to a function/mixin so that it gets parsed as a series of arguments.

```scss
@mixin dummy($a, $b, $c) {
  // …
}

// Yep
@include dummy(true, 42, 'kittens');

// Yep but nope
$params: (true, 42, 'kittens');
$value: dummy(nth($params, 1), nth($params, 2), nth($params, 3));

// Yep
$params: (true, 42, 'kittens');
@include dummy($params...);

// Yep
$params: (
  'c': 'kittens',
  'a': true,
  'b': 42,
);
@include dummy($params...);
```

For more information on whether it is best to use multiple arguments, a list or an argument list, [SitePoint has a nice piece on the topic](http://www.sitepoint.com/sass-multiple-arguments-lists-or-arglist/).

### *Mixins And Vendor Prefixes*

It might be tempting to define custom mixins to handle vendor prefixes for unsupported or partially supported CSS properties. But we do not want to do this. First, if you can use [Autoprefixer](https://github.com/postcss/autoprefixer), use Autoprefixer. It will remove Sass code from your project, will always be up-to-date and will necessarily do a much better job than you at prefixing stuff.

Unfortunately, Autoprefixer is not always an option. If you use either [Bourbon](http://bourbon.io/)or [Compass](http://compass-style.org/), you may already know that they both provide a collection of mixins that handle vendor prefixes for you. Use those.

If you cannot use Autoprefixer and use neither Bourbon nor Compass, then and only then, you can have your own mixin for prefixing CSS properties. But. Please do not build a mixin per property, manually printing each vendor.

```scss
// Nope
@mixin transform($value) {
  -webkit-transform: $value;
  -moz-transform: $value;
  transform: $value;
}
```

Do it the clever way.

```scss
/// Mixin helper to output vendor prefixes
/// @access public
/// @author HugoGiraudel
/// @param {String} $property - Unprefixed CSS property
/// @param {*} $value - Raw CSS value
/// @param {List} $prefixes - List of prefixes to output
@mixin prefix($property, $value, $prefixes: ()) {
  @each $prefix in $prefixes {
    -#{$prefix}-#{$property}: $value;
  }

  #{$property}: $value;
}
```

Then using this mixin should be very straightforward:

```scss
.foo {
  @include prefix(transform, rotate(90deg), ('webkit', 'ms'));
}
```

Please keep in mind this is a poor solution. For instance, it cannot deal with complex polyfills such as those required for Flexbox. In that sense, using Autoprefixer would be a far better option.

## Conditional Statements

You probably already know that Sass provides conditional statements via the `@if` and `@else` directives. Unless you have some medium to complex logic in your code, there is no need for conditional statements in your everyday stylesheets. Actually, they mainly exist for libraries and frameworks.

Anyway, if you ever find yourself in need of them, please respect the following guidelines:

- No parentheses unless they are necessary;
- Always an empty new line before `@if`;
- Always a line break after the opening brace (`{`);
- `@else` statements on the same line as previous closing brace (`}`).
- Always an empty new line after the last closing brace (`}`) unless the next line is a closing brace (`}`).

```scss
// Yep
@if $support-legacy {
  // …
} @else {
  // …
}

// Nope
@if ($support-legacy == true) {
  // …
}
@else {
  // …
}
```

When testing for a falsy value, always use the `not` keyword rather than testing against `false` or `null`.

```scss
// Yep
@if not index($list, $item) {
  // …
}

// Nope
@if index($list, $item) == null {
  // …
}
```

Always put the variable part on the left side of the statement, and the (un)expected result on the right. Reversed conditional statements often are more difficult to read, especially to unexperienced developers.

```scss
// Yep
@if $value == 42 {
  // …
}

// Nope
@if 42 == $value {
  // …
}
```

When using conditional statements within a function to return a different result based on some condition, always make sure the function still has a `@return` statement outside of any conditional block.

```scss
// Yep
@function dummy($condition) {
  @if $condition {
    @return true;
  }

  @return false;
}

// Nope
@function dummy($condition) {
  @if $condition {
    @return true;
  } @else {
    @return false;
  }
}
```

## Loops

Because Sass provides complex data structures such as [lists](https://sass-guidelin.es/#lists) and [maps](https://sass-guidelin.es/#maps), it is no surprise that it also gives a way for authors to iterate over those entities.

However, the presence of loops usually implies moderately complex logic that probably does not belong to Sass. Before using a loop, make sure it makes sense and that it actually solves an issue.

### *Each*

The `@each` loop is definitely the most-used out of the three loops provided by Sass. It provides a clean API to iterate over a list or a map.

```scss
@each $theme in $themes {
  .section-#{$theme} {
    background-color: map-get($colors, $theme);
  }
}
```

When iterating on a map, always use `$key` and `$value` as variable names to enforce consistency.

```scss
@each $key, $value in $map {
  .section-#{$key} {
    background-color: $value;
  }
}
```

Also be sure to respect those guidelines to preserve readability:

- Always an empty new line before `@each`;
- Always an empty new line after the closing brace (`}`) unless the next line is a closing brace (`}`).

### *For*

The `@for` loop might be useful when combined with CSS’ `:nth-*` pseudo-classes. Except for these scenarios, prefer an `@each` loop if you *have to* iterate over something.

```scss
@for $i from 1 through 10 {
  .foo:nth-of-type(#{$i}) {
    border-color: hsl($i * 36, 50%, 50%);
  }
}
```

Always use `$i` as a variable name to stick to the usual convention and unless you have a really good reason to, never use the `to` keyword: always use `through`. Many developers do not even know Sass offers this variation; using it might lead to confusion.

Also be sure to respect those guidelines to preserve readability:

- Always an empty new line before `@for`;
- Always an empty new line after the closing brace (`}`) unless the next line is a closing brace (`}`).

### *While*

The `@while` loop has absolutely no use case in a real Sass project, especially since there is no way to break a loop from the inside. **Do not use it**.

## Warnings And Errors

If there is a feature that is often overlooked by Sass developers, it is the ability to dynamically output warnings and errors. Indeed, Sass comes with three custom directives to print content in the standard output system (CLI, compiling app…):

- `@debug`;
- `@warn`;
- `@error`.

Let’s put `@debug` aside since it is clearly intended to debug SassScript, which is not our point here. We are then left with `@warn` and `@error` which are noticeably identical except that one stops the compiler while the other does not. I’ll let you guess which does what.

Now, there is a lot of room in a Sass project for warnings and errors. Basically any mixin or function expecting a specific type or argument could throw an error if something went wrong, or display a warning when doing an assumption.

### *Warnings*

Take this function from [Sass-MQ](https://github.com/sass-mq/sass-mq) attempting to convert a `px` value to `em`, for instance:

```scss
@function mq-px2em($px, $base-font-size: $mq-base-font-size) {	
  @if unitless($px) {	
    @warn 'Assuming #{$px} to be in pixels, attempting to convert it into pixels.';	
    @return mq-px2em($px + 0px);	
  } @else if unit($px) == em {	
    @return $px;	
  }	
   @return ($px / $base-font-size) * 1em;	
}	
```

If the value happens to be unitless, the function assumes the value is meant to be expressed in pixels. At this point, an assumption may be risky so the user should be warned that the software did something that could be considered unexpected.

### *Errors*

Errors, unlike warnings, prevent the compiler from going any further. Basically, they stop the compilation and display a message in the output stream as well as the stack trace, which is handy for debugging. Because of this, errors should be thrown when there is no way for the program to keep running. When possible, try to work around the issue and display a warning instead.

As an example, let’s say you build a getter function to access values from a specific map. You could throw an error if the requested key does not exist in the map.

```scss
/// Z-indexes map, gathering all Z layers of the application
/// @access private
/// @type Map
/// @prop {String} key - Layer’s name
/// @prop {Number} value - Z value mapped to the key
$z-indexes: (
  'modal': 5000,
  'dropdown': 4000,
  'default': 1,
  'below': -1,
);

/// Get a z-index value from a layer name
/// @access public
/// @param {String} $layer - Layer's name
/// @return {Number}
/// @require $z-indexes
@function z($layer) {
  @if not map-has-key($z-indexes, $layer) {
    @error 'There is no layer named `#{$layer}` in $z-indexes. '
         + 'Layer should be one of #{map-keys($z-indexes)}.';
  }

  @return map-get($z-indexes, $layer);
}
```

For more information on how to use `@error` efficiently, [this introduction about error handling](http://webdesign.tutsplus.com/tutorials/an-introduction-to-error-handling-in-sass--cms-19996) should help you.

## Tools

What’s nice about a CSS preprocessor as popular as Sass is that it comes with a whole ecosystem of frameworks, plugins, libraries and tools. After 8 years of existence, we are getting closer and closer to the point where [everything that can be written in Sass has been written in Sass](http://hugogiraudel.com/2014/10/27/rethinking-atwoods-law/).

However my advice would to be to lower the number of dependencies to the strict minimum. Managing dependencies is some sort of hell you don’t want to be part of. Plus, there is little to no need for external dependencies when it comes to Sass.

### *Compass*

[Compass](http://compass-style.org/) is the main [Sass framework](http://www.sitepoint.com/compass-or-bourbon-sass-frameworks/) out there. Developed by [Chris Eppstein](https://twitter.com/chriseppstein), one of the two core designers of Sass, I don’t see it dramatically losing in popularity for a while, if you want my opinion.

Still, [I do not use Compass anymore](http://www.sitepoint.com/dont-use-compass-anymore/), the main reason is that it slows Sass down a lot. Ruby Sass is quite slow in itself, so adding more Ruby and more Sass on top of it doesn’t really help.

The thing is, we use very little from the whole framework. Compass is huge. Cross-browser compatibility mixins is just the tip of the iceberg. Math functions, image helpers, spriting… There is so much that can be done with this great piece of software.

Unfortunately, this is all sugar and there is no killer feature in there. An exception could be made of the sprite builder which is *really great*, but [Grunticon](https://github.com/filamentgroup/grunticon) and [Grumpicon](http://grumpicon.com/) do the job as well, and have the benefit of being pluggable in the build process.

Anyway, I do not forbid the use of Compass although I would not recommend it either, especially since it is not LibSass-compatible (even if efforts have been made in that direction). If you feel better using it, fair enough, but I don’t think you’ll get much from it at the end of the day.

<blockquote class="note"><p>Ruby Sass is currently going under some outstanding optimizations that are specifically targeted at logic-heavy styles with many functions and mixins. They should dramatically improve performance to the point where Compass and other frameworks might not be slowing Sass anymore.</p></blockquote>

### *Grid Systems*

Not using a grid system is not an option now that Responsive Web Design is all over the place. To make designs look consistent and solid across all sizes, we use some sort of grid to lay out the elements. To avoid having to code this grid work over and over again, some brilliant minds made theirs reusable.

Let me put this straight: I am not a big fan of grid systems. Of course I do see the potential, but I think most of them are completely overkill and are mostly used to draw red columns on a white background in nerdy designers’ speaker decks. When is the last time you thought *thank-God-I-have-this-tool-to-build-this-2-5-3.1-π-grid*? That’s right, never. Because in most cases, you just want the usual regular 12-columns grid, nothing fancy.

If you are using a CSS framework for your project like [Bootstrap](http://getbootstrap.com/) or [Foundation](http://foundation.zurb.com/), chances are high it includes a grid system already in which case I would recommend to use it to avoid having to deal with yet another dependency.

If you are not tied to a specific grid system, you will be pleased to know there are two top-notch Sass powered grid engines out there: [Susy](http://susy.oddbird.net/) and [Singularity](https://github.com/at-import/Singularity). Both do much more than you will ever need so you can pick the one you prefer between these two and be sure all your edge cases—even the most nifty ones—will be covered. If you ask me, Susy has a slightly better community, but that’s my opinion.

Or you can head over to something a bit more casual, like [csswizardry-grids](https://github.com/csswizardry/csswizardry-grids). All in all, the choice will not have much of an impact on your coding style, so this is pretty much up to you at this point.

### *SCSS-Lint*

Linting code is very important. Usually, following guidelines from a styleguide helps reducing the amount of code quality mistakes but nobody’s perfect and there are always things to improve. So you could say that linting code is as important as commenting it.

[SCSS-lint](https://github.com/causes/scss-lint) is a tool to help you keep your SCSS files clean and readable. It is fully customisable and easy to integrate with your own tools.

Fortunately, SCSS-lint recommendations are very similar to those described in this document. In order to configure SCSS-lint according to Sass Guidelines, may I recommend the following setup:

```yaml
linters:

  BangFormat:
    enabled: true
    space_before_bang: true
    space_after_bang: false

  BemDepth:
    enabled: true
    max_elements: 1

  BorderZero:
    enabled: true
    convention: zero

  ChainedClasses:
    enabled: false

  ColorKeyword:
    enabled: true

  ColorVariable:
    enabled: false

  Comment:
    enabled: false

  DebugStatement:
    enabled: true

  DeclarationOrder:
    enabled: true

  DisableLinterReason:
    enabled: true

  DuplicateProperty:
    enabled: false

  ElsePlacement:
    enabled: true
    style: same_line

  EmptyLineBetweenBlocks:
    enabled: true
    ignore_single_line_blocks: true

  EmptyRule:
    enabled: true

  ExtendDirective:
    enabled: false

  FinalNewline:
    enabled: true
    present: true

  HexLength:
    enabled: true
    style: short

  HexNotation:
    enabled: true
    style: lowercase

  HexValidation:
    enabled: true

  IdSelector:
    enabled: true

  ImportantRule:
    enabled: false

  ImportPath:
    enabled: true
    leading_underscore: false
    filename_extension: false

  Indentation:
    enabled: true
    allow_non_nested_indentation: true
    character: space
    width: 2

  LeadingZero:
    enabled: true
    style: include_zero

  MergeableSelector:
    enabled: false
    force_nesting: false

  NameFormat:
    enabled: true
    convention: hyphenated_lowercase
    allow_leading_underscore: true

  NestingDepth:
    enabled: true
    max_depth: 1

  PlaceholderInExtend:
    enabled: true

  PrivateNamingConvention:
    enabled: true
    prefix: _

  PropertyCount:
    enabled: false

  PropertySortOrder:
    enabled: false

  PropertySpelling:
    enabled: true
    extra_properties: []

  PropertyUnits:
    enabled: false

  PseudoElement:
    enabled: true

  QualifyingElement:
    enabled: true
    allow_element_with_attribute: false
    allow_element_with_class: false
    allow_element_with_id: false

  SelectorDepth:
    enabled: true
    max_depth: 3

  SelectorFormat:
    enabled: true
    convention: hyphenated_lowercase
    class_convention: '^(?:u|is|has)\-[a-z][a-zA-Z0-9]*$|^(?!u|is|has)[a-zA-Z][a-zA-Z0-9]*(?:\-[a-z][a-zA-Z0-9]*)?(?:\-\-[a-z][a-zA-Z0-9]*)?$'

  Shorthand:
    enabled: true

  SingleLinePerProperty:
    enabled: true
    allow_single_line_rule_sets: false

  SingleLinePerSelector:
    enabled: true

  SpaceAfterComma:
    enabled: true

  SpaceAfterPropertyColon:
    enabled: true
    style: one_space

  SpaceAfterPropertyName:
    enabled: true

  SpaceAfterVariableColon:
    enabled: true
    style: at_least_one_space

  SpaceAfterVariableName:
    enabled: true

  SpaceAroundOperator:
    enabled: true
    style: one_space

  SpaceBeforeBrace:
    enabled: true
    style: space
    allow_single_line_padding: true

  SpaceBetweenParens:
    enabled: true
    spaces: 0

  StringQuotes:
    enabled: true
    style: single_quotes

  TrailingSemicolon:
    enabled: true

  TrailingZero:
    enabled: true

  TransitionAll:
    enabled: false

  UnnecessaryMantissa:
    enabled: true

  UnnecessaryParentReference:
    enabled: true

  UrlFormat:
    enabled: false

  UrlQuotes:
    enabled: true

  VariableForProperty:
    enabled: false

  VendorPrefixes:
    enabled: true
    identifier_list: base
    include: []
    exclude: []

  ZeroUnit:
    enabled: true
```

If you are not convinced of the necessity to use SCSS-lint, I recommend reading these great articles: [Clean Up your Sass with SCSS-lint](http://blog.martinhujer.cz/clean-up-your-sass-with-scss-lint/), [Improving Sass code quality on theguardian.com](http://www.theguardian.com/info/developer-blog/2014/may/13/improving-sass-code-quality-on-theguardiancom) and [An Auto-Enforceable SCSS Styleguide](http://davidtheclark.com/scss-lint-styleguide/).

<blockquote class="note"><p>If you want to plug SCSS lint into your Grunt build process, you will be pleased to know there is a Grunt plugin for that called <a href="https://github.com/ahmednuaman/grunt-scss-lint">grunt-scss-lint</a>.</p><p>Also, if you are on the hunt for a neat application that works with SCSS-lint and the like, the guys at <a href="http://thoughtbot.com/">Thoughtbot</a> (Bourbon, Neat…) are working on <a href="https://houndci.com/">Hound</a>.</p></blockquote>

## Too Long; Didn’t Read

These guidelines are quite long and sometimes it is good to have them summed up in a shorter version. Below is this summary.

### *Key Principles*

- Having a styleguide is all about **consistency**. If you disagree with some rules from Sass Guidelines, fair enough as long as you are consistent. [↩](https://sass-guidelin.es/#why-a-styleguide)
- Sass should be kept as simple as it can be. Avoid building complex systems unless absolutely necessary. [↩](https://sass-guidelin.es/#key-principles)
- Keep in mind that sometimes *KISS* (Keep It Simple, Stupid) is better than *DRY* (Don’t Repeat Yourself). [↩](https://sass-guidelin.es/#key-principles)

### *Syntax & Formatting*

- An indentation is made of two (2) spaces, no tabs. [↩](https://sass-guidelin.es/#syntax--formatting)
- Lines should be, as much as possible, shorter than 80 characters. Feel free to split them into several lines when necessary. [↩](https://sass-guidelin.es/#syntax--formatting)
- CSS should be properly written, possibly following the [CSS Guidelines](http://cssguidelin.es/)from Harry Roberts. [↩](https://sass-guidelin.es/#syntax--formatting)
- Whitespace is free, use it to separate items, rules and declarations. Do not hesitate to leave empty lines, it never hurts. [↩](https://sass-guidelin.es/#syntax--formatting)

###### STRINGS

- Declaring the `@charset` directive on top of the stylesheet is highly recommended. [↩](https://sass-guidelin.es/#encoding)
- Unless applied as CSS identifiers, strings should be quoted using single quotes. URLs should also be quoted. [↩](https://sass-guidelin.es/#strings-as-css-values)

###### NUMBERS

- Sass makes no distinction between numbers, integers, floats so trailing zeros (0) should be omitted. However, leading zeros (0) help readability and should be added. [↩](https://sass-guidelin.es/#zeros)
- A zero (0) length should not have a unit. [↩](https://sass-guidelin.es/#units)
- Units manipulation should be thought as arithmetic operations, not string operations. [↩](https://sass-guidelin.es/#units)
- In order to improve readability, top-level calculations should be wrapped in parentheses. Also, complex math operations might be splitted into smaller chunks. [↩](https://sass-guidelin.es/#calculations)
- Magic numbers dramatically hurt code maintainability and should be avoided at all time. When in doubt, extensively explain the questionable value. [↩](https://sass-guidelin.es/#magic-numbers)

###### COLORS

- Colors should be expressed in HSL when possible, then RGB, then hexadecimal (in a lowercase and shortened form). Color keywords should be avoided. [↩](https://sass-guidelin.es/#color-formats)
- Prefer `mix(..)` instead of `darken(..)` and `lighten(..)` when lightening or darkening a color. [↩](https://sass-guidelin.es/#lightening-and-darkening-colors)

###### LISTS

- Unless used as a direct mapping to space-separated CSS values, lists should be separated with commas. [↩](https://sass-guidelin.es/#lists)
- Wrapping parentheses should also be considered to improve readability. [↩](https://sass-guidelin.es/#lists)
- Inlined lists should not have a trailing comma, multi-line lists should have it. [↩](https://sass-guidelin.es/#lists)

### *MAPS*

- Maps containing more than a single pair are written on several lines. [↩](https://sass-guidelin.es/#maps)
- To help maintainability, the last pair of a map should have a trailing comma. [↩](https://sass-guidelin.es/#maps)
- Map keys that happen to be strings should be quoted as any other string. [↩](https://sass-guidelin.es/#maps)

###### DECLARATION SORTING

- The system used for declaration sorting (alphabetical, by type, etc.) doesn’t matter as long as it is consistent. [↩](https://sass-guidelin.es/#declaration-sorting)

###### SELECTOR NESTING

- Avoid selector nesting when it is not needed (which represents most of the cases). [↩](https://sass-guidelin.es/#selector-nesting)
- Use selector nesting for pseudo-classes and pseudo-elements. [↩](https://sass-guidelin.es/#selector-nesting)
- Media queries can also be nested inside their relevant selector. [↩](https://sass-guidelin.es/#selector-nesting)

### *Naming Conventions*

- It is best to stick to CSS naming conventions which are (except a few errors) lowercase and hyphen-delimited. [↩](https://sass-guidelin.es/#naming-conventions)

### *Commenting*

- CSS is a tricky language; do not hesitate to write very extensive comments about things that look (or are) fishy. [↩](https://sass-guidelin.es/#commenting)
- For variables, functions, mixins and placeholders establishing a public API, use SassDoc comments. [↩](https://sass-guidelin.es/#documentation)

### *Variables*

- Do use the `!default` flag for any variable part of a public API that can be safely changed. [↩](https://sass-guidelin.es/#default-flag)
- Do not use the `!global` flag at root level as it might constitue a violation of Sass syntax in the future. [↩](https://sass-guidelin.es/#global-flag)

### *Extend*

- Stick to extending placeholders, not existing CSS selectors. [↩](https://sass-guidelin.es/#extend)
- Extend a placeholder as few times as possible in order to avoid side effects. [↩](https://sass-guidelin.es/#extend)