# purpose-consulting<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Purpose of Life - Discover Your Meaning</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            color: #333;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        .header {
            text-align: center;
            color: white;
            margin-bottom: 40px;
            padding: 40px 0;
        }

        .header h1 {
            font-size: 3rem;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }

        .header p {
            font-size: 1.3rem;
            opacity: 0.9;
            max-width: 600px;
            margin: 0 auto;
        }

        .main-content {
            background: white;
            border-radius: 20px;
            padding: 40px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.1);
            margin-bottom: 30px;
        }

        .service-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
            margin-bottom: 40px;
        }

        .service-card {
            background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
            color: white;
            padding: 30px;
            border-radius: 15px;
            text-align: center;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            cursor: pointer;
        }

        .service-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 40px rgba(0,0,0,0.3);
        }

        .service-card h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
        }

        .service-card .price {
            font-size: 2rem;
            font-weight: bold;
            margin: 20px 0;
        }

        .service-card .duration {
            opacity: 0.9;
            margin-bottom: 20px;
        }

        .btn {
            background: rgba(255,255,255,0.2);
            border: 2px solid white;
            color: white;
            padding: 12px 30px;
            border-radius: 50px;
            cursor: pointer;
            font-size: 1rem;
            font-weight: bold;
            transition: all 0.3s ease;
            border: none;
        }

        .btn:hover {
            background: white;
            color: #f5576c;
        }

        .about-section {
            background: linear-gradient(135deg, #a8edea 0%, #fed6e3 100%);
            padding: 40px;
            border-radius: 15px;
            margin-bottom: 30px;
            text-align: center;
        }

        .about-section h2 {
            font-size: 2rem;
            color: #333;
            margin-bottom: 20px;
        }

        .about-section p {
            font-size: 1.1rem;
            line-height: 1.6;
            color: #555;
            max-width: 800px;
            margin: 0 auto;
        }

        .testimonials {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 40px;
        }

        .testimonial {
            background: white;
            padding: 25px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            border-left: 4px solid #667eea;
        }

        .testimonial p {
            font-style: italic;
            margin-bottom: 15px;
            color: #666;
        }

        .testimonial .author {
            font-weight: bold;
            color: #333;
        }

        .footer {
            text-align: center;
            color: white;
            padding: 30px 0;
            opacity: 0.8;
        }

        .modal {
            display: none;
            position: fixed;
            z-index: 1000;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0,0,0,0.7);
            overflow-y: auto;
        }

        .modal-content {
            background-color: white;
            margin: 5% auto;
            padding: 40px;
            border-radius: 20px;
            width: 90%;
            max-width: 500px;
            position: relative;
            text-align: center;
        }

        .close {
            color: #aaa;
            float: right;
            font-size: 28px;
            font-weight: bold;
            position: absolute;
            top: 15px;
            right: 25px;
            cursor: pointer;
        }

        .close:hover {
            color: black;
        }

        .form-group {
            margin-bottom: 20px;
            text-align: left;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: bold;
            color: #333;
        }

        .form-group input, .form-group textarea, .form-group select {
            width: 100%;
            padding: 12px;
            border: 2px solid #ddd;
            border-radius: 8px;
            font-size: 1rem;
        }

        .form-group input:focus, .form-group textarea:focus, .form-group select:focus {
            outline: none;
            border-color: #667eea;
        }

        .pay-btn {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            border: none;
            padding: 15px 40px;
            border-radius: 50px;
            font-size: 1.1rem;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            width: 100%;
            margin-top: 20px;
        }

        .pay-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.3);
        }

        .success-message {
            background: linear-gradient(135deg, #56ab2f 0%, #a8e063 100%);
            color: white;
            padding: 30px;
            border-radius: 15px;
            margin-top: 20px;
            display: none;
        }

        .earnings-display {
            background: linear-gradient(135deg, #ffd89b 0%, #19547b 100%);
            color: white;
            padding: 30px;
            border-radius: 15px;
            text-align: center;
            margin-bottom: 30px;
        }

        .earnings-display h2 {
            font-size: 2.5rem;
            margin-bottom: 10px;
        }

        .earnings-display p {
            opacity: 0.9;
        }

        @media (max-width: 768px) {
            .header h1 {
                font-size: 2rem;
            }
            .header p {
                font-size: 1rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>🌟 Discover Your Life's Purpose 🌟</h1>
            <p>Personal consultations to help you understand why you're here on Earth</p>
        </div>

        <div class="earnings-display">
            <h2>$<span id="totalEarnings">0</span></h2>
            <p>Total Earnings</p>
        </div>

        <div class="main-content">
            <h2 style="text-align: center; margin-bottom: 30px; color: #667eea;">Choose Your Consultation</h2>
           
            <div class="service-grid">
                <div class="service-card" onclick="openBooking('Quick Insight', 25, 15)">
                    <h3>✨ Quick Insight</h3>
                    <div class="price">$25</div>
                    <div class="duration">15 minutes</div>
                    <p>Get a brief understanding of your life's purpose and direction</p>
                    <button class="btn">Book Now</button>
                </div>

                <div class="service-card" onclick="openBooking('Deep Dive', 75, 45)">
                    <h3>🔮 Deep Dive</h3>
                    <div class="price">$75</div>
                    <div class="duration">45 minutes</div>
                    <p>Comprehensive exploration of your purpose, values, and path forward</p>
                    <button class="btn">Book Now</button>
                </div>

                <div class="service-card" onclick="openBooking('Life Transformation', 150, 90)">
                    <h3>🌈 Life Transformation</h3>
                    <div class="price">$150</div>
                    <div class="duration">90 minutes</div>
                    <p>Complete life purpose analysis with actionable guidance and follow-up</p>
                    <button class="btn">Book Now</button>
                </div>
            </div>
        </div>

        <div class="about-section">
            <h2>Why Discover Your Purpose?</h2>
            <p>Understanding the purpose of your existence on Earth brings clarity, peace, and direction to your life. Through personalized consultations, you'll gain insights into your unique path, overcome confusion, and align with your true calling. Join thousands who have discovered their meaningful purpose.</p>
        </div>

        <div class="main-content">
            <h2 style="text-align: center; margin-bottom: 30px; color: #667eea;">What Others Say</h2>
            <div class="testimonials">
                <div class="testimonial">
                    <p>"This consultation changed my entire perspective on life. I finally understand why I'm here!"</p>
                    <div class="author">- Sarah M.</div>
                </div>
                <div class="testimonial">
                    <p>"Incredible wisdom and clarity. Worth every penny for the peace of mind it brought me."</p>
                    <div class="author">- James T.</div>
                </div>
                <div class="testimonial">
                    <p>"I was lost and confused. This session gave me the direction I desperately needed."</p>
                    <div class="author">- Maria L.</div>
                </div>
            </div>
        </div>

        <div class="footer">
            <p>&copy; 2025 Purpose of Life Consultations | Discover Your Meaning</p>
        </div>
    </div>

    <!-- Booking Modal -->
    <div id="bookingModal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal()">&times;</span>
            <h2 id="modalTitle">Book Your Session</h2>
            <p id="modalPrice" style="font-size: 1.5rem; color: #667eea; margin: 20px 0;"></p>
           
            <form id="bookingForm" onsubmit="processPayment(event)">
                <div class="form-group">
                    <label for="name">Full Name</label>
                    <input type="text" id="name" required>
                </div>
               
                <div class="form-group">
                    <label for="email">Email Address</label>
                    <input type="email" id="email" required>
                </div>
               
                <div class="form-group">
                    <label for="phone">Phone Number</label>
                    <input type="tel" id="phone" required>
                </div>
               
                <div class="form-group">
                    <label for="payment">Payment Method</label>
                    <select id="payment" required>
                        <option value="">Select payment method</option>
                        <option value="cashapp">Cash App</option>
                        <option value="paypal">PayPal</option>
                        <option value="venmo">Venmo</option>
                        <option value="zelle">Zelle</option>
                    </select>
                </div>
               
                <div class="form-group">
                    <label for="paymentHandle">Your Payment Username/Email</label>
                    <input type="text" id="paymentHandle" placeholder="e.g., $YourCashTag or email" required>
                </div>
               
                <div class="form-group">
                    <label for="date">Preferred Date</label>
                    <input type="date" id="date" required>
                </div>
               
                <div class="form-group">
                    <label for="time">Preferred Time</label>
                    <select id="time" required>
                        <option value="">Select a time</option>
                        <option value="9:00 AM">9:00 AM</option>
                        <option value="11:00 AM">11:00 AM</option>
                        <option value="1:00 PM">1:00 PM</option>
                        <option value="3:00 PM">3:00 PM</option>
                        <option value="5:00 PM">5:00 PM</option>
                        <option value="7:00 PM">7:00 PM</option>
                    </select>
                </div>
               
                <div class="form-group">
                    <label for="question">What brought you here today? (Optional)</label>
                    <textarea id="question" rows="3" placeholder="Share what you hope to discover..."></textarea>
                </div>
               
                <button type="submit" class="pay-btn">Complete Booking & Pay</button>
            </form>
           
            <div id="successMessage" class="success-message">
                <h3>🎉 Booking Confirmed!</h3>
                <p>Payment request sent to your Cash App. Please complete the payment to secure your session.</p>
                <p style="margin-top: 15px;">You'll receive a confirmation email shortly with session details.</p>
            </div>
        </div>
    </div>

    <script>
        let currentPrice = 0;
        let currentService = '';
        let totalEarnings = 0;

        function openBooking(service, price, duration) {
            currentPrice = price;
            currentService = service;
            document.getElementById('modalTitle').textContent = `Book ${service}`;
            document.getElementById('modalPrice').textContent = `$${price} - ${duration} minutes`;
            document.getElementById('bookingModal').style.display = 'block';
            document.getElementById('successMessage').style.display = 'none';
        }

        function closeModal() {
            document.getElementById('bookingModal').style.display = 'none';
            document.getElementById('bookingForm').reset();
        }

        function processPayment(event) {
            event.preventDefault();
           
            const name = document.getElementById('name').value;
            const email = document.getElementById('email').value;
            const paymentMethod = document.getElementById('payment').value;
            const paymentHandle = document.getElementById('paymentHandle').value;
            const date = document.getElementById('date').value;
            const time = document.getElementById('time').value;
           
            // Store booking info
            const booking = {
                service: currentService,
                price: currentPrice,
                name: name,
                email: email,
                paymentMethod: paymentMethod,
                paymentHandle: paymentHandle,
                date: date,
                time: time,
                timestamp: new Date().toISOString()
            };
           
            // Save to memory (in real app, this would go to a database)
            let bookings = JSON.parse(localStorage.getItem('bookings') || '[]');
            bookings.push(booking);
            localStorage.setItem('bookings', JSON.stringify(bookings));
           
            // Simulate payment processing
            setTimeout(() => {
                // Update earnings
                totalEarnings += currentPrice;
                document.getElementById('totalEarnings').textContent = totalEarnings;
               
                // Show success message
                document.getElementById('bookingForm').style.display = 'none';
                document.getElementById('successMessage').style.display = 'block';
               
                // Reset form after 3 seconds
                setTimeout(() => {
                    closeModal();
                    document.getElementById('bookingForm').style.display = 'block';
                }, 3000);
            }, 1000);
        }

        // Close modal when clicking outside
        window.onclick = function(event) {
            const modal = document.getElementById('bookingModal');
            if (event.target == modal) {
                closeModal();
            }
        }
    </script>
</body>
</html> 
