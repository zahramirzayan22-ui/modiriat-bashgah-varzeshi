```mermaid
classDiagram
    class Member {
        -id: int
        -name: string
        -membershipType: string
        +register()
        +makeReservation()
    }
    
    class Reservation {
        -id: int
        -date: DateTime
        -status: string
        +confirm()
        +cancel()
    }
    
    class Class {
        -id: int
        -name: string
        -time: DateTime
        -capacity: int
        +checkAvailability()
    }
    
    Member --> Reservation : creates
    Reservation --> Class : reserves
    Member --> Class : attends
    ```