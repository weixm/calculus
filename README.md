# calculus
public class Test {

	public static void main(String[] args) {
	    System.out.println("y=x^7的积分");
	    long l = System.nanoTime();
		int n = 1000000;float sum = 0f;
		float a = 0.0f;float b = 0.0f;
		for (int i = 0; i < n; i++) {
			a = (float) (i*0.0001);
			b = (float) ((i+1)*(0.0001));
			sum = (float) (sum +0.0001*((a+b)/2)*((a+b)/2)*((a+b)/2)*((a+b)/2)*((a+b)/2)*((a+b)/2)*((a+b)/2));
		}
	    System.out.println(sum);
	    long o = System.nanoTime();
		float e = 0.0f;float g = 0.0f;
		float[] d = new float[10000];
		for(int j = 0;j<d.length;j++){
			
	        g = (float) (100*Math.random());
	        d[j] = g*g*g*g*g*g*g;
	    
		}
		for (float f : d) {
			e = e + f;
		}
		float h = e/d.length;
//		float k = h*n;
		System.out.println(h);
		 long p = System.nanoTime();
		 System.out.println(o-l);
		 System.out.println(p-o);
		 System.out.println(p-l);
		 }

}
