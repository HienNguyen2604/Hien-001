<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GIA ĐÌNH TRUNG NAM</title>
     <link rel="icon" href="https://hiennguyen2604.github.io/Hien-001/logo.jpg" type="image/x-icon">
    <style>
        /* CSS cơ bản để căn giữa nội dung và thiết lập màu sắc */
        body {
            font-family: Arial, sans-serif;/* Chọn font Arial làm font chính, nếu không có, nó sẽ chọn một font không chân (sans-serif). */
            margin: 0;/*  Xóa tất cả khoảng cách bên ngoài của phần tử <body>. */
            padding: 0;/*   Xóa tất cả khoảng cách bên trong của phần tử <body>. */
        }
        header {
            background-color: #4CAF50; /* Màu nền xanh cho header */
            color: white;/* Màu chữ cho header */
            text-align: center;/* Căn giữa nội dung trong header */
            padding: 20px;/* Thêm khoảng cách 20px bên trong header từ các cạnh. */
        }
        section {
            background-color: #f4f4f4; /* Màu nền sáng cho nội dung chính */
            text-align: center;/* Căn giữa nội dung trong section */
            padding: 20px;
        }
        footer {
            background-color: #333;
            color: white;
            text-align: center;/* Căn giữa nội dung trong footer */
            padding: 10px;
            position: fixed;/* Đặt vị trí của footer là cố định, tức là nó sẽ ở cùng một vị trí khi cuộn trang. */
            width: 100%;/* Thiết lập chiều rộng của footer là 100% chiều rộng của viewport.*/
            bottom: 0;/* Đặt footer ở dưới cùng của viewport.*/
        }
       
         img {
            width: 300px; /* Đặt kích thước cho hình ảnh */
            height: auto; /* Giữ tỉ lệ hình ảnh */
            border-radius: 10px; /* Bo tròn góc của hình ảnh */
            margin: auto; /* Khoảng cách giữa các hình ảnh */
            cursor: pointer;/* Đặt con trỏ chuột thành hình bàn tay khi di chuột qua img. */
            transition: all 0.3s ease; /* Thêm hiệu ứng chuyển tiếp cho tất cả các thuộc tính */
            box-sizing: border-box; /* Giúp ảnh không bị thay đổi kích thước khi thêm viền */
        }

         /* Thiết lập cho modal */
        .modal {
            display: none;
            position: fixed;
            z-index: 1;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            overflow: auto;
            background-color: rgba(0, 0, 0, 0.8);
        }

        /* Hình ảnh trong modal */
        .modal-content {
            margin: auto;
            display: block;
            width: 80%;
            max-width: 700px;
        }

        /* Hiệu ứng phóng to */
        .modal-content {
            animation-name: zoom;
            animation-duration: 0.6s;
        }

        @keyframes zoom {
            from {transform: scale(0)} 
            to {transform: scale(1)}
        }

        /* Nút đóng modal */
        .close {
            position: absolute;
            top: 15px;
            right: 35px;
            color: #fff;
            font-size: 40px;
            font-weight: bold;
            transition: 0.3s;
        }

        .close:hover,
        .close:focus {
            color: #bbb;
            text-decoration: none;
            cursor: pointer;
        }

        figure {
		    display: inline-block; /* Để các hình ảnh và chú thích hiện trên cùng một hàng nếu có đủ không gian */
		    margin: 10px;
		    text-align: center; /* Căn giữa tên ảnh dưới ảnh */
		}

		figcaption {
		    margin-top: 10px; /* Khoảng cách giữa ảnh và tên ảnh */
		    font-size: 14px;
		    color: #333; /* Màu chữ cho chú thích */
		}

		/* CSS cho mũi tên */
		.prev, .next {
		    cursor: pointer;
		    position: absolute;
		    top: 50%;
		    width: auto;
		    padding: 16px;
		    margin-top: -22px;
		    color: white;
		    font-weight: bold;
		    font-size: 30px;
		    transition: 0.6s ease;
		    user-select: none;
		    background-color: rgba(0, 0, 0, 0.5); /* Nền mờ cho mũi tên */
		}

		.next {
		    right: 0;
		    border-radius: 3px 0 0 3px;
		}

		.prev {
		    left: 0;
		    border-radius: 0 3px 3px 0;
		}

		.prev:hover, .next:hover {
		    background-color: rgba(0, 0, 0, 0.8); /* Hiệu ứng khi hover */
		}

        /* Nút Xem Thêm */
        button {
            background-color: #4CAF50; /* Nút màu xanh */
            color: white;
            padding: 10px 20px;
            border: none;/* Không có viền cho nút. */
            cursor: pointer;/* Đặt con trỏ chuột thành hình bàn tay khi di chuột qua nút. */
            font-size: 16px;/* Thiết lập kích thước chữ cho nút là 16px */
        }
        button:hover /* Thiết lập hiệu ứng khi chuột di chuyển qua nút. */{
            background-color: #45a049;/* Thay đổi màu nền của nút khi di chuột qua thành một màu xanh đậm hơn. */
        }

        img:hover {
		    border: 4px solid red; /* Hiện viền đỏ khi di chuột qua ảnh */
		}
    </style>
</head>
<body>

    <!-- Header -->
    <header>
        <h1>GIA ĐÌNH TRUNG NAM</h1>
    </header>

    <!-- Nội dung chính -->
    <section>
		<hr/>
		
        <!-- Hình ảnh sản phẩm -->
        <figure> 
        <img id="img1" src="https://hiennguyen2604.github.io/Hien-001/ba mẹ.jpg" alt="Ba mẹ Trung Nam">
        <figcaption>Ba mẹ Trung Nam</figcaption>
        </figure>

        <figure>
        <img id="img2" src="https://hiennguyen2604.github.io/Hien-001/trung nam.jpg" alt="Trung Nam">
        <figcaption>Trung Nam</figcaption>
        </figure>

        <figure>
        <img id="img3" src="https://hiennguyen2604.github.io/Hien-001/nam.jpg" alt="Nam">
        <figcaption>Nam</figcaption>
        </figure>

        <figure>
        <img id="img4" src="https://hiennguyen2604.github.io/Hien-001/ba & nam.jpg" alt="Nam được ba bồng">
        <figcaption>Nam được ba bồng</figcaption>
        </figure>

        <figure> 
        <img id="img5" src="https://hiennguyen2604.github.io/Hien-001/ăn vụng.jpg" alt="ăn vụng">
        <figcaption>ăn vụng</figcaption>
        </figure>
		
		<figure> 
        <img id="img6" src="https://hiennguyen2604.github.io/Hien-001/anh 2 buồn.jpg" alt="anh 2 buồn">
        <figcaption>anh 2 buồn</figcaption>
        </figure>

        <figure> 
        <img id="img7" src="https://hiennguyen2604.github.io/Hien-001/anh em trên sofa.jpg" alt="anh em trên sofa">
        <figcaption>anh em trên sofa</figcaption>
        </figure>

        <figure> 
        <img id="img8" src="https://hiennguyen2604.github.io/Hien-001/ba bo tự sướng.jpg" alt="ba bo tự sướng">
        <figcaption>ba bo tự sướng</figcaption>
        </figure>

        <figure> 
        <img id="img9" src="https://hiennguyen2604.github.io/Hien-001/ba tự sướng 1.jpg" alt="ba tự sướng 1">
        <figcaption>ba tự sướng 1</figcaption>
        </figure>

        <figure> 
        <img id="img10" src="https://hiennguyen2604.github.io/Hien-001/ba tự sướng 2.jpg" alt="ba tự sướng 2">
        <figcaption>ba tự sướng 2</figcaption>
        </figure>

        <figure> 
        <img id="img11" src="https://hiennguyen2604.github.io/Hien-001/ba và bi.jpg" alt="ba và bi">
        <figcaption>ba và bi</figcaption>
        </figure>

        <figure> 
        <img id="img12" src="https://hiennguyen2604.github.io/Hien-001/bo bi đẹp trai.jpg" alt="bo bi đẹp trai">
        <figcaption>bo bi đẹp trai</figcaption>
        </figure>

        <figure> 
        <img id="img13" src="https://hiennguyen2604.github.io/Hien-001/bo vui đùa.jpg" alt="bo vui đùa">
        <figcaption>bo vui đùa</figcaption>
        </figure>

        <figure> 
        <img id="img14" src="https://hiennguyen2604.github.io/Hien-001/người và hoa.jpg" alt="người và hoa">
        <figcaption>người và hoa</figcaption>
        </figure>

        <figure> 
        <img id="img15" src="https://hiennguyen2604.github.io/Hien-001/sinh nhật anh hai bi.jpg" alt="sinh nhật anh hai bi">
        <figcaption>sinh nhật anh hai bi</figcaption>
        </figure>

        <figure> 
        <img id="img16" src="https://hiennguyen2604.github.io/Hien-001/sinh nhật ba.jpg" alt="sinh nhật ba">
        <figcaption>sinh nhật ba</figcaption>
        </figure>

        <figure> 
        <img id="img17" src="https://hiennguyen2604.github.io/Hien-001/sinh nhật ông ngoại 001.jpg" alt="sinh nhật ông ngoại 001">
        <figcaption>sinh nhật ông ngoại 001</figcaption>
        </figure>

        <figure> 
        <img id="img18" src="https://hiennguyen2604.github.io/Hien-001/sinh nhật ông ngoại 002.jpg" alt="sinh nhật ông ngoại 002">
        <figcaption>sinh nhật ông ngoại 002</figcaption>
        </figure>

        <figure> 
        <img id="img19" src="https://hiennguyen2604.github.io/Hien-001/sinh nhật ông ngoại 003.jpg" alt="sinh nhật ông ngoại 003">
        <figcaption>sinh nhật ông ngoại 003</figcaption>
        </figure>

        <figure> 
        <img id="img20" src="https://hiennguyen2604.github.io/Hien-001/sinh nhật ông ngoại 003.jpg" alt="sơ mi trắng">
        <figcaption>sơ mi trắng</figcaption>
        </figure>

        <figure> 
        <img id="img21" src="https://hiennguyen2604.github.io/Hien-001/trồng cây.jpg" alt="trồng cây">
        <figcaption>trồng cây</figcaption>
        </figure>
        <hr/>

        <!-- Modal -->
        <div id="myModal" class="modal">
		    <span class="close">&times;</span>
		    <img class="modal-content" id="modalImg">
		    <a class="prev">&#10094;</a> <!-- Mũi tên qua trái -->
		    <a class="next">&#10095;</a> <!-- Mũi tên qua phải -->
		</div>


        <!-- Nút -->
        <button>Xem Thêm</button>
    </section>

    <!-- Footer -->
    <footer>
        <p>Email: trungnamgreen@gmail.com | Phone : 0979077486</p>
    </footer>

     <script>
        // Lấy các phần tử cần thiết
        var modal = document.getElementById("myModal");
        var modalImg = document.getElementById("modalImg");
        var closeBtn = document.getElementsByClassName("close")[0];
        var images = document.querySelectorAll("section img");
        var currentIndex;

        // Lấy tất cả các ảnh và gán sự kiện click cho từng ảnh
        var images = document.querySelectorAll("img, index");
        images.forEach(function(img, index) {
            img.onclick = function() {
                modal.style.display = "block";
                modalImg.src = this.src;  // Gán đường dẫn của ảnh được click vào modal
                currentIndex = index;
            }
        });

        // Khi click vào nút "x", đóng modal
        closeBtn.onclick = function() {
            modal.style.display = "none";
        }

        // Đóng modal khi click bên ngoài modal
        window.onclick = function(event) {
            if (event.target == modal) {
                modal.style.display = "none";
            }
        }
       // Hàm chuyển đến ảnh tiếp theo
		function showNextImage() {
		    currentIndex = (currentIndex + 1) % images.length; // Chuyển sang ảnh kế tiếp
		    modalImg.src = images[currentIndex].src; // Cập nhật ảnh trong modal
		}

		// Hàm chuyển đến ảnh trước
		function showPrevImage() {
		    currentIndex = (currentIndex - 1 + images.length) % images.length; // Quay về ảnh trước
		    modalImg.src = images[currentIndex].src; // Cập nhật ảnh trong modal
		}

		// Gán sự kiện click cho các mũi tên
		document.querySelector('.next').onclick = showNextImage;
		document.querySelector('.prev').onclick = showPrevImage; 
    </script>

</body>
</html>
