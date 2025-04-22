# python-Assign 1
# Base class (Parent)
class Superhero:
    def __init__(self, name, power, origin):
        self.name = name
        self.power = power
        self.origin = origin
        self.__identity = f"{name} from {origin}"  

    def show_info(self):
        print(f"{self.name} possesses {self.power} powers and hails from {self.origin}.")

    def reveal_identity(self):
        print(f"Secret Identity: {self.__identity}")


# Subclass (Child) with Inheritance and Polymorphism
class FlyingHero(Superhero):
    def __init__(self, name, power, origin, wing_span):
        super().__init__(name, power, origin)
        self.wing_span = wing_span

    def show_info(self): 
        print(f"{self.name} soars with {self.wing_span}m wings and controls {self.power}!")


# Subclass with its own unique method
class TechHero(Superhero):
    def __init__(self, name, power, origin, gadgets):
        super().__init__(name, power, origin)
        self.gadgets = gadgets

    def use_gadget(self):
        print(f"{self.name} uses {', '.join(self.gadgets)} to fight crime.")

Assign 2
# Parent class
class Vehicle:
    def move(self):
        print("This vehicle moves in some way.")

# Child classes
class Car(Vehicle):
    def move(self):
        print("Driving 🚗")

class Plane(Vehicle):
    def move(self):
        print("Flying ✈️")

class Boat(Vehicle):
    def move(self):
        print("Sailing 🚢")

# Function demonstrating polymorphism
def travel(vehicle):
    vehicle.move()

