# TallerExcepciones
Juan jose Rodriguez Lozano (2419084)
Samuel Banguero Ortega (2418671)
Steven Aragon (2418804)

Ejercicio#1:
R//a: Se lanza una excepcion de tipo ArithmeticException.
R//b: La consola muestra un mensaje de error, menciona el tipo de excepcion aritmetica, y nos señala que fue por la razon / by zero. (division por cero)

Ejercicio#2:
------------------------------------------------------------------------------------------------------------------------------------
try
            {
                int a = 10;
                int b = 0;
                System.out.println("Resultado: " + (a / b));
            }catch(Exception e) {
                System.out.println("Error, you're making an arithmetic mistake! ->: " + e);
            }
------------------------------------------------------------------------------------------------------------------------------------
Ejercicio#3:
try {
                Scanner sc = new Scanner(System.in);
                int number1;
                System.out.println("Ingrese el numero numero 1");
                number1 = sc.nextInt();
                int number2;
                System.out.println("Ingrese el numero numero 2");
                number2 = sc.nextInt();
                
                int Operation = number1/number2;

                System.out.println("El resultado es: "+Operation);

            }catch (ArithmeticException e1)
            {
                System.out.println("Error, you're making an arithmetic mistake! ->:" + e1);
            }catch (InputMismatchException e2) {
                System.out.println("Error, you can only enter NUMBERS!!!!" + e2);
            }
------------------------------------------------------------------------------------------------------------------------------------
Ejercicio#4:
try {
            Scanner sc = new Scanner(System.in);
            int number1;
            System.out.println("Ingrese el numero numero 1");
            number1 = sc.nextInt();

            int number2;
            System.out.println("Ingrese el numero numero 2");
            number2 = sc.nextInt();

            int Operation = number1 / number2;

            System.out.println("El resultado es: " + Operation);

        }catch (ArithmeticException e1)
        {
            System.out.println("Error, you're making an arithmetic mistake! ->:" + e1);
        }catch (InputMismatchException e2) {
            System.out.println("Error, you can only enter NUMBERS!" + e2);
        } finally {
            System.out.println("Operacion Finalizada ");
        }
------------------------------------------------------------------------------------------------------------------------------------
Ejercicio#5:
try {
            var resource = HelloApplication.class.getResource("hello-view2.fxml");

            if (resource == null) {
                throw new IllegalArgumentException("FXML file not found: hello-view2.fxml");
            }

            FXMLLoader fxmlLoader = new FXMLLoader(resource);
            fxmlLoader.load();
            //No se encuentra la excepcion, se interpreta como que sera un mensaje
        } catch (IllegalArgumentException e) {
            System.out.println("Error: " + e.getMessage());
        } catch (IOException e) {
            System.out.println("Error loading FXML: " + e.getMessage());
        }
------------------------------------------------------------------------------------------------------------------------------------

