# Parking_Lot
Getting Started with the Setup
Instructions to setup the project in local machine and run the test file
System Requirements:
Java 1.8
Apache Maven
Git (For Version Control)

Running the Test Cases:
Run the command bin/setup to install the build the project (Java, Maven assumed to be pre-installed on the system)
./bin/setup
Running with Bash
./bin/setup java -jar ../target/parking_lot-1.0-SNAPSHOT

Built With
Maven - Build/Dependency Management

Sample Test Cases & Outputs for Reference
Sample Case is incorporated into /functional_spec/fixtures/file_input.txt

To give custom input edit the main file configuration => edit configuration => (remove) the project arguments .

create_parking_lot 6
park KA-01-HH-1234 White
park KA-01-HH-9999 Black
park KA-01-BB-0001 Black
park KA-01-HH-7777 Black
park KA-01-HH-2701 Red
park KA-01-HH-3141 Green
leave KA-01-HH-3141 6
status
park KA-01-P-333 White
park DL-12-AA-9999 Red
leave KA-01-HH-1234 4
leave KA-01-BB-0001 6
leave DL-12-AA-9999 2
park KA-09-HH-0987 Red
park CA-09-IO-1111 Green
park KA-09-HH-0123 Yellow
status

Test Cases Usage:
The Exceptions are handled keeping actual real life scenario in mind:

Parking Lot Once Created Cannot be override (Singleton class).

Empty Slot Cannot be Emptied again.

Car with same Registration number is not allowed.

Car number not available in any slot then should throw error.

Slot will not be given if registration number or colour of the vehicle is not available.

Same slot is not provided for two different cars.

For Integration testing commands are checked for any invalid command or argument.

No Slots to be allocated if parking lot is full.

One Ticket to be generated per Car at a time (Singleton Class) to be passed to one thread at a time.

Checking the parking time and exit time and calculating hours and charge first 2 hours $10 and after 2 hours charge every hours charge $10.

No child threads are created so one operation at a time.
