![image](https://github.com/TheDaniel3131/design-patterns-module-study-materials-notes-and-exercises/assets/71692327/016bdff5-05f5-4c8f-b78f-52ec90bbc3db)

Primitive Data Types (In Java):
1. boolean
2. int 
3. char
4. long
5. short
6. byte
7. float
8. double

API Class Types (In Java):
1. String
2. StringBuffer
3. Date
4. ArrayList

User-Defined Types (In Java):
1. Student
2. Hotel
3. Train
4. Flight

We always prefer to use dynamic array rather than fixed array. In Java, we use ArrayList because you can set any array size.

### Answer:
#### Clsas Diagram:
![image](https://github.com/TheDaniel3131/design-patterns-module-study-materials-notes-and-exercises/assets/71692327/ed0e427e-99e3-4711-a826-2831f7a4b266)

#### Source Code:
```java
import java.util.*;

class Hotel {
    String name;
    Hotel(String name) {
        this.name = name;
    }
    public String toString() {
        return "Hotel{" + "Hotel Name='" + name + '\'' + '}';
    }
}
 
class Flight {
    String flightNumber;
    Flight(String flightNumber) {
        this.flightNumber = flightNumber;
    }
    public String toString() {
        return "Flight{" + "Flight Name='" + flightNumber + '\'' + '}';
    }
}
 
class Train {
    String trainNumber;
    Train(String trainNumber) {
        this.trainNumber = trainNumber;
    }
    public String toString() {
        return "Train{" + "Train Name='" + trainNumber + '\'' + '}';
    }
}
 
class HotelBooker {
    ArrayList<Hotel> getHotelFor(Date from, Date to) {
        ArrayList<Hotel> hotels = new ArrayList<>();
        hotels.add(new Hotel("Hotel Ambassador"));
        hotels.add(new Hotel("Hotel Espira"));
        return hotels;
    }
}
 
class FlightBooker {
    ArrayList<Flight> getFlightsFor(Date from, Date to) {
        ArrayList<Flight> flights = new ArrayList<>();
        flights.add(new Flight("Flight Royal Brunei"));
        flights.add(new Flight("Flight Qatar Airways"));
        flights.add(new Flight("Flight AirAsia"));
        return flights;
    }
}
 
class TrainBooker {
    ArrayList<Train> getTrainsFor(Date from, Date to) {
        ArrayList<Train> trains = new ArrayList<>();
        trains.add(new Train("Train KLIA"));
        trains.add(new Train("Train KTM Commuter"));
        return trains;
    }
} 
 
class TravelFacade {
    private HotelBooker hotelBooker = new HotelBooker();
    private FlightBooker flightBooker = new FlightBooker();
    private TrainBooker trainBooker = new TrainBooker();
 
    void getFlightsAndHotels(Date from, Date to) {
        ArrayList<Flight> flights = flightBooker.getFlightsFor(from, to);
        ArrayList<Hotel> hotels = hotelBooker.getHotelFor(from, to);
        System.out.println("Flights: " + flights);
        System.out.println("Hotels: " + hotels);
    }
 
    void getTrainsAndHotels(Date from, Date to) {
        ArrayList<Train> trains = trainBooker.getTrainsFor(from, to);
        ArrayList<Hotel> hotels = hotelBooker.getHotelFor(from, to);
        System.out.println("Trains: " + trains);
        System.out.println("Hotels: " + hotels);
    }
}

public class Test {
    public static void main(String[] args) {
        TravelFacade facade = new TravelFacade();
        Date from = new Date();
        Date to = new Date();
        System.out.println("Searching for flights and hotels...");
        facade.getFlightsAndHotels(from, to);
        System.out.println("\nSearching for trains and hotels...");
        facade.getTrainsAndHotels(from, to);
    }
}
```
