# Car Parking Management System

A console-based **Car Parking Lot Management System** written in **C++** using Object Oriented Programming concepts. The program parks cars in a lot with limited capacity, shows the lot status, and calculates the parking fee when a car leaves.

## Features

- Park a vehicle (with a check that the lot is not full)
- Remove a vehicle by plate number and calculate the parking fee
- Display lot status: capacity, occupied slots, free slots and the parked vehicles
- Fee calculation: **Rs. 50 per hour**
- Clear messages for every action (success, lot full, vehicle not found)

## OOP Concepts Used

| Concept | Where it is used |
|---------|------------------|
| **Abstraction** | `Vehicle` is an abstract class with the pure virtual function `calculateFee()` |
| **Inheritance** | `Car` inherits from `Vehicle` |
| **Polymorphism** | `calculateFee()` is overridden in `Car` and called through a `Vehicle*` pointer |
| **Encapsulation** | Data members like `plateNumber`, `capacity` and `count` are `protected` / `private` and accessed through member functions |
| **Constructors** | `Vehicle`, `Car` and `ParkingLot` initialize their data using constructors |

## Class Overview

- **`Vehicle`** (abstract): stores the plate number and declares `calculateFee(int hours)`
- **`Car`** : derived from `Vehicle`; fee = hours × 50
- **`ParkingLot`**: manages the slots with `parkVehicle()`, `removeVehicle()` and `displayStatus()`

## How to Compile and Run

Requires a C++ compiler such as `g++`.

```bash
g++ myproject.cpp -o parking
./parking
```

On Windows:

```bash
g++ myproject.cpp -o parking.exe
parking.exe
```

> The program prints emojis. If they do not display correctly in the Windows console, run `chcp 65001` first.

## Sample Output (shortened)

```
========================================
🚘 Welcome to Car Parking Lot System 🚘
========================================

----------------------------------
🚗 Attempting to park vehicle...
✅ Vehicle [BMW M5 F90-360] parked successfully.
Current Occupancy: 1/3
----------------------------------

========== Parking Lot Status ==========
Capacity: 3 | Occupied: 3 | Free Slots: 0
Vehicles currently parked:
 - Slot 1: BMW M5 F90-360
 - Slot 2: Corvette C8-45
 - Slot 3: AUDI RS6-320
========================================

>>> Removing vehicle AUDI RS6 after 2 hours...

----------------------------------
🚗 Attempting to remove vehicle...
✅ Vehicle [AUDI RS6-320] removed successfully.
Parking Duration: 2 hour(s)
Total Fee: Rs.100
Current Occupancy: 2/3
----------------------------------
```

## Project Files

| File | Description |
|------|-------------|
| `myproject.cpp` | Complete C++ source code |
| `Car parking lot Management system.pptx` | Project presentation |

## Possible Future Improvements

- Add more vehicle types (Bike, Bus) with their own fee rates
- Add a user menu so the user can park and remove vehicles interactively
- Save parking records to a file

## Author

**Ali Raza** – BS Computer Science student, Abasyn University Islamabad
