# POOheypol
HERENCIA Y POLIMORFISMO
# Base
class Vehiculo:
    def __init__(self, marca):
        self.marca = marca

    def hacer_sonido(self):
        print("El vehículo hace un sonido genérico.")

 
class Auto(Vehiculo):
    def __init__(self, marca, puertas):
        super().__init__(marca)
        self.puertas = puertas

    def hacer_sonido(self):
        print(f"{self.marca} (Auto) dice: brum brum")


class Motocicleta(Vehiculo):
    def __init__(self, marca, tiene_casco):
        super().__init__(marca)
        self.tiene_casco = tiene_casco

    def hacer_sonido(self):
        print(f"{self.marca} (Motocicleta) dice: ñeeeeee,ñeñeeeeee")


if __name__ == "__main__":
    auto = Auto("Toyota", 4)
    moto = Motocicleta("Yamaha", True)

   
    vehiculos = [auto, moto]

    for vehiculo in vehiculos:
        vehiculo.hacer_sonido()  
