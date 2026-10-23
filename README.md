# Escala-RASS
Es un instrumento validado para medir de forma objetiva el nivel de agitación o sedación de un paciente


def escala_rass():
    niveles = {
        4: "Combativo: violento, peligro inmediato para el personal",
        3: "Muy agitado: conducta agresiva, intenta retirar tubos o catéteres",
        2: "Agitado: movimientos frecuentes y lucha con el ventilador",
        1: "Inquieto: ansioso, pero sin movimientos agresivos",
        0: "Alerta y tranquilo",
        -1: "Somnoliento: despierta al llamado verbal y mantiene contacto visual por más de 10 segundos",
        -2: "Sedación ligera: despierta brevemente al llamado verbal, contacto visual menor de 10 segundos",
        -3: "Sedación moderada: movimiento o apertura ocular al llamado verbal, sin contacto visual",
        -4: "Sedación profunda: no responde a la voz, pero se mueve o abre los ojos ante estímulo físico",
        -5: "Sin respuesta: no responde a la voz ni al estímulo físico"
    }

    print("=== ESCALA RASS ===")
    print("Escala de agitación y sedación")
    print("Ingresa un valor entre -5 y +4.")

    try:
        puntuacion = int(input("Puntuación RASS del paciente: "))

        if puntuacion in niveles:
            print("\nResultado:")
            print("Puntuación:", f"{puntuacion:+d}" if puntuacion > 0 else puntuacion)
            print("Interpretación:", niveles[puntuacion])
        else:
            print("Error: la puntuación debe estar entre -5 y +4.")

    except ValueError:
        print("Error: debes ingresar un número entero.")
