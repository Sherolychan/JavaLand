# JavaLand
import java.text.DecimalFormat; 
public class NewtonRoot{
	public static void main (String args[]){
		double x,y,c;
		c=Double.parseDouble(args[0]);
		x=Math.random();
		DecimalFormat df = new DecimalFormat("0.0000");
		while(Math.abs(x*x-c)>1e-4)
		{
			y=x*x-c;
			x=(2*x-y)/(2*x);
		}
		System.out.println(c+"的平方根是："+df.format(x));
	}
}
