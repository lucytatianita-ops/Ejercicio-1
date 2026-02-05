# Ejercicio-1
import statistics

def calcular_promedio():
    """
    Algoritmo para analistas: Calcula el promedio de ventas diarias.
    """
    print("--- 📊 Analizador de Ventas Diarias ---")
    ventas = []

    while True:
        entrada = input("Ingrese el valor de la venta (o escriba 'fin' para terminar): ").lower().strip()
        
        if entrada == 'fin':
            break
        
        try:
            valor = float(entrada)
            ventas.append(valor)
        except ValueError:
            print("❌ Error: Ingrese un número válido.")

    if ventas:
        promedio = statistics.mean(ventas)
        total_ventas = sum(ventas)
        
        print("\n" + "="*30)
        print(f"📈 RESULTADOS DEL ANÁLISIS:")
        print(f"Total de días: {len(ventas)}")
        print(f"Venta Total: ${total_ventas:,.2f}")
        print(f"Promedio Diario: ${promedio:,.2f}")
        print("="*30)
    else:
        print("⚠️ No se ingresaron datos para analizar.")

if __name__ == "__main__":
    calcular_promedio()
