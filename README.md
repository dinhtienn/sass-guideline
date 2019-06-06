# Sass Guideline

*Nguồn: https://sass-guidelin.es/*

*Gitpage: https://dinhtienn.github.io/sass-guideline/*

## Hướng dẫn sử dụng Sass chuẩn mực, có khả năng bảo trì và mở rộng (mang quan điểm cá nhân).

### Dự án Sass Guidelines được dịch sang nhiều ngôn ngữ bởi [những người đóng góp](https://github.com/HugoGiraudel/sass-guidelines/issues/96).

## About The Author

Tên tôi là [Hugo Giraudel](http://hugogiraudel.com/), Tôi là một front-end developer người Pháp, gốc ở Berlin (Đức) từ năm 2015, hiện đang làm việc tại [N26](https://n26.com/).

Tôi đã viết Sass được vài năm nay và tôi là tác giả của nhiều dự án liên quan đến Sass như [SassDoc](http://sassdoc.com/), [SitePoint Sass Reference](http://sitepoint.com/sass-reference/) và [Sass-Compatibility](http://sass-compatibility.github.io/). Nếu bạn quan tâm nhiều hơn đến những đóng góp của tôi cho cộng đồng Sass, hãy xem qua [danh sách này](http://github.com/HugoGiraudel/awesome-sass).

Tôi cũng là tác giả của một cuốn sách về CSS (bằng tiếng Pháp) có tựa đề [CSS3 Pratique du Design Web](http://css3-pratique.fr/) (phiên bản *Eyrolles*), cũng như một cuốn sách về Sass (bằng Tiếng Anh) có tên [Jump Start Sass](https://learnable.com/books/jump-start-sass) (phiên bản *Learnable*).

## Contributing

Sass Guidelines là một dự án miễn phí mà tôi duy trì trong thời gian rảnh rỗi. Không cần phải nói, đó là một khối công việc khá lớn để giữ cho mọi thứ được cập nhật, được dẫn chứng và thích hợp. Rất may, tôi nhận được sự đóng góp của rất nhiều người tuyệt vời đặc biệt là việc duy trì hàng tá các bản dịch khác nhau. Hãy chắc chắn rằng cảm ơn họ nhé!

Nếu bạn muốn đóng góp vào dự án, vui lòng tweet nó, truyền bá hoặc sửa từng lỗi đánh máy nhỏ bằng cách mở ra một issue hoặc pull-request trên [GitHub repository](https://github.com/HugoGiraudel/sass-guidelines) sẽ là rất tuyệt vời!

Cuối cùng nhưng không kém phần quan trọng trước khi ta bắt đầu: Nếu bạn thích tài liệu này hoặc nó hữu ích cho bạn hoặc team của bạn, vui lòng xem xét việc hỗ trợ để tôi có thể tiếp tục làm việc với nó!

## About Sass

Đây là cách [Sass](http://sass-lang.com/) được mô tả trong [documentation](http://sass-lang.com/documentation/file.SASS_REFERENCE.html) của nó:

> Sass là một phần mở rộng của CSS tăng thêm sức mạnh và sự thanh lịch tới ngôn ngữ cơ bản.

Mục tiêu cuối cùng của `Sass` là hỗ trợ những thiếu xót của CSS. CSS, như chúng ta đã biết, không phải là ngôn ngữ tốt nhất trên thế giới [cần dẫn nguồn]. Mặc dù rất đơn giản để học, nó có thể nhanh chóng trở nên khá lộn xộn, đặc biệt là trong các dự án lớn.

Đó là lý do Sass xuất hiện, như một meta-language, để cải thiện cú pháp của CSS nhằm cung cấp các tính năng bổ sung và các công cụ tiện dụng. Trong khi đó, Sass muốn bảo tồn về ngôn ngữ CSS.

Điều này không biến CSS trở thành một ngôn ngữ lập trình đầy đủ tính năng; Sass chỉ muốn giúp đỡ những nơi CSS thất bại. Chính về điều này, khởi đầu với Sass không khó hơn việc học CSS, nó đơn giản là thêm một vài [tính năng bổ sung](http://sitepoint.com/sass-reference/) trên đầu của nó.

Điều đó có nghĩa rằng, có nhiều cách để sử dụng những tính năng này. Một vài chỗ tốt, một vài chỗ tệ, một số bất bình thường. Các hướng dẫn này nhằm cung cấp cho bạn một cách tiếp cận nhất quán và được dẫn chứng rõ ràng để viết code Sass.

### *Ruby Sass Or LibSass*

[Commit đầu tiên của Sass](https://github.com/hcatlin/sass/commit/fa5048ba405619273e474a50400c7243fbff54fe), trở lại vào cuối năm 2016, hơn 10 năm trước. Không cần phải nói nó đã đi một chặng đường dài kể từ đó. Ban đầu được phát triển trên Ruby, các port khác nhau xuất hiện ở đây đó. Phiên bản thành công nhất, [LibSass](http://webdesign.tutsplus.com/articles/getting-to-know-libsass--cms-23114) (được viết bằng C/C++) hiện đã gần như tương thích hoàn toàn với phiên bản Ruby gốc.

Vào năm 2014, [các team Ruby Sass và LibSass đã quyết định chờ đợi cả hai phiên bản đồng bộ hoá trước khi chuyển tiếp](https://github.com/sass/libsass/wiki/The-LibSass-Compatibility-Plan). Kể từ đó, LibSass đã tích cực phát hành các phiên bản để có tính năng tương đương với các phiên bản cũ hơn của nó. Những mâu thuẫn còn lại của nó được tôi thu thập và liệt kê tại dự án [Sass-Compatibility](http://sass-compatibility.github.io/). Nếu bạn nhận thấy sự không tương thích giữa hai phiên bản mà không được liệt kê, vui lòng mở ra một issue.

Quay trở lại chọn trình biên dịch. Trên thực tế, tất cả đều phụ thuộc vào dự án của bạn. Nếu nó là một dự án Ruby on Rails, tốt nhất bạn nên sử dụng Ruby Sass là hoàn toàn phù hợp. Ngoài ra, hãy lưu ý rằng Ruby Sass sẽ luôn là bản triển khai tham chiếu và sẽ luôn dẫn đầu LibSass về các tính năng. Và nếu bạn đang tìm cách [chuyển từ Ruby Sass sang LibSass](http://www.sitepoint.com/switching-ruby-sass-libsass/), bài viết này là dành cho bạn.

Trong các dự án không phải Ruby cần tích hợp quy trình làm việc, LibSass có lẽ là một ý tưởng tốt hơn vì nó chủ yếu dành riêng cho việc được bao bọc. Vì vậy, nếu bạn muốn sử dụng, cùng nói về Node.js [node-sass](https://github.com/sass/node-sass) đều được chọn.

### *Sass or SCSS*

Có khá nhiều nhầm lẫn về ngữ nghĩa của cái tên *Sass*, và câu trả lời xác đáng nhất: Sass mang nghĩa là cả bộ tiền xử lý và cú pháp của chính nó. Có vẻ nó không thích hợp lắm phải không?

Bạn thấy đấy, Sass ban đầu mô tả một cú pháp trong đó sự hạn chế riêng biệt chính là sự nhạy cảm indent của nó. Ngay sau đó, những người duy trì Sass đã quyết định thu hẹp khoảng cách giữa Sass và CSS bằng cách cung cấp một cú pháp thân thiện với CSS có tên là *SCSS* nghĩa là *Sassy CSS*. Phương châm của nó là: nếu CSS hợp lệ, SCSS cũng hợp lệ.

Kể từ đó, Sass (bộ tiền xử lý) đã cung cấp [hai cú pháp khác nhau](http://www.sitepoint.com/whats-difference-sass-scss/): Sass (not all-caps, [please](http://sassnotsass.com/)), còn được gọi là *cú pháp thụt lề*, và SCSS. Sử dụng cái nào là tuỳ thuộc vào bạn vì cả hai đều tương đương nhau về tính năng. Nó chỉ là vấn đề thẩm mỹ tại thời điểm này.

Cú pháp nhạy cảm với khoảng trắng của Sass, dựa vào thụt lề để loại bỏ dấu ngoặc, dấu chấm phẩy và các ký hiệu dấu chấm câu khác, dẫn đến cú pháp gọn và ngắn hơn. Trong khi đó, SCSS dễ học hơn vì nó chủ yếu là một số bit thừa nhỏ trên CSS.

Cá nhân tôi, thích SCSS hơn Sass vì nó gần với CSS hơn và thân thiện hơn với hầu hết các nhà phát triển. Do đó, SCSS là cú pháp mặc địch trong suốt hướng dẫn này. Bạn có thể chuyển sang cú pháp thụt lề Sass trong bảng điều khiển bên.

### *Các bộ tiền xử lý khác*

Sass là một tiền xử lý trong số những bộ tiền xử lý khác. Đối thủ nặng ký nhất của nó là [Less](http://lesscss.org/), một bộ tiền xử lý dựa trên Node.js đã trở nên khá phổ biến nhờ khung CSS nổi tiếng [Bootstrap](http://getbootstrap.com/) sử dụng nó (cho đến phiên bản 4). Ngoài ra còn có [Stylus](http://learnboost.github.io/stylus/), một bộ tiền xử lý rất dễ được chấp nhận và linh hoạt tuy nhiên hơi khó sử dụng và với một cộng đồng nhỏ hơn.

*Tại sao lại chọn Sass hơn bất kỳ bộ tiền xử lý nào khác?* vẫn là một câu hỏi xác đáng ngày nay. Cách đây không lâu, chúng tôi đã từng đề xuất Sass cho các dự án dựa trên Ruby vì nó lần đầu tiên được tạo ra trong Ruby và kết hợp tốt với Ruby on Rails. Hiện tại LibSass đã bắt kịp (chủ yếu) với Sass ban đầu, đây không còn là lời khuyên thích hợp.

Những gì tôi thích ở Sass là cách tiếp cận bảo toàn của nó với CSS. Thiết kế của Sass dựa trên các nguyên tắc mạnh mẽ: phần lớn phương pháp thiết kế xuất phát tự nhiên từ niềm tin của các team cốt lõi rằng thêm các tính năng bổ sung có chi phí phức tạp cần được chứng minh bằng tính hữu dụng và về những gì một block style cho trước đang làm bằng cách chỉ nhìn vào riêng khối đó. Ngoài ra, Sass có sự chú ý sắc nét hơn nhiều so với các bộ tiền xử lý khác. Theo tôi, có thể nói rằng các nhà thiết kế cốt lõi quan tâm sâu sắc đến việc hỗ trợ mọi trường hợp tương thích CSS và đảm bảo mọi hành vi chung đều nhất quán. Nói cách khác, Sass là một phần mềm nhằm giải quyết các vấn đề thực tế, giúp cung cấp chức năng hữu ích cho những thiếu xót của CSS.

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

Rõ ràng, đây chắc chắn không phải là cách duy nhất để làm việc, và nó có thể có hoặc không phù hợp với dự án của bạn. Hãy chọn từ nó những thứ thích hợp với nhu cầu của bạn. Như ta vẫn thường nói *your mileage may vary*.

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

Tôi phải nói rằng mình không thể tự quyết định. Một [cuộc thăm dò gần đây về CSS-Tricks](http://css-tricks.com/poll-results-how-do-you-order-your-css-properties/) đã xác định rằng hơn 45% developer đặt hàng khai báo theo loại chống lại 14% theo thứ tự abc. Ngoài ra, có 39% hoàn toàn ngẫu nhiên, bao gồm cả bản thân tôi.

<figure role="group" style="text-align: center"> <img width="700" height="308" alt="Chart showing how developers order their CSS declarations " src="https://d33wubrfki0l68.cloudfront.net/189c15208fdc614be2ca324c26ec14350f591a30/56132/assets/images/css-order-chart.png"><figcaption>Biểu đồ cho thấy cách các developer đặt hàng khai báo CSS của họ</figcaption></figure>

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

Trong phần này, chúng tôi sẽ không giải quyết các quy ước đặt tên CSS tốt nhất về khả năng duy trì và mở rộng; ngoài việc tùy thuộc vào bạn, nó còn nằm ngoài phạm vi của một Sass styleguide. Tôi đề xuất những bài viết theo [CSS Guidelines](http://cssguidelin.es/#naming-conventions).

Có một vài thứ bạn có thể đặt tên trong Sass và điều quan trọng là phải đặt tên cho chúng thật tốt để toàn bộ codebase trông vừa nhất quán vừa dễ đọc:

- Biến;
- Hàm;
- Mixin.

Các Sass placeholder được cố tình bỏ qua khỏi danh sách này vì chúng có thể được coi là các CSS selector thông thường, do đó tuân theo cùng kiểu đặt tên như các lớp.

Về các biến, hàm và mixin, chúng tôi dính vào một cái gì đó rất *CSS-y*: **chữ viết thường được phân cách bằng dấu gạch ngang**, và trên hết là có ý nghĩa.

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

Nếu bạn tình cờ là một framework developer hoặc nhà văn thư viện, bạn có thể thấy mình xử lý các biến không có nghĩa là được cập nhật trong mọi trường hợp: hằng số. Thật không may (hoặc may mắn thay?), Sass không cung cấp bất kỳ cách nào để xác định các thực thể đó, vì vậy chúng tôi phải tuân theo các quy ước đặt tên nghiêm ngặt để đưa ra quan điểm của mình.

Đối với nhiều ngôn ngữ, tôi đề xuất tất cả các biến snakerized khi chúng là hằng số. Đây không chỉ là một quy ước rất cũ, mà nó còn tương phản tốt với các biến gạch nối thấp hơn thông thường.

```scss
// Yep
$CSS_POSITIONS: (top, right, bottom, left, center);

// Nope
$css-positions: (top, right, bottom, left, center);
```

Nếu bạn thật sự muốn sử dụng các ý tưởng của hằng số trong Sass, bạn nên đọc [bài viết dành riêng này](http://www.sitepoint.com/dealing-constants-sass/).

### *Namespace*

Nếu bạn có ý định phân phối code Sass của mình, trong trường hợp thư viện, framework, grid system hoặc bất cứ điều gì, bạn có thể muốn xem xét việc đặt tên cho tất cả các biến, hàm, mixin và placeholder của mình để nó không xung đột với code của bất kỳ ai khác.

Ví dụ, nếu bạn làm việc trong dự án *Sassy Unicorn* có nghĩa là được phân phối, bạn có thể xem xét sử dụng `su-` làm namespace. Nó là đủ cụ thể để ngăn chặn bất kỳ xung đột đặt tên và đủ ngắn để không phải là một sự cố gắng để viết.

```scss
$su-configuration: ( … );

@function su-rainbow($unicorn) {
  // …
}
```

[Kaelig](http://kaelig.fr/) có [một bài viết rất sâu sắc về CSS namespace](http://blog.kaelig.fr/post/44554267597/please-respect-the-global-css-namespace), trong trường hợp chủ đề này ngẫu nhiên lại được bạn quan tâm.

<blockquote class="note"><p>Lưu ý rằng namespace tự động chắc chắn là một mục tiêu thiết kế cho cải tiến <code>@import</code> sắp tới từ Sass 4.0. Khi nó đến gần hơn với kết quả, nó sẽ ngày càng ít hữu ích hơn để thực hiện namespace thủ công, cuối cùng, các thư viện được đặt tên thủ công thực sự có thể khó sử dụng hơn.</p></blockquote>

## Commenting

CSS là một ngôn ngữ phức tạp, đầy những thủ thuật và kỳ quặc. Chính vì điều này, nó nên được comment rất nhiều, đặc biệt nếu bạn hoặc ai đó có ý định đọc và cập nhật code 6 tháng hoặc 1 năm kể từ bây giờ. Đừng đặt bạn hoặc bất kỳ ai khác ở vị trí của *I-didn’t-write-this-oh-my-god-why*.

Đơn giản như CSS có thể nhận được, vẫn còn rất nhiều chỗ để comment. Đây có thể là giải thích:

- Cấu trúc và / hoặc vai trò của một tập tin;
- Mục tiêu của một quy tắc;
- Ý tưởng đằng sau một magic number;
- Lý do cho một thuộc tính CSS;
- Thứ tự khai báo CSS;
- Quá trình suy nghĩ đằng sau một cách làm việc.

Và tôi có lẽ đã quên rất nhiều lý do khác nhau. Comment mất rất ít thời gian khi được thực hiện liền mạch cùng với code vì vậy hãy thực hiện nó đúng lúc. Trở lại với một đoạn code để comment nó không chỉ hoàn toàn phi thực tế mà còn vô cùng khó chịu.

### *Writing Comments*

Lý tưởng nhất, *bất kỳ* quy tắc CSS nào phải được đi trước bởi một nhận xét kiểu C giải thích đặc điểm của khối CSS. Comment này cũng lưu trữ các giải thích được đánh số liên quan đến các phần cụ thể của quy tắc. Ví dụ:

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

Về cơ bản mọi thứ không rõ ràng khi thoạt nhìn nên được comment. Không có những thứ như quá nhiều tài liệu. Hãy nhớ rằng bạn không thể *comment quá nhiều*, vì vậy hãy tiếp tục và viết comment cho mọi thứ đáng giá.

Khi comment một phần dành riêng cho Sass, hãy sử dụng các comment nội tuyến Sass thay vì khối kiểu C. Điều này làm cho comment vô hình ở đầu ra, ngay cả trong chế độ mở rộng trong quá trình phát triển.

```scss
// Add current module to the list of imported modules.
// `!global` flag is required so it actually updates the global variable.
$imported-modules: append($imported-modules, $module) !global;
```

Lưu ý rằng cách thực hiện này cũng được CSS Guidelines hỗ trợ trong phần [Commenting](http://cssguidelin.es/#commenting).

### *Documentation*

Mọi biến, hàm, mixin và placeholder được dự định sẽ được sử dụng lại trên toàn bộ codebase phải được ghi lại như một phần của API toàn cục bằng cách sử dụng [SassDoc](http://sassdoc.com/).

```scss
/// Vertical rhythm baseline used all over the code base.
/// @type Length
$vertical-rhythm-baseline: 1.5rem;
```

<blockquote class="note"><p>Ba dấu gạch chéo (<code>/</code>) là cần thiết.</p></blockquote>

SassDoc có hai vai trò chính:

- Buộc các comment được tiêu chuẩn hóa bằng cách sử dụng một hệ thống dựa trên chú thích cho mọi thứ thuộc về API công khai hoặc riêng tư;
- Có thể tạo phiên bản HTML của tài liệu API bằng cách sử dụng bất kỳ trình dịch SassDoc nào (công cụ CLI, Grunt, Gulp, Broccoli, Node mật).

<figure role="group" style="text-align: center"> <img data-proofer-ignore="" alt="Documentation generated by SassDoc " sizes="100vw" srcset="https://d33wubrfki0l68.cloudfront.net/68a6846edb356c44cb53dda05760797b2d1baf81/c2a92/assets/images/sassdoc-preview_small.png 540w, https://d33wubrfki0l68.cloudfront.net/97984b488095bfee6f2c6e47c500915b665cfe86/5aa53/assets/images/sassdoc-preview_medium.png 900w, https://d33wubrfki0l68.cloudfront.net/c5894fe21ae4828475ba1483a6fb1d94e151a3d5/4d6c5/assets/images/sassdoc-preview_large.png 1200w, https://d33wubrfki0l68.cloudfront.net/a73c466f7ea902521035603506888db0af2c8e3d/0aa5a/assets/images/sassdoc-preview_huge.png 1590w"><figcaption>Documentation generated by SassDoc</figcaption></figure>

Dưới đây là một ví dụ về một mixin được ghi lại rộng rãi với SassDoc:

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

Kiến trúc một dự án CSS có lẽ là một trong những điều khó khăn nhất mà bạn sẽ phải làm trong suốt vòng đời của dự án. Giữ kiến trúc nhất quán và có ý nghĩa thậm chí còn khó hơn.

May mắn thay, một trong những lợi ích chính của việc sử dụng bộ tiền xử lý CSS là có khả năng phân tách codebase trên một số tệp mà không ảnh hưởng đến hiệu suất (như chỉ thị CSS `@import` đã làm). Nhờ có overload của Sass qua chỉ thị `@import`, nên hoàn toàn an toàn (và thực sự được khuyến nghị) để sử dụng nhiều tệp khi cần thiết trong quá trình phát triển, tất cả được biên dịch thành một bản định kiểu duy nhất khi đi vào production.

Trên hết, tôi không thể nhấn mạnh đủ nhu cầu cho các thư mục, ngay cả trên các dự án quy mô nhỏ. Ở nhà, bạn không lồng thả từng sheet vào cùng một box. Bạn sử dụng các thư mục; Một cho nhà / căn hộ, một cho ngân hàng, một cho hóa đơn, vv. Không có lý do để làm khác khi cấu trúc một dự án CSS. Tách codebase thành các thư mục riêng biệt có ý nghĩa để dễ dàng tìm thấy nội dung sau này khi bạn phải quay lại code.

Có [rất nhiều kiến trúc phổ biến](http://www.sitepoint.com/look-different-sass-architectures/) cho những dự án CSS: [OOCSS](http://www.smashingmagazine.com/2011/12/12/an-introduction-to-object-oriented-css-oocss/), [Atomic Design](http://bradfrost.com/blog/post/atomic-web-design/), [Bootstrap](http://getbootstrap.com/)-like, [Foundation](http://foundation.zurb.com/)-like… Tất cả đều có ưu và nhược điểm riêng

Bản thân tôi sử dụng một cách tiếp cận khá giống với [SMACSS](https://smacss.com/) từ [Jonathan Snook](http://snook.ca/), trong đó tập trung vào việc giữ mọi thứ đơn giản và rõ ràng.

<blockquote class="note"><p>Tôi đã học được rằng kiến trúc chiếm hầu hết thời gian của dự án. Vui lòng loại bỏ hoàn toàn hoặc điều chỉnh giải pháp được đề xuất để giải quyết một hệ thống phù hợp với nhu cầu của bạn.</p></blockquote>

### *Components*

Có một sự khác biệt lớn giữa việc làm cho nó *hoạt động* và làm cho nó *tốt*. Một lần nữa, CSS là một ngôn ngữ khá lộn xộn [cần dẫn nguồn]. CSS càng ít, càng vui. Chúng ta không muốn đối phó với megabyte của code CSS. Để giữ cho các stylesheet ngắn và hiệu quả, và điều này sẽ không gây bất ngờ cho bạn, bạn nên nghĩ về giao diện là một bộ sưu tập các component.

Các component có thể là bất cứ thứ gì, miễn là chúng:

- Làm một việc và một việc duy nhất;
- Được tái sử dụng và tái sử dụng trên toàn dự án;
- Độc lập.

Ví dụ, một search form nên được coi là một component. Nó nên được tái sử dụng, ở các vị trí khác nhau, trên các trang khác nhau, trong các tình huống khác nhau. Nó không nên phụ thuộc vào vị trí của nó trong DOM (footer, sidebar, main content).

Hầu hết mọi giao diện đều có thể được coi là các component nhỏ và tôi thực sự khuyên bạn nên tuân thủ mô hình này. Điều này sẽ không chỉ rút ngắn lượng CSS cần thiết cho toàn bộ dự án, mà còn dễ bảo trì hơn nhiều so với một mớ hỗn độn nơi mọi thứ đều rối loạn.

### *Component Structure*

Lý tưởng nhất là các component nên tồn tại trong một phần Sass của riêng chúng (trong thư mục `component/`, như được mô tả trong [7-1 pattern](https://sass-guidelin.es/#the-7-1-potype)), chẳng hạn như `component/ _button.scss`. Các style được mô tả trong mỗi tệp component chỉ nên được quan tâm với:

- Style của chính component đó;
- Style của các biến thể component, bộ sửa đổi và /hoặc trạng thái component;
- Style của các hậu duệ của component (tức là con), nếu cần thiết.

Nếu bạn muốn các component của mình có thể được theo theme bên ngoài (ví dụ: từ một theme bên trong thư mục `Themes/`), hãy giới hạn các khai báo chỉ các style cấu trúc, chẳng hạn như kích thước (width/height), padding, margin, alignment, v.v. . Loại trừ các style như color, shadows, quy tắc font, quy tắc background, v.v.

Một phần component có thể bao gồm các biến component cụ thể, placeholder và thậm chí cả mixin và function. Tuy nhiên, hãy nhớ rằng bạn nên tránh tham chiếu các tệp component (ví dụ: `@ import`-ing) từ các tệp component khác, vì điều này có thể làm cho biểu đồ phụ thuộc của dự án của bạn trở thành một mớ hỗn độn dễ nhầm lẫn.

Dưới đây là một ví dụ về một phần component button:

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

<blockquote class="note"><p>Cảm ơn <a href="https://twitter.com/davidkpiano">David Khourshid</a> vì sự giúp đỡ và chuyên môn trong phần này.</p></blockquote>

### *The 7-1 Pattern*

Quay lại với kiến trúc, tôi thường nói về những gì tôi gọi là  *7-1 pattern*: 7 thư mục, 1 tệp. Về cơ bản, bạn có tất cả các phần của mình được nhồi vào 7 thư mục khác nhau và một tệp duy nhất ở cấp gốc (thường được đặt tên là `main.scss`) để nhập tất cả chúng để được biên dịch thành CSS stylesheet.

- `base/`
- `components/`
- `layout/`
- `pages/`
- `themes/`
- `abstracts/`
- `vendors/`

Và dĩ nhiên:

- `main.scss`

<blockquote class="note"><p>Nếu bạn đang tìm cách sử dụng 7-1 pattern, đã có sẵn một <a href="https://github.com/HugoGiraudel/sass-boilerplate">boilerplate</a> trên GitHub. Nó chứa mọi thứ bạn cần để bắt đầu với kiến trúc này.</p></blockquote>

<figure role="group" style="text-align: center"> <img data-proofer-ignore="" alt="Wallpaper by Julien He " sizes="100vw" srcset="https://d33wubrfki0l68.cloudfront.net/83050df0f35e960a4fc2bb0b0f8df68ee25ab80a/d4b00/assets/images/sass-wallpaper_small.jpg 540w, https://d33wubrfki0l68.cloudfront.net/6687589e656a32ecb7780d13fac82a67cd8c679d/e3e38/assets/images/sass-wallpaper_medium.jpg 900w, https://d33wubrfki0l68.cloudfront.net/c0f986a6a230f667e2b180436899ffe86c29f33c/03f50/assets/images/sass-wallpaper_large.jpg 1200w, https://d33wubrfki0l68.cloudfront.net/2cc0bf5eb77112d83166f6324013ba157139ae24/8e392/assets/images/sass-wallpaper_huge.jpg 1590w"><figcaption>Wallpaper by <a href="https://twitter.com/julien_he">Julien He</a></figcaption></figure>

Lý tưởng nhất, ta có thể đưa ra một cái gì đó trông như thế này:

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

<blockquote class="note"><p>Các tệp tuân theo các quy ước đặt tên giống như được mô tả ở trên: chúng được phân cách bằng dấu gạch nối.</p></blockquote>

###### BASE FOLDER

Thư mục `base/` chứa những gì chúng ta có thể gọi là code soạn sẵn cho dự án. Trong đó, bạn có thể tìm thấy tệp đặt lại, một số quy tắc chính tả và có thể là stylesheet xác định một số style chuẩn cho các phần tử HTML thường được sử dụng (mà tôi muốn gọi là `_base.scss`).

- `_base.scss`
- `_reset.scss`
- `_typography.scss`

<blockquote class="note"><p>Nếu dự án của bạn sử dụng <em>quả nhiều</em> CSS animation, bạn có thể xem xét thêm tệp <code>\_animations.scss</code> trong đó chứa các định nghĩa <code>@keyframes</code> của tất cả các animation của bạn. Nếu bạn chỉ sử dụng chúng một cách rời rạc, hãy cứ đặt chúng dọc theo các selector sử dụng chúng.</p></blockquote>

###### LAYOUT FOLDER

Thư mục `layout/` chứa mọi thứ tham gia vào việc bố trí trang web hoặc ứng dụng. Thư mục này có thể có các stylesheet cho các phần chính của trang web (header, footer, navigation, sidebar, ...), grid systemi hoặc thậm chí các CSS style cho tất cả các biểu mẫu.

- `_grid.scss`
- `_header.scss`
- `_footer.scss`
- `_sidebar.scss`
- `_forms.scss`
- `_navigation.scss`

<blockquote class="note"><p>Thư mục <code>layout/</code> cũng có thể được gọi là <code>partials/</code>, tuỳ thuộc ý thích của bạn.</p></blockquote>

###### COMPONENTS FOLDER

Đối với các thành phần nhỏ hơn, ta có thư mục `components/`. Trong khi `layout/` là * macro * (xác định wireframe toàn cục), thì `components/` tập trung nhiều hơn vào các widget. Nó chứa tất cả các loại module cụ thể như slider, loader, widget và về cơ bản là bất cứ thứ gì tương tự như vậy. Thường có rất nhiều tệp trong `components/` vì toàn bộ trang web / ứng dụng nên chủ yếu bao gồm các module nhỏ.

- `_media.scss`
- `_carousel.scss`
- `_thumbnails.scss`

<blockquote class="note"><p>Thư mục <code>components/</code> có thể được đặt là  <code>modules/</code>, tuỳ thuộc vào ý thích của bạn.</p></blockquote>

###### PAGES FOLDER

If you have page-specific styles, it is better to put them in a `pages/` folder, in a file named after the page. For instance, it’s not uncommon to have very specific styles for the home page hence the need for a `_home.scss` file in `pages/`.

Nếu bạn có style dành riêng cho trang, tốt hơn là đặt chúng vào thư mục `pages/`, trong một tệp có tên sau trang. Chẳng hạn, không có gì lạ khi có các style rất cụ thể cho trang chủ do đó cần có tệp `_home.scss` trong` pages/`.

- `_home.scss`
- `_contact.scss`

<blockquote class="note"><p>Tùy thuộc vào quá trình triển khai của bạn, các tệp này có thể được gọi riêng để tránh hợp nhất chúng với các tệp khác trong stylesheet kết quả. Nó thực sự là tùy thuộc vào bạn.</p></blockquote>

###### THEMES FOLDER

Trên các trang web và ứng dụng lớn, không có gì lạ khi có các chủ đề khác nhau. Chắc chắn là có nhiều cách khác nhau để xử lý các chủ đề nhưng cá nhân tôi thích có tất cả chúng trong một thư mục `Themes/`.

- `_theme.scss`
- `_admin.scss`

<blockquote class="note"><p>Điều này rất đặc biệt và có khả năng không tồn tại trên nhiều dự án.</p></blockquote>

###### ABSTRACTS FOLDER

Thư mục `abstracts/` tập hợp tất cả các công cụ và helper Sass được sử dụng trên toàn dự án. Mỗi biến toàn cục, hàm, mixin và placeholder nên được đặt ở đây.

Nguyên tắc chung cho thư mục này là nó không nên xuất một dòng CSS nào khi được biên dịch riêng. Nó không có vai trò gì ngoài việc củng cố Sass.

- `_variabled.scss`
- `_mixins.scss`
- `_fiances.scss`
- `_placeholder.scss`

Khi làm việc trong một dự án rất lớn với nhiều tiện ích trừu tượng, sẽ rất thú vị khi nhóm chúng theo chủ đề thay vì kiểu, ví dụ như kiểu chữ (`_typography.scss`), theo chủ đề (` _theming.scss`), v.v. tập tin chứa tất cả các helper liên quan: variable, function, mixins và placeholder. Làm như vậy có thể làm cho code dễ duyệt và bảo trì hơn, đặc biệt là khi các tệp đang trở nên rất dài.

<blockquote class="note"><p>Thư mục <code>abstracts/</code> có thể được đặt là <code>utilities/</code> hoặc <code>helpers/</code>, tuỳ thuộc vào bạn thích cái nào hơn.</p></blockquote>

###### VENDORS FOLDER

Và cuối cùng nhưng không kém phần quan trọng, hầu hết các dự án sẽ có thư mục `vendors/` chứa tất cả các tệp CSS từ các thư viện và framework bên ngoài - Normalize, Bootstrap, jQueryUI, FancyCarouselSliderjQueryPowered, v.v. Đặt những thứ đó sang một bên trong cùng một thư mục là một cách hay để nói rằng "Hey, code này không phải từ tôi, không phải code của tôi, không phải trách nhiệm của tôi".

- `_nnormalize.scss`
- `_bootstrap.scss`
- `_jquery-ui.scss`
- `_select2.scss`

Nếu bạn phải ghi đè một phần của bất kỳ vendor nào, tôi khuyên bạn nên có một thư mục thứ 8 có tên là 'vendors-extensions / ` trong đó bạn có thể có các tệp được đặt tên chính xác theo nhà cung cấp mà họ ghi đè.

Chẳng hạn, `nhà vendors-extensions/_bootstrap.scss` là một tệp chứa tất cả các quy tắc CSS nhằm khai báo lại một số CSS mặc định của Bootstrap. Điều này là để tránh tự chỉnh sửa các tập tin nhà cung cấp, thường không phải là một ý tưởng tốt.

###### MAIN FILE

Tệp chính (thường được gắn nhãn `main.scss`) phải là tệp Sass duy nhất trong toàn bộ codebase không bắt đầu bằng dấu gạch dưới. Tệp này không được chứa bất cứ thứ gì ngoài `@import` và các comment.

Các tệp nên được nhập theo thư mục mà chúng tồn tại, lần lượt theo thứ tự sau:

1. `abstracts/`
2. `vendors/`
3. `base/`
4. `layout/`
5. `components/`
6. `pages/`
7. `themes/`

Để duy trì khả năng đọc, tệp chính cần tôn trọng các nguyên tắc sau:

- Một tệp cho mỗi `@import`;
- Một `@import` trên mỗi dòng;
- Không có dòng mới giữa hai lần nhập từ cùng một thư mục;
- Một dòng mới sau lần nhập cuối cùng từ một thư mục;
- Phần mở rộng tập tin và dấu gạch dưới hàng đầu bị bỏ qua.

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

Có một cách khác để nhập các phần mà tôi cho là hợp lệ. Về mặt tươi sáng, nó làm cho tập tin dễ đọc hơn. Mặt khác, nó làm cho việc cập nhật nó hơi đau đớn hơn. Dù sao, tôi sẽ cho phép bạn quyết định cái nào là tốt nhất, nó không quan trọng lắm. Đối với cách làm này, tệp chính phải tôn trọng các nguyên tắc sau:

- Một `@import` cho mỗi thư mục;
- Ngắt dòng sau `@import`;
- Mỗi tệp trên dòng riêng của nó;
- Một dòng mới sau lần nhập cuối cùng từ một thư mục;
- Phần mở rộng tập tin và dấu gạch dưới hàng đầu bị bỏ qua.

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

Trong lập trình máy tính, các pattern toàn cục chỉ định các tên tệp có ký tự đại diện, chẳng hạn như `*.scss`. Ở một mức độ chung, globalbing có nghĩa là khớp một tập hợp các tệp dựa trên biểu thức thay vì danh sách tên tệp. Khi được áp dụng cho Sass, điều đó có nghĩa là nhập các phần vào [tệp chính](https://sass-guidelin.es/#main-file) với mẫu hình cầu thay vì liệt kê riêng lẻ. Điều này sẽ dẫn đến một tệp chính trông như thế này:

```scss
@import 'abstracts/*';
@import 'vendors/*';
@import 'base/*';
@import 'layout/*';
@import 'components/*';
@import 'pages/*';
@import 'themes/*';
```

Sass không hỗ trợ tập tin toàn cục vì nó có thể là một tính năng nguy hiểm vì CSS được biết là phụ thuộc vào thứ tự. Khi nhập động các tệp (thường đi theo thứ tự bảng chữ cái), người ta không kiểm soát thứ tự nguồn nữa, điều này có thể dẫn đến khó gỡ lỗi tác dụng phụ.

Điều đó đang được đề cập đến, trong một kiến trúc dựa trên thành phần nghiêm ngặt, đặc biệt cẩn thận không rò rỉ bất kỳ style nào từ bộ phận này sang bộ phận khác, thứ tự sẽ không thực sự quan trọng nữa, điều này sẽ cho phép import toàn cục. Điều này sẽ giúp dễ dàng thêm hoặc xóa các phần vì việc cập nhật cẩn thận tệp chính sẽ không còn cần thiết nữa.

Khi sử dụng Ruby Sass, có một Ruby gem được gọi là [sass-continbing](https://github.com/chriseppstein/sass-globbing) cho phép thực hiện chính xác hành vi đó. Nếu chạy trên node-sass, người ta có thể dựa vào Node.js hoặc bất kỳ công cụ xây dựng nào họ sử dụng để xử lý việc biên dịch (Gulp, Grunt, v.v.).

### *Shame File*

Có một khái niệm thú vị đã được phổ biến bởi [Harry Roberts](http://csswizardry.com/), [Dave Rupert](http://daverupert.com/) và [Chris Coyier](http: // css-tricks.com/) bao gồm việc đưa tất cả các khai báo CSS, hack và những thứ chúng tôi không tự hào về [tệp xấu hổ](http://csswizardry.com/2013/04/shame-css-full-net -phỏng vấn/). Tệp này, có tiêu đề rõ ràng là `_shame.scss`, sẽ được nhập sau bất kỳ tệp nào khác, ở cuối biểu định kiểu.

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

Tôi không nghĩ rằng chúng ta vẫn cần phải giới thiệu về Responsive Web Design nữa vì nó đã có ở khắp mọi nơi. Tuy nhiên, bạn có thể tự hỏi *tại sao lại có một phần về RWD trong Sass styleguide?* Trên thực tế có khá nhiều điều có thể được thực hiện để làm việc với các breakpoint dễ dàng hơn, vì vậy tôi nghĩ rằng sẽ không phải là một ý tưởng tồi để liệt kê nó ra đây

### *Naming Breakpoints*

Tôi nghĩ rằng hoàn toàn hợp lý khi nói rằng các media query không nên được gắn với các thiết bị cụ thể. Ví dụ, đây chắc chắn là một ý tưởng tồi để thử nhắm mục tiêu cụ thể vào iPad hoặc điện thoại Blackberry. Các media query nên quan tâm đến một loạt các kích thước màn hình, cho đến khi thiết kế bị hỏng và media query tiếp theo sẽ tiếp tục đè lên.

Vì những lý do tương tự, các breakpoint không nên được đặt tên theo thiết bị mà là một cái tên đó tổng quát hơn. Đặc biệt là vì một số điện thoại bây giờ lớn hơn máy tính bảng, một số máy tính bảng lớn hơn một số máy tính màn hình nhỏ, v.v.

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

Tại thời điểm này, [bất kỳ quy ước đặt tên nào](http://css-tricks.com/naming-media-queries/) làm cho rõ ràng rằng một thiết kế không được gắn chặt với một loại thiết bị cụ thể sẽ thực hiện thủ thuật, miễn là vì nó mang lại một cảm giác về độ lớn bao phủ.

```scss
$breakpoints: (
  'seed': (min-width: 800px),
  'sprout': (min-width: 1000px),
  'plant': (min-width: 1200px),
);
```

<blockquote class="note"><p>Các ví dụ trước sử dụng map lồng nhau để xác định breakpoint, tuy nhiên điều này thực sự phụ thuộc vào loại trình quản lý breakpoint bạn sử dụng. Bạn có thể chọn các chuỗi thay vì các map bên trong để linh hoạt hơn (e.g. <code>'(min-width: 800px)'</code>).</p></blockquote>

### *Breakpoint Manager*

Khi bạn đã đặt tên cho breakpoint của mình theo cách bạn muốn, bạn cần một cách để sử dụng chúng trong các media query thực tế. Có rất nhiều cách để làm như vậy nhưng tôi phải nói rằng tôi là một fan hâm mộ lớn của breakpoint map được đọc bởi một hàm getter. Hệ thống này vừa đơn giản vừa hiệu quả.

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

<blockquote class="note"><p>Rõ ràng, đây là một trình quản lý breakpoint khá đơn giản. Nếu bạn cần một thứ dễ dàng hơn một chút, tôi có thể khuyên bạn rằng không nên phát minh lại bánh xe và sử dụng những thứ đã được chứng minh là hiệu quả như <a href="https://github.com/sass-mq/sass-mq">Sass-MQ</a>, <a href="http://breakpoint-sass.com/">Breakpoint</a> hay <a href="https://github.com/eduardoboucas/include-media">include-media</a>.</p><p>Nếu bạn muốn đọc thêm về cách tiếp cận các media query trong Sass, hay cả <a href="http://www.sitepoint.com/managing-responsive-breakpoints-sass/">SitePoint</a> (từ chính bạn) và <a href="http://css-tricks.com/approaches-media-queries-sass/">CSS-Tricks</a> đều có những bài viết hay về chủ đề này.</p></blockquote>

### *Media Queries Usage*

Cách đây không lâu, đã có một cuộc tranh luận khá sôi nổi về nơi nên viết các media query: chúng có thuộc về selector (vì Sass cho phép nó) hoặc tách ra khỏi chúng không? Tôi phải nói rằng tôi là một người bảo vệ nhiệt thành cho hệ thống *media-queries-within-selectors*, vì tôi nghĩ rằng nó hoạt động rất tốt tốt với các ý tưởng của *component*.

```scss
.foo {
  color: red;

  @include respond-to('medium') {
    color: blue;
  }
}
```

Dẫn đến đầu ra CSS như sau:

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

Bạn có thể nghe rằng quy ước này dẫn đến các media query trùng lặp trong đầu ra CSS. Điều đó chắc chắn là đúng. Mặc dù, [các thử nghiệm đã được thực hiện](http://sasscast.tumblr.com/post/38673939456/sass-and-media-queries) và từ cuối cùng là nó không thành vấn đề khi Gzip (hoặc bất kỳ thứ tương đương nào) thực hiện công việc của nó:

> … we hashed out whether there were performance implications of combining vs scattering Media Queries and came to the conclusion that the difference, while ugly, is minimal at worst, essentially non-existent at best.
> — [Sam Richards, regarding Breakpoint](http://sasscast.tumblr.com/post/38673939456/sass-and-media-queries)

Bây giờ, nếu bạn thực sự lo lắng về các media query trùng lặp, bạn vẫn có thể sử dụng một công cụ để hợp nhất chúng như [gem này](https://github.com/aaronjensen/sass-media_query_combiner) tuy nhiên tôi cảm thấy như mình phải cảnh báo bạn chống lại các tác dụng phụ có thể có của việc di chuyển code CSS xung quanh. Bạn hẳn là biết rằng thứ tự nguồn là rất quan trọng.

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

Guideline này khá dài và đôi khi thật tốt khi chúng được tóm tắt trong một phiên bản ngắn hơn. Dưới đây là tóm tắt này.

### *Key Principles*

- Một styleguide tất cả về **tính nhất quán**. Nếu bạn không đồng ý với một số nguyên tắc trong Sass Guidelines, hoàn toàn ổn miễn là bạn nhất quán. [↩](https://sass-guidelin.es/#why-a-styleguide)
- Sass nên được giữ đơn giản như bản chất của nó. Tránh xây dựng các hệ thống phức tạp trừ khi thực sự cần thiết. [↩](https://sass-guidelin.es/#key-principles)
- Hãy nhớ rằng đôi khi *KISS* (Giữ cho nó đơn giản, ngu ngốc) sẽ tốt hơn *DRY* (Don’t Repeat Yourself). [↩](https://sass-guidelin.es/#key-principles)

### *Syntax & Formatting*

- Một indentation được tạo thành từ hai (2) khoảng trắng, không dùng tabs. [↩](https://sass-guidelin.es/#syntax--formatting)
- Các dòng nên ngắn hơn 80 ký tự. Hãy chia chúng thành nhiều dòng khi cần thiết. [↩](https://sass-guidelin.es/#syntax--formatting)
- CSS nên được viết đúng, có thể tham khảo và tuân theo  [CSS Guidelines](http://cssguidelin.es/) từ Harry Roberts. [↩](https://sass-guidelin.es/#syntax--formatting)
- Khoảng trắng là miễn phí, sử dụng nó để phân tách các mục, quy tắc và khai báo. Đừng ngần ngại để lại những dòng trống. [↩](https://sass-guidelin.es/#syntax--formatting)

###### STRINGS

- Việc khai báo `@charset` lên đầu stylesheet được khuyến khích cao. [↩](https://sass-guidelin.es/#encoding)
- Trừ khi được dùng làm định danh CSS, các chuỗi phải được trích dẫn bằng dấu nháy đơn. Các URL cũng nên được trích dẫn. [↩](https://sass-guidelin.es/#strings-as-css-values)

###### NUMBERS

- Sass không phân biệt giữa số, số nguyên và số thực nên các số 0 ở cuối nên được bỏ qua. Tuy nhiên các số 0 đứng đầu giúp dễ đọc và nên được thêm vào. [↩](https://sass-guidelin.es/#zeros)
- Độ dài 0 không nên có đơn vị. [↩](https://sass-guidelin.es/#units)
- Thao tác với các đơn vị nên được coi là hoạt động số học, không phải hoạt động chuỗi. [↩](https://sass-guidelin.es/#units)
- Để cải thiện khả năng đọc, các tính toán cấp cao nhất phải được gói trong ngoặc đơn. Ngoài ra, các phép toán phức tạp có thể được chia thành các phần nhỏ hơn. [↩](https://sass-guidelin.es/#calculations)
- Magic numbers làm giảm đáng kể khả năng duy trì code và nên tránh bất cứ khi nào. Khi nghi ngờ, hãy giải thích rõ ở phần mở rộng. [↩](https://sass-guidelin.es/#magic-numbers)

###### COLORS

- Màu sắc nên được thể hiện bằng HSL khi có thể, sau đó là RGB, sau đó là thập lục phân (ở dạng chữ thường và rút gọn). Từ khoá màu nên tránh. [↩](https://sass-guidelin.es/#color-formats)
- Hãy dùng `mix(..)` thay vì `darken(..)` và `lighten(..)` khi làm sáng hoặc làm tối một màu. [↩](https://sass-guidelin.es/#lightening-and-darkening-colors)

###### LISTS

- Các list phải được phân tách bằng dấu phảy, trừ khi được sử dụng làm ánh xạ trực tiếp tới các giá trị CSS được phân tách bằng dấu cách. [↩](https://sass-guidelin.es/#lists)
- Gói bằng dấu ngoặc đơn cũng cần được xem xét để cải thiện khả năng đọc. [↩](https://sass-guidelin.es/#lists)
- List nội tuyến không nên có dấu phảy, list trên nhiều dòng nên có. [↩](https://sass-guidelin.es/#lists)

### *MAPS*

- Maps chứa nhiều hơn một cặp nên được viết trên nhiều dòng. [↩](https://sass-guidelin.es/#maps)
- Để tăng khả năng bảo trì, cặp cuối cùng của map cũng nên có dấu phảy. [↩](https://sass-guidelin.es/#maps)
- Map keys là các chuỗi nên được trích dẫn như bất kỳ chuỗi nào khác. [↩](https://sass-guidelin.es/#maps)

###### DECLARATION SORTING

- Hệ thống được sử dụng để sắp xếp các khai báo(theo bảng chữ cái, theo loại, …) không có vấn đề gì miễn là nó phù hợp. [↩](https://sass-guidelin.es/#declaration-sorting)

###### SELECTOR NESTING

- Tránh lồng selector khi không cần thiết (đại diện cho hầu hết các trường hợp). [↩](https://sass-guidelin.es/#selector-nesting)
- Sử dụng selector lồng nhau cho các lớp giả và các phần tử giả. [↩](https://sass-guidelin.es/#selector-nesting)
- Media queries cũng có thể được lồng trong selector liên quan của chúng. [↩](https://sass-guidelin.es/#selector-nesting)

### *Naming Conventions*

- Tốt nhất là tuân theo các quy ước đặt tên CSS (trừ một vài lỗi) chữ thường và phân cách bằng dấu gạch nối. [↩](https://sass-guidelin.es/#naming-conventions)

### *Commenting*

- CSS là một ngôn ngữ phức tạp, đừng ngần ngại viết ra comment về những thứ trông kinh khủng. [↩](https://sass-guidelin.es/#commenting)
- Đối với các biến, hàm, mixin và placeholder thiết lập API công khai, hãy sử dụng các comment SassDocs. [↩](https://sass-guidelin.es/#documentation)

### *Variables*

- Sử dụng `!default` cho bất kỳ phần biến nào của API công khai có thể được thay đổi một cách an toàn. [↩](https://sass-guidelin.es/#default-flag)
- Không sử dụng `!global` ở cấp độ gốc vì nó có thể tạo ra vi phạm cú pháp Sass trong tương lai. [↩](https://sass-guidelin.es/#global-flag)

### *Extend*

- Bám sát việc mở rộng placeholders, không phải các CSS selector hiện có. [↩](https://sass-guidelin.es/#extend)
- Mở rộng một placeholder càng nhiều lần càng tốt để tránh tác dụng phụ. [↩](https://sass-guidelin.es/#extend)