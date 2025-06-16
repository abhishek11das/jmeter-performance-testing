# Performance Testing with JMeter (Booking API)

## Project Overview
This project performs **Load Testing** and **Stress Testing** on a booking API using JMeter. Users log in, create bookings with randomized data and search the booking.

## Project Instructions (As Provided)
- Create a Collection of APIs (JMeter Collection) of Login API, Create Booking API, and Search API HTTP requests.
 Add the following properties to the Header Controller:
  - Accept: `*/*`

- **Login**  
  - URL: `https://restful-booker.herokuapp.com/auth`  
  - Body:
    ```json
    {
      "username": "admin",
      "password": "password123"
    }
    ```

- **Create Booking**  
  - URL: `https://restful-booker.herokuapp.com/booking`  
  - Body:
    ```json
    {
      "firstname": "Generate Random FirstName",
      "lastname": "Generate Random LastName",
      "totalprice": Generate random amount,
      "depositpaid": true,
      "bookingdates": {
        "checkin": "2024-01-01",
        "checkout": "2024-01-02"
      }
    }
    ```

- **Search Booking**  
  - URL: `https://restful-booker.herokuapp.com/booking/<booking_id>`
 
## Project Scenario

This project involves performance testing of the **Restful Booker API** using Apache JMeter. The objective is to simulate real-world user behavior where users:
- Login to the system
- Create bookings with random data
- Search for the booking using the generated booking ID

The performance testing is divided into two main parts:
1. **Load Testing:** Simulating up to 120,000 users over 12 hours (compressed into 5, 10, and 20-minute intervals).
2. **Stress Testing:** Gradually increasing load to identify the system's failure or bottleneck point.

## 🛠️ Tools & Features
- Apache JMeter
- Gaussian Timer
- Random Variable Controller
- Excel
- HTML Report Generation

## Prerequisites
- Apache JMeter installed
- Java JDK 17.0.12 (LTS) installed and configured in your system PATH

## Performance Testing Results: HTML Report Screenshots
### 📸 Load Test HTML Report Screenshot
![image alt](https://github.com/abhishek11das/jmeter-performance-testing/blob/55a5688773ea6a6d8e1b3ca30494b58e718a1966/Load%20Test.png)

### 📸 Stress Test HTML Report Screenshot
![image alt](https://github.com/abhishek11das/jmeter-performance-testing/blob/55a5688773ea6a6d8e1b3ca30494b58e718a1966/Stress%20Test.png)




