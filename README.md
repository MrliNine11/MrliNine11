
Kandula Aditya Sitaram, nr 317444
EiTi PW
Preliminary project 
CAR RALLY 


AIM OF THE PROJECT
The following project aims to design an application that does the following tasks:
•	Provide the user with the schedules of car races happening.
•	Give access to add a car rally or schedule a car rally with players etc. 
•	Creates the list of all participants and shows the list of all the races they are participating in.
•	Can show no of tickets available in the following race stadium.
•	Can show the results and records of all the racers.
•	Presenting all data
•	Can prevent operations that are against restrictions.
CLASS DEFINITIONS:

The following class Race shows all the races that are completed as well as the upcoming races. It also helps edit the information about the upcoming race (venue, timing, racers, etc… .).

class Race
{
public:

	Race();	// Constructor
	~Race();	// Destructor
	void Add_Player;
	void Delete_Player;
	

private:

	string Name;
	string address;
	string Owner;
	string CarModel;
	Race *next;
};

Class date works to show dates and the number of races on a particular day. The user can select a date and can see all the races on the selected date and will have access to book tickets to a race on the selected date.  
class date
{
public:

	date();	// Constructor
	~date();	// Destructor
	void Add_race();
	void Delete_race();
	void Get_address();

private:

	string address;
	int trackDistance;
	double date;
	Race *next;
	date *next;
};

Class Racer describes the Player’s data such as the name of the participant, sponsor of the team, model of his car used in the race and his remuneration.
class Racer
{
public:

	Racer(string Name, string Owner, string CarModel, double pay);	// Constructor
	~Racer();	// Destructor

private:

	string Name;
	string Owner;
	string CarModel;
double payment;
	Racer *next;

};

The following class result describes the results in the race with the timings of each racer in the race.

class result
{
public:

	result(); // Constructor
	~result(); // Destructor
	int Get_time();		// Method that gives finish time of each player
	void Set_Next();

private:

	string racer;
	int FinishTime;
	string winner;
	race *next;

};

Class tickets is a class that registers and creates all the audients and allot them places in the stadium.

class tickets
{
public:

	tickets(); // Constructor
	~tickets(); // Destructor
	int Get_Pnumber();		// Method that gives finish time of each player
	void Set_Next();
	int num_seats();

private:

	string aud_name;
	string stadium;
	int P_number;
	tickets*next;
	int capacity;
	int remainingSeats;

};



RESTRICTIONS
1.	Racer
1.	Cannot be present in more than one Race at a time or on a single day.
2.	Race
1.	Cannot have fewer than 6 Racers to play a race.
2.	The maximum number of Players is 8.
3.	There cannot be more than a race at the same venue at the same time
3.	Tickets
1.	Cannot be more than the capacity of the stadium.
OBJECT MAP

 


![image](https://user-images.githubusercontent.com/97223689/148361688-2aca0710-d97f-4f7c-abbe-3349a6a58e42.png)


