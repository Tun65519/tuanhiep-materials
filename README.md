
</head>
<body>
  <header>
    <h1>Tuấn Hiệp Materials</h1>
    <p>Chuyên cung cấp vật liệu xây dựng chất lượng</p>
  </header>

  <nav>
    <a href="#">Trang chủ</a>
    <a href="#products">Sản phẩm</a>
    <a href="#order">Đặt hàng</a>
    <a href="#contact">Liên hệ</a>
  </nav>

  <div class="container" id="products">
    <h2>Sản phẩm tiêu biểu</h2>
    <div class="product">
      <h3>Gạch không nung</h3>
      <p>Gạch bền chắc, thân thiện với môi trường.</p>
      <p>Giá: 1.200đ/viên</p>
    </div>
    <div class="product">
      <h3>Xi măng Hà Tiên</h3>
      <p>Chất lượng cao, phù hợp mọi công trình xây dựng.</p>
      <p>Giá: 90.000đ/bao</p>
    </div>
  </div>

  <div class="container" id="order">
    <h2>Đặt hàng</h2>
    <form action="https://formspree.io/f/your-email-id" method="POST">
      <label for="name">Tên khách hàng</label>
      <input type="text" id="name" name="name" required>

      <label for="phone">Số điện thoại</label>
      <input type="text" id="phone" name="phone" required>

      <label for="product">Sản phẩm muốn đặt</label>
      <input type="text" id="product" name="product" required>

      <label for="quantity">Số lượng</label>
      <input type="number" id="quantity" name="quantity" min="1" required>

      <label for="message">Ghi chú thêm</label>
      <textarea id="message" name="message"></textarea>

      <button type="submit">Gửi đơn hàng</button>
    </form>
  </div>

  <footer id="contact">
    <p>Địa chỉ: 123 Đường Xây Dựng, Q.9, TP.HCM</p>
    <p>Hotline: 0909 123 456 | Email: lienhe@tuanhiepmaterials.vn</p>
  </footer>
</body>
</html>
