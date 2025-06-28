
<html lang="vi">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Tuấn Hiệp Materials</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
      tailwind.config = {
        theme: {
          extend: {
            colors: {
              primary: '#1e3a8a',
              secondary: '#e5e7eb'
            }
          }
        }
      }
    </script>
  </head>
  <body class="bg-gray-100 text-gray-800">
    <!-- Header -->
    <header class="bg-white shadow p-4 flex justify-between items-center">
      <div class="flex items-center gap-2">
        <img src="https://via.placeholder.com/40" class="w-10 h-10" alt="Logo">
        <h1 class="text-2xl font-bold text-primary">Tuấn Hiệp Materials</h1>
      </div>
      <div class="flex items-center gap-4">
        <a href="#products" class="hover:underline">Sản phẩm</a>
        <a href="#contact" class="hover:underline">Liên hệ</a>
        <button onclick="toggleCart()" class="relative">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 3h2l.4 2M7 13h10l4-8H5.4" />
          </svg>
          <span id="cartCount" class="absolute -top-2 -right-2 bg-red-500 text-white rounded-full px-1 text-xs">0</span>
        </button>
      </div>
    </header>
  <!PRODUCTS>
    <section id="products" class="py-10 px-4lastfire65519a@gmail.com</strong></p>
        <p>Địa chỉ: Làng Châm, Iagrai, Gia Lai.</p>
      </div>
    </section>

    <!-- Cart Modal -->
    <div id="cartModal" class="fixed inset-0 bg-black bg-opacity-40 hidden items-center justify-center z-50">
      <div class="bg-white rounded p-6 w-full max-w-lg relative">
        <h2 class="text-xl font-bold mb-4">Giỏ hàng</h2>
        <div id="cartItems" class="space-y-2"></div>
        <div class="mt-4 text-right">
          <button onclick="checkout()" class="bg-primary text-white px-4 py-2 rounded">Đặt hàng</button>
          <button onclick="toggleCart()" class="ml-2 px-4 py-2">Đóng</button>
        </div>
      </div>
    </div>

    <!-- Footer -->
    <footer class="bg-gray-200 text-center p-4 mt-10 text-sm">
      &copy; 2025 Tuấn Hiệp Materials. All rights reserved.
    </footer>

    <!-- Scripts -->
    <script>
      const products = [
        { id: 1, name: "Xi măng Hà Tiên", desc: "Bao 50kg", image: "https://via.placeholder.com/300x200", price: 75000 },
        { id: 2, name: "Gạch Tuynel", desc: "100 viên/lô", image: "https://via.placeholder.com/300x200", price: 120000 },
        { id: 3, name: "Cát xây dựng", desc: "1 khối", image: "https://via.placeholder.com/300x200", price: 95000 },
      ];

      const cart = [];

      function renderProducts() {
        const grid = document.getElementById("productGrid");
        grid.innerHTML = products.map(p => `
          <div class="bg-white shadow rounded p-4">
            <img src="${p.image}" class="rounded mb-2" alt="${p.name}">
            <h3 class="text-xl font-semibold">${p.name}</h3>
            <p class="text-gray-600">${p.desc}</p>
            <p class="text-primary font-bold">${p.price.toLocaleString()}đ</p>
            <button onclick="addToCart(${p.id})" class="mt-2 bg-primary text-white px-4 py-2 rounded">Thêm vào giỏ</button>
          </div>
        `).join("");
      }

      function addToCart(id) {
        const product = products.find(p => p.id === id);
        const item = cart.find(i => i.id === id);
        if (item) item.qty++;
        else cart.push({ ...product, qty: 1 });
        updateCartCount();
      }

      function updateCartCount() {
        document.getElementById("cartCount").textContent = cart.reduce((a, b) => a + b.qty, 0);
      }

      function toggleCart() {
        const modal = document.getElementById("cartModal");
        renderCart();
        modal.classList.toggle("hidden");
        modal.classList.toggle("flex");
      }

      function renderCart() {
        const wrapper = document.getElementById("cartItems");
        if (cart.length === 0) {
          wrapper.innerHTML = '<p>Giỏ hàng đang trống.</p>';
          return;
        }
        wrapper.innerHTML = cart.map(item => `
          <div class="flex justify-between border-b pb-2">
            <div>
              <p class="font-semibold">${item.name}</p>
              <p>${item.qty} x ${item.price.toLocaleString()}đ</p>
            </div>
            <div class="text-right font-bold">${(item.qty * item.price).toLocaleString()}đ</div>
          </div>
        `).join("");
      }

      function checkout() {
        alert("Cảm ơn bạn đã đặt hàng! Chúng tôi sẽ liên hệ sớm nhất.");
        cart.length = 0;
        updateCartCount();
        toggleCart();
      }

      renderProducts();
    </script>
  </body>
</html>
