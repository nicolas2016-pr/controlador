# controlador

from datetime import datetime
from models import Familia, Plastico, Vidrio, Lata
from views import mostrar_resumen

def main():
    familia = Familia("Familia López", 4, "Calle Falsa 123")
    
    # Registrar materiales
    familia.registrar_material(Plastico(3.5, datetime.now()))
    familia.registrar_material(Vidrio(2.0, datetime.now()))
    familia.registrar_material(Lata(5.0, datetime.now()))

    # Mostrar resumen
    mostrar_resumen(familia)

if __name__ == "__main__":
    main()
