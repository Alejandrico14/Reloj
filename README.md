
package reloj;

public class Reloj {

    public static void main(String[] args) {
        
        int horas=0,minutos=59, segundos=56;
        
        while(true){
          //Mostrar
          if(horas<10){
              System.out.print("0");
          }
          
          System.out.print(horas+":");
          
          if(minutos<10){
              System.out.print("0");
          }
          System.out.print(minutos+":");
          
          if(segundos<10){
              System.out.print("0");
              
          }
          
          System.out.println(segundos);
          
          //Aumentar 1 segundo bru
          segundos++;
          
          //checar el tiempo.
          
          if(segundos==60){
              segundos=0;
              minutos++;
              if(minutos==60){
                  minutos=0;
                  horas++;
                  if(horas==24){
                      horas=0;
                  }                   
              }
          }
            try {
                Thread.sleep(1000);
            } catch (InterruptedException ex) {
            }
    }
    
    }
}

