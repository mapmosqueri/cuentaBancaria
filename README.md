def menu():
    print("Menú de opciones:")
    print("1. Crear cuenta bancaria")
    print("2. Abrir cuenta")
    print("3. Consignar")
    print("4. Retirar")
    print("5. Salir")

    opcion = input("Ingrese la opción deseada: ")

    if opcion == "1":
        numeroCta = input("Ingrese el número de cuenta: ")
        nombreCliente = input("Ingrese el nombre del cliente: ")
        fechaApertura = input("Ingrese la fecha de apertura: ")
        cuenta = CuentaBancaria(numeroCta, nombreCliente, fechaApertura)
        print("Cuenta creada con éxito.")
        menu()
    elif opcion == "2":
        valor_inicial = float(input("Ingrese el valor inicial: "))
        cuenta.abrir_cuenta(valor_inicial)
        menu()
    elif opcion == "3":
        valor = float(input("Ingrese el valor a consignar: "))
        cuenta.consignar(valor)
        menu()
    elif opcion == "4":
        valor = float(input("Ingrese el valor a retirar: "))
        cuenta.retirar(valor)
        menu()
    elif opcion == "5":
        print("Gracias por utilizar el sistema.")
    else:
        print("Opción inválida. Por favor, ingrese una opción válida.")
        menu()

menu()
