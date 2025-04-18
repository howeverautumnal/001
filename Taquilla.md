Proceso TaquillaCine
	
	// Variables
Definir opcion, cantidad, total, edad, precioFinal Como Entero
Definir ventas1, ventas2, ventas3 Como Entero
Definir precio1, precio2, precio3 Como Entero

	// Precios de las pelis
precio1 <- 2500
precio2 <- 3000
precio3 <- 2800

ventas1 <- 0
ventas2 <- 0
ventas3 <- 0

	// Menú 
Repetir
	Limpiar Pantalla
	Escribir "=========================================="
	Escribir "         TAQUILLA DE CINE - MENÚ          "
	Escribir "=========================================="
	Escribir "1. ---------            - ", precio1, " colones"
	Escribir "2. ---------            - ", precio2, " colones"
	Escribir "3. ---------            - ", precio3, " colones"
	Escribir "------------------------------------------"
	Escribir "4. Ver resumen de ventas"
	Escribir "5. Salir"
	Escribir "------------------------------------------"
	Escribir "Seleccione una opción: "
	Leer opcion
	
	// Opción 1
Si opcion = 1 Entonces
		Limpiar Pantalla
		Escribir "¿Cuántos boletos desea comprar para -------------?"
		Leer cantidad
		Escribir "Ingrese la edad del comprador:"
		Leer edad
		
		// Aplicar descuento
Si edad < 12 Entonces
			precioFinal <- precio1 / 2
		Sino
			Si edad >= 65 Entonces
				precioFinal <- precio1 * 0.7
			Sino
				precioFinal <- precio1
			FinSi
		FinSi
		
total <- precioFinal * cantidad
		ventas1 <- ventas1 + cantidad
		Escribir "Total a pagar (con descuento si aplica): ", total, " colones"
		Esperar Tecla
		
	// Opción 2
Sino
		Si opcion = 2 Entonces
			Limpiar Pantalla
			Escribir "¿Cuántos boletos desea comprar para ---------?"
			Leer cantidad
			Escribir "Ingrese la edad del comprador:"
			Leer edad
			
			// Aplicar descuento
Si edad < 12 Entonces
				precioFinal <- precio2 / 2
			Sino
				Si edad >= 65 Entonces
					precioFinal <- precio2 * 0.7
				Sino
					precioFinal <- precio2
				FinSi
			FinSi
			
total <- precioFinal * cantidad
			ventas2 <- ventas2 + cantidad
			Escribir "Total a pagar (con descuento si aplica): ", total, " colones"
			Esperar Tecla
			
		// Opción 3
Sino
			Si opcion = 3 Entonces
				Limpiar Pantalla
				Escribir "¿Cuántos boletos desea comprar para -------------?"
				Leer cantidad
				Escribir "Ingrese la edad del comprador:"
				Leer edad
				
				// Aplicar descuento
Si edad < 12 Entonces
					precioFinal <- precio3 / 2
				Sino
					Si edad >= 65 Entonces
						precioFinal <- precio3 * 0.7
					Sino
						precioFinal <- precio3
					FinSi
				FinSi
				
total <- precioFinal * cantidad
				ventas3 <- ventas3 + cantidad
				Escribir "Total a pagar (con descuento si aplica): ", total, " colones"
				Esperar Tecla
				
			// Opción 4
Sino
				Si opcion = 4 Entonces
					Limpiar Pantalla
					Escribir "=========================================="
					Escribir "           RESUMEN DE VENTAS              "
					Escribir "=========================================="
					Escribir "------------- : ", ventas1, " boletos - ", ventas1 * precio1, " colones"
					Escribir "-----------   : ", ventas2, " boletos - ", ventas2 * precio2, " colones"
					Escribir "-------------- : ", ventas3, " boletos - ", ventas3 * precio3, " colones"
					Esperar Tecla
				FinSi
			FinSi
		FinSi
	FinSi
	
Hasta Que opcion = 5

Escribir "Gracias por visitar nuestra taquilla."
