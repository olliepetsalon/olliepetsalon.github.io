# olliepetsalon.github.io
<!DOCTYPE html>
<html lang="zh-TW">
<head>
  <meta charset="UTF-8">
  <title>歐里寵物沙龍｜犬貓美容服務定型化契約</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI",
                   "PingFang TC", "Noto Sans TC", Arial, sans-serif;
      background: #f6f6f6;
      line-height: 1.8;
      margin: 0;
      padding: 0;
    }
    .container {
      max-width: 900px;
      margin: 30px auto;
      background: #fff;
      padding: 30px;
      border-radius: 8px;
      box-shadow: 0 2px 10px rgba(0,0,0,0.08);
    }
    h1, h2 {
      text-align: center;
    }
    h2 {
      margin-top: 40px;
      border-bottom: 1px solid #ddd;
      padding-bottom: 5px;
    }
    p {
      margin: 10px 0;
    }
    .info {
      background: #f2f2f2;
      padding: 15px;
      border-radius: 6px;
      margin-bottom: 20px;
    }
    .notice {
      color: #b00020;
      font-weight: bold;
    }
    .agree-box {
      margin-top: 40px;
      padding: 20px;
      border: 2px solid #ddd;
      border-radius: 8px;
      background: #fafafa;
    }
    .agree-box label {
      font-weight: bold;
    }
    .submit-btn {
      margin-top: 20px;
      width: 100%;
      padding: 14px;
      font-size: 16px;
      background: #333;
      color: #fff;
      border: none;
      border-radius: 6px;
      cursor: not-allowed;
      opacity: 0.5;
    }
    .submit-btn.enabled {
      cursor: pointer;
      opacity: 1;
    }
    .footer {
      margin-top: 40px;
      font-size: 14px;
      color: #666;
      text-align: center;
    }
  </style>
</head>

<body>
  <div class="container">

    <h1>犬、貓美容服務定型化契約</h1>

    <div class="info">
      <p><strong>店家名稱：</strong>歐里寵物沙龍</p>
      <p><strong>聯絡方式：</strong>LINE：@olliepetsalon</p>
      <p><strong>營業地址：</strong>桃園市桃園區正光一街88號</p>
    </div>

    <p>
      本契約係由歐里寵物沙龍（以下簡稱「甲方」）與寵物飼主
      （以下簡稱「乙方」）就犬、貓美容服務相關事項，
      本於誠信原則訂立。
    </p>

    <!-- 中間條款（略，與你原本相同） -->

    <div class="agree-box">
      <p>
        <input type="checkbox" id="agree">
        <label for="agree">我已詳細閱讀並同意以上所有契約條款</label>
      </p>

      <p>
        <strong>請上傳您的簽名（照片或截圖）：</strong><br>
        <input type="file" id="signature" accept="image/*">
      </p>

      <button id="submitBtn" class="submit-btn">
        送出並同意契約
      </button>
    </div>

    <div class="footer">
      <p>※ 勾選同意並送出，即表示乙方已理解並同意本契約內容。</p>
    </div>

  </div>

  <script>
    const agree = document.getElementById("agree");
    const signature = document.getElementById("signature");
    const submitBtn = document.getElementById("submitBtn");

    function checkStatus() {
      if (agree.checked && signature.files.length > 0) {
        submitBtn.classList.add("enabled");
        submitBtn.disabled = false;
      } else {
        submitBtn.classList.remove("enabled");
        submitBtn.disabled = true;
      }
    }

    agree.addEventListener("change", checkStatus);
    signature.addEventListener("change", checkStatus);

    submitBtn.addEventListener("click", function () {
      alert("已完成契約同意，請將此頁面截圖或將簽名圖片提供給店家留存。");
    });
  </script>

</body>
</html>
