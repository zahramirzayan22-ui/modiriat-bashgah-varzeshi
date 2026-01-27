# نمودار کلاس سیستم باشگاه ورزشی

mermaid
classDiagram
    %% تعریف کلاس‌ها
    class Member {
        -id: int
        -name: string
        -email: string
        -phone: string
        -joinDate: Date
        +register(): void
        +renewMembership(): void
        +makeReservation(classId: int): Reservation
        +cancelReservation(reservationId: int): boolean
    }
    
    class Trainer {
        -id: int
        -name: string
        -specialty: string
        -hourlyRate: float
        +addClass(class: Class): void
        +getSchedule(date: Date): Class[]
    }
    
    class Class {
        -id: int
        -name: string
        -description: string
        -capacity: int
        -schedule: DateTime
        +isFull(): boolean
        +getAvailableSlots(): int
        +addToWaitlist(member: Member): void
    }
    
    class Reservation {
        -id: int
        -reservationDate: DateTime
        -status: string
        -paymentId: int
        +confirm(): void
        +cancel(): boolean
        +checkIn(): void
    }
    
    class Payment {
        -id: int
        -amount: float
        -paymentDate: DateTime
        -paymentMethod: string
        +processPayment(): boolean
        +generateReceipt(): string
    }
    
    %% تعریف روابط بین کلاس‌ها
    Member "1" -- "*" Reservation : makes
    Member "*" -- "*" Class : attends
    Trainer "1" -- "*" Class : teaches
    Class "1" -- "*" Reservation : has
    Reservation "1" -- "1" Payment : has
    ```