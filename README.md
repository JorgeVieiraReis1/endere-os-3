# endere-os-3
teste-pwc
 import java.util.Arrays;
    public class Address {
      public static void main(String[] args){
        String[] inputs = {
          "Miritiba 339",
          "Babaçu 500",
          "Cambuí 804B",
          "Rio Branco 23",
          "Quirino dos Santos 23 b",
          "4, Rue de la République",
          "100 Broadway Av",
          "Calle Sagasta, 26",
          "Calle 44 No 1991"
          };
        String[][] resp = {
          {"Miritiba", "339"},
          {"Babaçu", "500"},
          {"Cambuí", "804B"},
          {"Rio Branco", "23"},
          {"Quirino dos Santos", "23 b"},
          {"Rue de la République", "4"},
          {"Broadway Av", "100"},
          {"Calle Sagasta", "26"},
          {"Calle 44", "No 1991"}
        };
        checkAddress(inputs, resp);
      
      }
      
      private static boolean arraysEquals(String[] vetor1, String[] vetor2){
        if (vetor1.length != vetor2.length) return false;
        for (int i = vetor1.length -1; i >= 0; --i){
          if (!vetor1[i].equals(vetor2[i])) return false;
        }
        return true;
      }
      
      private static void checkAddress(String[] vetor, String[][] matriz){
        String[] got, expected;
        for (int i = 0; i < vetor.length; ++i){
          got = arrayAddress(vetor[i]);
          expected = matriz[i];
          if (!arraysEquals(got, expected)){
            System.out.println("\nEsperado: " + Arrays.toString(expected));
            System.out.println("Recebido: " + Arrays.toString(got));
          }
        }    
      }
      
      private static String[] arrayAddress(String address){
       
        String[] array = {};   
        return array;  
      }

      public Address() {
      }

      @Override
      public String toString() {
        return "Address []";
      }  
       
}
