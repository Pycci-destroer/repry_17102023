# repry_17102023
import java.math.BigDecimal;
import java.math.MathContext;
import java.math.RoundingMode;
import java.util.Scanner;

public class physic {

    public static void main(String[] args){
        Scanner k = new Scanner(System.in);
        Scanner o = new Scanner(System.in);
        Scanner p = new Scanner(System.in);
        Scanner j = new Scanner(System.in);
        Scanner sh = new Scanner(System.in);
        Scanner lg = new Scanner(System.in);
        //System.out.println("Введите массу тела в кг");



        //double m = k.nextDouble();
        System.out.println("Введите угол в градусах");

        double a = o.nextDouble()*(3.14/180);
        System.out.println("Введите начальную скорость в м/c");
        double v = p.nextDouble();
        System.out.println("Введите х координату объекта");
        double x1 = sh.nextDouble();
        System.out.println("Введите y координату объекта");
        double y1 = lg.nextDouble();
        System.out.println("Ускорение свободного падение будет равным 10 м/c^2");


        double g =10;

        System.out.println("Дано:"+ ' '+ /*m + "кг" */+ ' ' + a +"град" + ' ' + v + "м/c");
        System.out.println("Если надо найти L Введите 1, Если H введите 2");
        int sol = j.nextInt();
        double L = 0;
        double H = 0;
        double x0 = 0.00;
        double y0 = 0.00;






        if(sol==1){

            L+=((Math.pow(v, 2 )*Math.sin(2*a)))/g;
            MathContext context = new MathContext(1,RoundingMode.HALF_UP);
            BigDecimal ichod = new BigDecimal(L,context);
            System.out.println(ichod);
        }
        if (sol==2){
            H+=(Math.pow(v,2)*Math.pow(Math.sin(a),2))/(2*g);
            //H+=1;
            //System.out.println(H);
            MathContext context = new MathContext(1, RoundingMode.HALF_UP);
            BigDecimal ichod = new BigDecimal(H,context);
                System.out.println(ichod);



        }






    }
}
