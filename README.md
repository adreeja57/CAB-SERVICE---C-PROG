
This C program simulates a simple ride-booking system, similar to what you might find in a basic cab service app.

Key Components
1. Data Structures

Driver: Represents a driver, storing their name and whether they are available.
User: Represents a user requesting a ride, storing their name, pickup, and drop locations.
Ride: Represents a ride, tying together a user, a driver, and a ride status string (e.g., "Ongoing", "Completed").
2. Global Variables

drivers[MAX_DRIVERS]: Array to store up to 5 drivers.
driverCount: Keeps track of how many drivers have been added.
3. Functions

void addDriver(const char* name):
Adds a driver to the system if there is room. Sets the driver as available.

Driver* findAvailableDriver():
Searches for the first available driver in the drivers array and returns a pointer to that driver; otherwise, returns NULL.

void requestRide(User user):
Handles a ride request:

Finds an available driver.
If found, creates a Ride, assigns the driver, marks the ride "Ongoing", and marks the driver as unavailable.
Immediately marks the ride as "Completed" and makes the driver available again (simulating a fast ride).
Prints ride assignment and completion messages.
If no driver is available, prints a message saying so.
4. Main Function

Adds two drivers ("Alice" and "Bob").
Creates three users, each with a name and pickup/drop locations.
Requests three rides for these users.
Each ride is assigned to an available driver (drivers are made available again after each ride, so all rides succeed if there are enough drivers).
