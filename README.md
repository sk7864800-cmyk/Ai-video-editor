<!DOCTYPE html>
<html lang="hi">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <meta name="description" content="सुपर वेबसाइट: ई-कॉमर्स, अपॉइंटमेंट बुकिंग और ब्लॉग — एक ही प्लेटफॉर्म पर। भारतीय उपयोगकर्ताओं के लिए अनुकूलित, Razorpay समर्थित।">
  <title>सुपर वेबसाइट | ई-कॉमर्स + बुकिंग + ब्लॉग</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">
  <style>
    :root {
      --primary: #2563eb;
      --primary-dark: #1d4ed8;
      --accent: #ec4899;
      --light: #f9fafb;
      --dark: #1e293b;
      --gray: #64748b;
      --border: #e2e8f0;
      --success: #10b981;
      --warning: #f59e0b;
      --radius: 10px;
      --shadow: 0 4px 6px -1px rgba(0,0,0,0.1), 0 2px 4px -1px rgba(0,0,0,0.06);
    }
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body {
      font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
      line-height: 1.6;
      color: var(--dark);
      background-color: #f1f5f9;
    }
    .container {
      width: 90%;
      max-width: 1200px;
      margin: 0 auto;
    }
    /* Header */
    header {
      background: linear-gradient(135deg, var(--primary), #1d4ed8);
      color: white;
      padding: 1.2rem 0;
      position: sticky;
      top: 0;
      z-index: 100;
      box-shadow: var(--shadow);
    }
    .header-content {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    .logo h1 {
      font-size: 1.8rem;
      font-weight: 800;
      letter-spacing: -0.5px;
    }
    .logo span {
      color: #ffd166;
    }
    nav ul {
      display: flex;
      list-style: none;
      gap: 1.8rem;
    }
    nav a {
      color: white;
      text-decoration: none;
      font-weight: 500;
      padding: 0.5rem 0.8rem;
      border-radius: 6px;
      transition: all 0.2s;
    }
    nav a:hover, nav a.active {
      background: rgba(255,255,255,0.2);
    }
    .cart-icon {
      position: relative;
      font-size: 1.4rem;
      cursor: pointer;
    }
    .cart-count {
      position: absolute;
      top: -8px;
      right: -8px;
      background: var(--accent);
      color: white;
      font-size: 0.7rem;
      width: 18px;
      height: 18px;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      font-weight: bold;
    }
    /* Hero */
    .hero {
      background: linear-gradient(rgba(37, 99, 235, 0.9), rgba(29, 78, 216, 0.95)), url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 100 100"><rect width="100" height="100" fill="%232563eb"/><circle cx="20" cy="20" r="2" fill="%23ec4899"/><circle cx="80" cy="70" r="1.5" fill="%23ec4899"/></svg>');
      background-size: cover;
      color: white;
      padding: 6rem 0;
      text-align: center;
    }
    .hero h2 {
      font-size: 2.8rem;
      margin-bottom: 1.2rem;
      font-weight: 800;
    }
    .hero p {
      font-size: 1.3rem;
      max-width: 760px;
      margin: 0 auto 2rem;
      opacity: 0.95;
    }
    .btn {
      display: inline-block;
      background: white;
      color: var(--primary);
      padding: 0.9rem 2.2rem;
      font-weight: 700;
      text-decoration: none;
      border-radius: 8px;
      transition: all 0.3s;
      border: 2px solid white;
      font-size: 1.1rem;
      margin: 0.5rem;
    }
    .btn:hover {
      background: transparent;
      color: white;
      transform: translateY(-3px);
      box-shadow: 0 6px 15px rgba(0,0,0,0.2);
    }
    .btn-outline {
      background: transparent;
      color: white;
      border: 2px solid white;
    }
    .btn-outline:hover {
      background: white;
      color: var(--primary);
    }
    /* Section */
    section {
      padding: 5rem 0;
    }
    .section-title {
      text-align: center;
      margin-bottom: 3rem;
    }
    .section-title h2 {
      font-size: 2.2rem;
      color: var(--primary);
      position: relative;
      display: inline-block;
      margin-bottom: 0.8rem;
    }
    .section-title h2::after {
      content: '';
      display: block;
      width: 70px;
      height: 4px;
      background: var(--accent);
      margin: 0.5rem auto;
      border-radius: 2px;
    }
    .section-title p {
      color: #666;
      max-width: 700px;
      margin: 0 auto;
      font-size: 1.15rem;
    }
    /* Grids */
    .grid-2, .grid-3 {
      display: grid;
      gap: 2rem;
    }
    .grid-2 { grid-template-columns: repeat(auto-fit, minmax(300px, 1fr}};
    .grid-3 { grid-template-columns: repeat(auto-fit, minmax(300px, 1fr}};
    /* Product Card */
    .product-card {
      background: white;
      border-radius: var(--radius);
      overflow: hidden;
      box-shadow: var(--shadow);
      transition: all 0.3s;
      border: 1px solid var(--border);
    }
    .product-card:hover {
      transform: translateY(-5px);
      box-shadow: 0 10px 25px rgba(0,0,0,0.1);
    }
    .product-img {
      height: 200px;
      background: linear-gradient(45deg, #3b82f6, #8b5cf6);
      display: flex;
      align-items: center;
      justify-content: center;
      color: white;
      font-size: 3rem;
    }
    .product-info {
      padding: 1.5rem;
    }
    .product-info h3 {
      font-size: 1.3rem;
      margin-bottom: 0.5rem;
      color: var(--dark);
    }
    .product-price {
      font-size: 1.4rem;
      font-weight: 700;
      color: var(--primary);
      margin: 0.5rem 0;
    }
    .product-actions {
      display: flex;
      gap: 0.8rem;
      margin-top: 1rem;
    }
    .btn-sm {
      padding: 0.5rem 1.2rem;
      font-size: 0.95rem;
      border-radius: 6px;
    }
    /* Calendar Booking */
    .calendar-container {
      background: white;
      border-radius: var(--radius);
      padding: 1.8rem;
      box-shadow: var(--shadow);
      border: 1px solid var(--border);
    }
    .calendar-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 1.5rem;
    }
    .calendar-month {
      font-size: 1.4rem;
      font-weight: 700;
      color: var(--primary);
    }
    .calendar-grid {
      display: grid;
      grid-template-columns: repeat(7, 1fr);
      gap: 0.5rem;
      margin-bottom: 1.5rem;
    }
    .calendar-day-header {
      text-align: center;
      font-weight: 600;
      color: var(--gray);
      padding: 0.5rem;
      font-size: 0.9rem;
    }
    .calendar-day {
      height: 50px;
      display: flex;
      align-items: center;
      justify-content: center;
      border-radius: 6px;
      cursor: pointer;
      font-weight: 500;
      transition: all 0.2s;
    }
    .calendar-day.available {
      background: #dbeafe;
      color: #3b82f6;
    }
    .calendar-day.available:hover {
      background: #93c5fd;
    }
    .calendar-day.unavailable {
      background: #fee2e2;
      color: #ef4444;
      cursor: not-allowed;
    }
    .calendar-day.selected {
      background: var(--primary);
      color: white;
      font-weight: 700;
    }
    .booking-form {
      background: #f1f5f9;
      padding: 1.5rem;
      border-radius: var(--radius);
      margin-top: 1.5rem;
    }
    .form-group {
      margin-bottom: 1rem;
    }
    .form-group label {
      display: block;
      margin-bottom: 0.4rem;
      font-weight: 600;
      color: var(--dark);
    }
    .form-control {
      width: 100%;
      padding: 0.75rem;
      border: 1px solid var(--border);
      border-radius: 6px;
      font-size: 1rem;
      transition: border 0.2s;
    }
    .form-control:focus {
      outline: none;
      border-color: var(--primary);
      box-shadow: 0 0 0 3px rgba(37, 99, 235, 0.1);
    }
    /* Blog */
    .blog-card {
      background: white;
      border-radius: var(--radius);
      overflow: hidden;
      box-shadow: var(--shadow);
      border: 1px solid var(--border);
    }
    .blog-img {
      height: 180px;
      background: linear-gradient(45deg, #10b981, #059669);
      display: flex;
      align-items: center;
      justify-content: center;
      color: white;
      font-size: 2.5rem;
    }
    .blog-content {
      padding: 1.5rem;
    }
    .blog-meta {
      display: flex;
      gap: 1rem;
      font-size: 0.85rem;
      color: var(--gray);
      margin-bottom: 0.8rem;
    }
    .blog-meta i {
      color: var(--primary);
    }
    /* Footer */
    footer {
      background: var(--dark);
      color: #94a3b8;
      padding: 3rem 0 1.8rem;
    }
    .footer-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 2rem;
      margin-bottom: 2.5rem;
    }
    .footer-col h3 {
      color: white;
      margin-bottom: 1.2rem;
      font-size: 1.3rem;
      display: flex;
      align-items: center;
      gap: 0.5rem;
    }
    .footer-col ul {
      list-style: none;
    }
    .footer-col ul li {
      margin-bottom: 0.6rem;
    }
    .footer-col ul li a {
      color: #94a3b8;
      text-decoration: none;
      transition: color 0.2s;
    }
    .footer-col ul li a:hover {
      color: white;
    }
    .copyright {
      text-align: center;
      padding-top: 1.8rem;
      border-top: 1px solid #334155;
      font-size: 0.9rem;
    }
    /* Responsive */
    @media (max-width: 768px) {
      .header-content {
        flex-direction: column;
        gap: 1.2rem;
      }
      nav ul {
        flex-wrap: wrap;
        justify-content: center;
      }
      .hero h2 {
        font-size: 2
indax.html






# Ai-video-editor
VidMuse AI is a browser-based AI video editing platform that lets users upload and enhance videos with auto subtitles, silence removal, smart reframing, background removal, and AI thumbnails. With a mobile-friendly design and secure cloud system, it delivers fast, high-quality editing without powerful hardware.
