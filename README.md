
</head>
<body>

  <header>
    <h1>Tuấn Hiệp Materials</h1>
    <p>Chuyên cung cấp vật liệu xây dựng chất lượng</p>
  </header>

  <div class="container">
    <h2>Sản phẩm nổi bật</h2>
    <div class="products">
      <div class="product">
        <img src="https://images.unsplash.com/photo-1597764691313-bf6e7b5e5b59" alt="Thép xây dựng">
        <h3>Thép xây dựng</h3>
        <p>Giá: 15,000đ/kg</p>
      </div>
      <div class="product">
        <img src="https://images.unsplash.com/photo-1603566171673-cbce1ff95c3a" alt="Xi măng">
        <h3>Xi măng Nghi Sơn</h3>
        <p>Giá: 85,000đ/bao</p>
      </div>
      <div class="product">
        <img src="https://images.unsplash.com/photo-1636819489845-d14978ef216e" alt="Gạch ốp lát">
        <h3>Gạch ốp lát cao cấp</h3>
        <p>Giá: 180,000đ/m²</p>
      </div>
    </div>

    <div class="order-form">
      <h2>Đặt hàng ngay</h2>
      <form action="mailto:lienhe@tuanhiepmaterials.vn" method="post" enctype="text/plain">
        <label for="name">Họ và tên:</label>
        <input type="text" id="name" name="Họ tên" required />

        <label for="phone">Số điện thoại:</label>
        <input type="tel" id="phone" name="Số điện thoại" required />

        <label for="product">Chọn sản phẩm:</label>
        <select id="product" name="Sản phẩm">
          <option value="Thép xây dựng">Thép xây dựng</option>
          <option value="Xi măng Nghi Sơn">Xi măng Nghi Sơn</option>
          <option value="Gạch ốp lát">Gạch ốp lát cao cấp</option>
        </select>

        <label for="quantity">Số lượng:</label>
        <input type="number" id="quantity" name="Số lượng" required />

        <label for="message">Ghi chú thêm:</label>
        <textarea id="message" name="Ghi chú" rows="4"></textarea>

        <button type="submit">Gửi đơn hàng</button>
      </form>
    </div>
  </div>
 <p>📍 Địa chỉ: Làng Châm, iagrai, Gia Lai, Việt Nam </p>
  <footer>
    &copy; 2025 Tuấn Hiệp Materials. Hotline: 083 797 8279
  </footer>

</body>
</html>


