# Assignment

###python

# Base Class
class Superhero:
    def __init__(self, name, power, weakness):
        self.name = name
        self.power = power
        self.weakness = weakness

    def show_identity(self):
        return f"I am {self.name}, and my power is {self.power}!"

# Derived Class
class FlyingSuperhero(Superhero):
    def __init__(self, name, power, weakness, flight_speed):
        super().__init__(name, power, weakness)
        self.flight_speed = flight_speed

    def fly(self):
        return f"{self.name} flies at {self.flight_speed} km/h!"

# Example Usage
hero1 = Superhero("Shadow Knight", "Invisibility", "Bright light")
hero2 = FlyingSuperhero("Sky Falcon", "Laser Vision", "Low oxygen", 200)

print(hero1.show_identity())
print(hero2.show_identity())
print(hero2.fly())

###python

# Parent Class
class Vehicle:
    def move(self):
        pass

# Subclass for Cars
class Car(Vehicle):
    def move(self):
        return "Driving 🚗"

# Subclass for Planes
class Plane(Vehicle):
    def move(self):
        return "Flying ✈️"

# Subclass for Boats
class Boat(Vehicle):
    def move(self):
        return "Sailing 🚤"

# Example Usage
vehicles = [Car(), Plane(), Boat()]

for vehicle in vehicles:
    print(vehicle.move())