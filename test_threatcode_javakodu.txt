public class RiskliKodOrnegi {
    public static void main(String[] args) {
        String kullaniciGirdisi = new Scanner(System.in).nextLine();
        int sayi = Integer.parseInt(kullaniciGirdisi); // Güvenlik açığı: SQL injection
        
        String sqlSorgu = "SELECT * FROM kullanicilar WHERE id = " + sayi; // SQL injection
        // ... SQL sorgusunu çalıştırma kısmı
        
        List<String> liste = new ArrayList<>();
        for (int i = 0; i <= liste.size(); i++) // IndexOutOfBoundsException riski
            System.out.println(liste.get(i));
    }
}
