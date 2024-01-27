---
layout: project
type: project
image: img/hotel/hotel.jpeg
title: "Hotel Management"
date: 2023
published: true
labels:
  - C++
summary: "Developed a Hotel Management system in C++."
---

Last semester, my group was tasked to create a Hotel Management system for our final ICS 212 project. Our task was to develop a hotel management system in C++, designed to track all the rooms and customers in a hotel. Our group consisted of six people. The system we developed equipped user-friendly options such as checking in and out of rooms, searching for available rooms and customers, and several other functions. 

We had dedicated class time to work together in person and divided the project into individual sections that covered different parts of the system. We used an online platform called Replit. Replit allowed us to collaborate and share our work in real-time, which helped us stay coordinated and combine different parts of the project with ease. 

I worked on the  `checkInRoom()` and `Room()` functions that interact directly with the system's users. These functions were designed to collect data from users to create new rooms and customer entries. A challenge I experienced was validating the user input phone numbers. I had to implement regex (regular expressions) from the C++ library, a method that enabled the system to check and ensure that the input matched a specific pattern. 

This project helped me test my coding skills in C++. Working on this project showed me how important it is to communicate clearly and solve problems effectively and how it can be applied in software engineering. These skills helped bring our work together into one flowing working system. 

Here is code for my `checkInRoom()` function: 

 ```cpp
 //Checks in a room, prompts the user for data and inputs it into a new room and customer
void checkInRoom(vector<Room>& rooms, vector<Customer>& guests) {
    int roomNumber, index;
    cout << "Enter Room Number: ";
    cin >> roomNumber;
// goes through room vector to find the room number
    for(int i =0 ; i < rooms.size(); i++){
      if(rooms[i].getNumber() == roomNumber){
          index = i;
      }
    } //if room is available it will book the room
    if (rooms[index].isAvailable()) {
        rooms[index].book();

        string customerName, address, phoneNumber, bookingStart, bookingEnd;
        int bookingId, advancePayment, days;
        // asks user input
        cout << "Enter Booking ID: ";
        cin >> bookingId;
        cout << "Enter Customer Name: ";
        cin.ignore();  // Ignore newline character left in the buffer
        getline(cin, customerName);
        cout << "Enter Address: ";
        getline(cin, address);
        cout << "Enter Phone (ex: 123-123-1234): ";
        cin >> phoneNumber;
      //In order to validate that the user is inputting a phone number, we use regex. Which stands for regular expression, it is a way to check a string's input for a specific pattern. In this case the pattern is 3 digits followed by a dash, a second 3 digits, a dash, and then 4 digits. We then use regex_match to check if the phone number matches the pattern.
        regex phoneRegex("\\d{3}-\\d{3}-\\d{4}");
        if (!regex_match(phoneNumber, phoneRegex)) {
            cout << "Error: Invalid phone number" << endl;
            rooms[index].unbook();  // Unbook the room if phone number is invalid
            return;
        }

        cout << "Enter Check-In Date: ";
        cin >> bookingStart;
        cout << "Enter Check-Out Date: ";
        cin >> bookingEnd;
        cout << "Enter Advance Payment: ";
        cin >> advancePayment;
        // insert a new element at the end of the vector
        guests.emplace_back(customerName, address, phoneNumber, roomNumber, bookingStart, bookingEnd, advancePayment);

        cout << "Customer Checked-in Successfully.." << endl;
    } else {
        cout << "Room not available for check-in." << endl;
    }
}
```

