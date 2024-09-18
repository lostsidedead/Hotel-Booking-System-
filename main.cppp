#include <iostream>
#include <vector>
#include <string>

using namespace std;

class Room {
public:
    int roomNumber;
    bool isAvailable;
    double pricePerNight;
    string roomType;

    Room(int roomNum, string type, double price) {
        roomNumber = roomNum;
        isAvailable = true;
        pricePerNight = price;
        roomType = type;
    }

    void showDetails() {
        cout << "Room Number: " << roomNumber
             << " | Type: " << roomType
             << " | Price per Night: $" << pricePerNight
             << (isAvailable ? " | Available" : " | Booked") << endl;
    }
};

class Hotel {
private:
    vector<Room> rooms;

public:
    Hotel() {
        // Initializing with some predefined rooms
        rooms.push_back(Room(101, "Single", 100));
        rooms.push_back(Room(102, "Double", 150));
        rooms.push_back(Room(103, "Suite", 250));
        rooms.push_back(Room(104, "Single", 100));
        rooms.push_back(Room(105, "Double", 150));
    }

    void showAvailableRooms() {
        cout << "\nAvailable Rooms:\n";
        for (const auto& room : rooms) {
            if (room.isAvailable) {
                room.showDetails();
            }
        }
    }

    void bookRoom(int roomNumber, int nights) {
        for (auto& room : rooms) {
            if (room.roomNumber == roomNumber) {
                if (room.isAvailable) {
                    room.isAvailable = false;
                    cout << "Room " << room.roomNumber << " booked successfully for " << nights
                         << " nights. Total cost: $" << room.pricePerNight * nights << endl;
                } else {
                    cout << "Sorry, room " << roomNumber << " is already booked." << endl;
                }
                return;
            }
        }
        cout << "Room number not found." << endl;
    }

    void cancelBooking(int roomNumber) {
        for (auto& room : rooms) {
            if (room.roomNumber == roomNumber) {
                if (!room.isAvailable) {
                    room.isAvailable = true;
                    cout << "Booking for room " << room.roomNumber << " has been cancelled." << endl;
                } else {
                    cout << "Room " << roomNumber << " is not currently booked." << endl;
                }
                return;
            }
        }
        cout << "Room number not found." << endl;
    }

    void showAllRooms() {
        cout << "\nAll Rooms:\n";
        for (const auto& room : rooms) {
            room.showDetails();
        }
    }
};

int main() {
    Hotel hotel;
    int choice;

    while (true) {
        cout << "\nHotel Booking System Menu:\n";
        cout << "1. Show Available Rooms\n";
        cout << "2. Book a Room\n";
        cout << "3. Cancel Booking\n";
        cout << "4. Show All Rooms\n";
        cout << "5. Exit\n";
        cout << "Enter your choice: ";
        cin >> choice;

        switch (choice) {
            case 1:
                hotel.showAvailableRooms();
                break;
            case 2: {
                int roomNumber, nights;
                cout << "Enter the room number to book: ";
                cin >> roomNumber;
                cout << "Enter the number of nights: ";
                cin >> nights;
                hotel.bookRoom(roomNumber, nights);
                break;
            }
            case 3: {
                int roomNumber;
                cout << "Enter the room number to cancel booking: ";
                cin >> roomNumber;
                hotel.cancelBooking(roomNumber);
                break;
            }
            case 4:
                hotel.showAllRooms();
                break;
            case 5:
                cout << "Exiting the system..." << endl;
                return 0;
            default:
                cout << "Invalid option, please try again." << endl;
        }
    }

    return 0;
}
