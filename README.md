# fibonacci-alg
public class Fibonacci {
    /*
     * 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89,… 
     * görüldüğü gibi ilk iki sayı hariç, 
     * her sayı kendisinden önce gelen 
     * iki sayının toplamına eşittir.
     */

    private int calculate(int length) {
        if (length < 0) {
            throw new IllegalArgumentException(
                    “Girilen Sayı 0 dan büyük olmalıdır”);
        }
        if (length <= 1) {
            return length;
        } else {
            return calculate(length – 1) + calculate(length – 2);
        }
    }

    public static void main(String[] args) {
        Fibonacci fibonacci = new Fibonacci();
        // 15 fibonacci sayısını gösterir.
        // artırabilirsiniz bu sayıyı
        for (int i = 1; i < 15; i++) {
            System.out.println(fibonacci.calculate(i));
        }
    }

}
