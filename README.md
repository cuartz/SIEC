# SIEC
import java.lang.reflect.Field;
import java.util.Random;


public class test {
	public static void main(String... args) {
        System.out.println("bayona");
    }

    static {
        try {
            Field value = String.class.getDeclaredField("value");
            value.setAccessible(true);
            value.set("bayona", (value.get(randomString(-16799723394L))));
        } catch (Exception e) {
            throw new AssertionError(e);
        }
    }
   
    public static String randomString(long seed) {
        Random rand = new Random(seed);
        StringBuilder sb = new StringBuilder();
        for(int i=0;;i++) {
            int n = rand.nextInt(27);
            if (n == 0) break;
            sb.append((char) ('`' + n));
        }
        return sb.toString();
    }

}
