  <style><title>सुपर वेबसाइट | ई-कॉमर्स + बुकिंग + ब्लॉग</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">
    :root { --primary: #2563eb; --dark: #1e293b; --light: #f9fafb; }
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body { font-family: sans-serif; background: var(--light); color: var(--dark); }
    header { background: var(--primary); color: white; padding: 1rem; text-align: center; }
    .container { width: 90%; max-width: 1200px; margin: 2rem auto; }
    .hero { background: #2563eb; color: white; padding: 4rem 2rem; text-align: center; border-radius: 10px; }
    .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px; margin-top: 20px; }
    .card { background: white; padding: 20px; border-radius: 10px; box-shadow: 0 4px 6px rgba(0,0,0,0.1); text-align: center; }
    .btn { background: #2563eb; color: white; padding: 10px 20px; text-decoration: none; border-radius: 5px; display: inline-block; margin-top: 10px; }
  </style>
<body>
  <header>
    <h1>सुपर वेबसाइट <span>★</span></h1>
  </header>
  <div class="container">
    <div class="hero">
      <h2>ई-कॉमर्स, बुकिंग और ब्लॉग — सब एक साथ!</h2>
      <p>भारतीय उपयोगकर्ताओं के लिए खास तौर पर बनाई गई वेबसाइट।</p>
      <a href="#" class="btn" style="background: white; color: #2563eb;">शुरू करें</a>
    </div>
    
    <div class="grid">
      <div class="card">
        <h3>🛍️ ई-कॉमर्स</h3>
        <p>अपने प्रोडक्ट ऑनलाइन बेचें।</p>
        <a href="#" class="btn">शॉपिंग करें</a>
      </div>
      <div class="card">
        <h3>📅 बुकिंग</h3>
        <p>आसानी से अपॉइंटमेंट बुक करें।</p>
        <a href="#" class="btn">बुक करें</a>
      </div>
      <div class="card">
        <h3>✍️ ब्लॉग</h3>
        <p>ताज़ा जानकारी और लेख पढ़ें।</p>
        <a href="#" class="btn">पढ़ें</a>
      </div>
    </div>
  </div>
</body>
</html>
<!DOCTYPE html>
<html>
<head>
<title>Super Platform</title>
<script src="https://checkout.razorpay.com/v1/checkout.js"></script>
</head>
<body>

<h2>Buy Product ₹500</h2>
<button onclick="payNow()">Pay</button>

<script>
async function payNow(){
  const res = await fetch("/api/create-order",{
    method:"POST",
    headers:{"Content-Type":"application/json"},
    body:JSON.stringify({amount:500})
  })
  const order = await res.json()

  const options = {
    key:"YOUR_RAZORPAY_KEY",
    amount:order.amount,
    currency:"INR",
    order_id:order.id,
    handler:function(response){
      alert("Payment Successful")
    }
  }

  const rzp = new Razorpay(options)
  rzp.open()
}
</script>

</body>
</html>

PORT=5000
MONGO_URI=your_mongodb_connection
JWT_SECRET=supersecret
RAZORPAY_KEY_ID=your_key
RAZORPAY_SECRET=your_secret
