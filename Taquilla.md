Proceso TaquillaCine
	
	// variables
	Definir opcion, cantidad, total Como Entero
	Definir ventas1, ventas2, ventas3 Como Entero
	Definir precio1, precio2, precio3 Como Entero
	
	// Los precios de las pelis=
	precio1 <- 2500
	precio2 <- 3000
	precio3 <- 2800
	
	ventas1 <- 0
	ventas2 <- 0
	ventas3 <- 0
	
	// Menú
	Repetir
		Limpiar Pantalla
		Escribir "======= Taquilla de Cine ======="
		Escribir "1. --------- - ", precio1, " colones"
		Escribir "2. --------- - ", precio2, " colones"
		Escribir "3. --------- - ", precio3, " colones"
		Escribir "4. Ver resumen de ventas"
		Escribir "5. Salir"
		Escribir "Seleccione una opción: "
		Leer opcion
		
		// boletos
		Si opcion = 1 Entonces
			Escribir "¿Cuántos boletos desea comprar para -------------?"
			Leer cantidad
			total <- precio1 * cantidad
			ventas1 <- ventas1 + cantidad
			Escribir "Total a pagar: ", total, " colones"
			Esperar Tecla
			
		Sino
			Si opcion = 2 Entonces
				Escribir "¿Cuántos boletos desea comprar para ---------?"
				Leer cantidad
				total <- precio2 * cantidad
				ventas2 <- ventas2 + cantidad
				Escribir "Total a pagar: ", total, " colones"
				Esperar Tecla
				
			Sino
				Si opcion = 3 Entonces
					Escribir "¿Cuántos boletos desea comprar para -------------?"
					Leer cantidad
					total <- precio3 * cantidad
					ventas3 <- ventas3 + cantidad
					Escribir "Total a pagar: ", total, " colones"
					Esperar Tecla
					
				Sino
					Si opcion = 4 Entonces
						Limpiar Pantalla
						Escribir "======= Resumen de Ventas ======="
						Escribir "-------------: ", ventas1, " boletos - ", ventas1 * precio1, " colones"
						Escribir "-----------: ", ventas2, " boletos - ", ventas2 * precio2, " colones"
						Escribir "--------------: ", ventas3, " boletos - ", ventas3 * precio3, " colones"
						Esperar Tecla
					FinSi
				FinSi
			FinSi
		FinSi
		
	Hasta Que opcion = 5
	
	Escribir "¡Gracias por visitar nuestra taquilla!"

FinProceso

