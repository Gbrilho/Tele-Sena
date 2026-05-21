# Tele-Sena
só gays (menos o gabriel e o jhonny)



public class TeleSena {

    // Valor fixo
    double valor = 10.0;

    // Dois conjuntos
    int[] jogo1 = new int[25];
    int[] jogo2 = new int[25];

    // Construtor
    public TeleSena() {

        preencherJogo(jogo1);
        preencherJogo(jogo2);
    }

    // Método para gerar números
    public void preencherJogo(int[] jogo) {

        for (int i = 0; i < jogo.length; i++) {

            int numero = (int)(Math.random() * 60 + 1);

            // Verifica repetição
            boolean repetido = false;

            for (int j = 0; j < i; j++) {

                if (jogo[j] == numero) {
                    repetido = true;
                }
            }

            // Se repetir, volta uma posição
            if (repetido) {
                i--;
            } else {
                jogo[i] = numero;
            }
        }
    }

    // Mostrar os jogos
    public void mostrarTeleSena() {

        System.out.println("JOGO 1:");

        for (int i = 0; i < jogo1.length; i++) {
            System.out.print(jogo1[i] + " ");
        }

        System.out.println();

        System.out.println("JOGO 2:");

        for (int i = 0; i < jogo2.length; i++) {
            System.out.print(jogo2[i] + " ");
        }

        System.out.println();
    }
}
