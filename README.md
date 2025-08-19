# narga-epub-core

An EPUB Boilerplate for generate ebook.

## Styles for ePub 3

  - `styles.css` has optimized CSS codes for ePub 3 reader which includes ePub reader, reader devices like Kindle, Kobo ...

## Favourited Fonts

Here is the list of my favourite fonts that I used in my created epub for long reading:

  - [Bookerly](https://en.wikipedia.org/wiki/Bookerly) – Default Kindle font;
  - [Literata](https://github.com/googlefonts/literata) – Google font (free);
  - [Crimson Pro](https://fontsarena.com/crimson-pro-by-sebastian-kosch-jacques-le-bailly/) – Sebastian Kosch & Jacques Le Bailly (free);
  - [Newsreader](https://github.com/productiontype/Newsreader) – an original typeface designed by Production Type (free);
  - [Cochineal](https://ctan.org/pkg/cochineal) – a fork from the Crimson fonts (free);
  - [Source Serif](https://github.com/adobe-fonts/source-serif) – a free font from Adobe;
  - [Libertinus](https://github.com/alerque/libertinus) – a fork of Linux Libertine (free);
  - [Georgia](https://docs.microsoft.com/typography/font-list/georgia) – classic font from Microsoft;

-----

## Cách sử dụng các lớp CSS đặc biệt

Dưới đây là hướng dẫn cách áp dụng các lớp (class) đặc biệt có trong file `styles.css` vào file HTML của bạn để tạo ra các định dạng trình bày đẹp mắt.

### 1\. Trang có nội dung căn giữa tuyệt đối

Để tạo một trang riêng biệt (ví dụ: trang bìa phụ, trang trích dẫn) với nội dung được căn vào chính giữa cả chiều ngang và dọc.

**HTML:**

```html
<div class="full-page-center" epub:type="full-page">
  <div>
    <h1>Tên Sách</h1>
    <p class="no-indent"><em>Tác giả</em></p>
  </div>
</div>
```

### 2\. Hình ảnh và chú thích

Sử dụng thẻ `<figure>` để nhóm hình ảnh (`<img>`) và chú thích (`<figcaption>`). CSS sẽ tự động căn giữa hình ảnh và định dạng chú thích.

**HTML:**

```html
<figure>
  <img src="../Images/ten-hinh-anh.jpg" alt="Mô tả hình ảnh" />
  <figcaption>Đây là chú thích cho hình ảnh bên trên.</figcaption>
</figure>
```

### 3\. Chữ cái lớn đầu đoạn (Dropcap)

Để làm cho chữ cái đầu tiên của đoạn văn lớn và nổi bật, hãy bọc nó trong một thẻ `<span>` với class `.dropcap`.

**HTML:**

```html
<p><span class="dropcap">N</span>gày xửa ngày xưa, ở một vương quốc xa xôi, có một nàng công chúa xinh đẹp...</p>
```

### 4\. Dấu ngăn cách trang trí

Thay vì dùng đường kẻ ngang (`<hr>`) mặc định, bạn có thể sử dụng các dấu ngăn cách trang trí để ngắt các phần hoặc cảnh trong truyện.

**HTML cho dấu chấm vuông:**

```html
<hr class="dots" />
```

**HTML cho dấu hoa thị:**

```html
<hr class="ornament" />
```

### 5\. Trích dẫn (Blockquote) có viền

Để tạo một khối trích dẫn có đường kẻ dọc bên trái để làm nổi bật, hãy thêm class `.border` vào thẻ `<blockquote>`.

**HTML:**

```html
<blockquote class="border">
  <p>Một câu trích dẫn hay và ý nghĩa được đặt ở đây để làm nổi bật trong văn bản.</p>
  <p class="no-indent">— Tên tác giả</p>
</blockquote>
```

### 6\. Các lớp tiện ích phổ biến

  - **`.no-indent`**: Xóa thụt lề đầu dòng của một đoạn văn.
  - **`.text-center`**: Căn giữa toàn bộ nội dung của một khối (ví dụ: một `<div>` hoặc `<p>`).
  - **`.smallcaps`**: Chuyển văn bản thành dạng chữ hoa nhỏ (small-caps).

**HTML:**

```html
<p class="no-indent">Đoạn văn này không có thụt lề đầu dòng.</p>

<div class="text-center">
  <p>Đoạn văn này sẽ được căn giữa.</p>
</div>

<p><span class="smallcaps">Văn bản này là chữ hoa nhỏ.</span></p>
```