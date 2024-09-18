# Hotel Booking System - C++ Project

This project is a **Hotel Booking System** implemented in C++. It allows users to view available rooms, book a room for a specified number of nights, cancel a room booking, and view all rooms (whether booked or available).

## Features

1. **Show Available Rooms**: Users can view a list of all the rooms that are currently available for booking.
2. **Book a Room**: Users can book a room by entering the room number and the number of nights they wish to stay. The system calculates and displays the total cost.
3. **Cancel Booking**: Users can cancel a room booking by providing the room number, making it available again for others to book.
4. **Show All Rooms**: Displays all rooms in the system, including both available and booked rooms.
5. **Exit**: Users can exit the system.

## How to Use

1. Clone or download the project files.
2. Open the terminal and navigate to the project directory.
3. Compile the C++ code using the following command:

    ```
    g++ hotel_booking.cpp -o hotelBooking
    ```

4. Run the program:

    ```
    ./hotelBooking
    ```

5. Follow the on-screen instructions to navigate the hotel booking system.

## Menu Options

- **1. Show Available Rooms**: Displays a list of rooms that are available for booking, including room number, type, and price per night.
- **2. Book a Room**: Users can select a room by its number and specify the number of nights for the booking. The system calculates the total cost and confirms the booking.
- **3. Cancel Booking**: Allows users to cancel a previously booked room, making it available again for others.
- **4. Show All Rooms**: Shows all rooms, indicating whether they are booked or available.
- **5. Exit**: Exits the program.

## Room Types and Prices

- **Single Room**: $100 per night
- **Double Room**: $150 per night
- **Suite**: $250 per night

## Example

1. The user selects **"Show Available Rooms"** to view all rooms that are currently available.
2. To book a room, the user selects **"Book a Room"**, enters the room number, and the number of nights they want to stay. The total cost is calculated and displayed.
3. If a room booking needs to be canceled, the user can choose **"Cancel Booking"** by entering the room number.
4. **"Show All Rooms"** lists all rooms with their availability status.

## Future Improvements

- Add customer details when booking rooms.
- Store room bookings in a file for persistence across sessions.
- Implement different payment methods.
