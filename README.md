# PRATIKUM_CONSTRUCTION.SETTERGETTER

link = "https://github.com/BAGAZDWI33/prototipe.git"

diatas adalah link untuk run dalam intelij IDEA tugas PRATIKUM5

## MATERI CONSTRUCTOR
Constructor, adalah mekanisme yang disediakan pada class untuk membuat object baru dari class tersebut. Dengan menyediakan constructor kita dapat memberikan syarat untuk pembuatan class yang nantinya dapat digunakan untuk melakukan inisialisasi nilai tertentu pada fields kelas bersangkutan. Proses ini sejatinya mirip dengan memberikan argumen pada sebuah method.\n

code construktor

public class pegawai {
    private String Nama;
    private double GajiPokok;


    pegawai(String Nama, double GajiPokok) {
        this.Nama = Nama;
        this.GajiPokok = GajiPokok;
    }



Constructor sebuah class dibuat menggunakan nama class bersangkutan (pada contoh di atas pegawai), kemudian parameter yang dibutuhkan oleh constructor tersebut (pada contoh: Nama, GajiPokok). Perhatikan bahwa cara ini serupa dengan saat kita mendeklarasikan parameter pada sebuah method.

Masing-masing baris ini berisi pemberian nilai (assignment) pada setiap field milik object yang dibuat dari class bersangkutan.

this.Nama = Nama; Ekspresi this merujuk pada instance (object dari class bersangkutan), sehingga this.Nama pada sebelum tanda “=” merujuk pada field Nama, sedangkan Nama setelah tanda “=” merujuk pada nilai argumen yang dikirim ke constructor.

code konstruktor lainnya 

public class programmer extends pegawai {
    private double Bonus;

    programmer (double Bonus) {
        super("BAGAS DWI PRASETYO ",5000000);
        this.Bonus = Bonus;
}

pada constructor diatas menggunakan super() untuk memanggil class sebelumnya dan menambahkan this.bonus = bonus pada class programmer

code constructor lainnya

public class manager extends pegawai{
    private double Tunjangan;

    public manager(double Tunjangan){
        super("SHODIK KURNAYA",5000000);
        this.Tunjangan = Tunjangan;

    }


pada constructor diatas masih sama menggunakan super() untuk memanggil class sebelumnya dan parameter diisi sesuai argumen yang diinginkan pada class super. dengan parameter nama dan GajiPokok, diisi sesuai keperluan yang dimiliki programmer inginkan(contoh diatas = nama BAGAS DWI PRASETYO/ SHODIK KURNAYA,GajiPokok 50000000)

## menggunakan overriding 
 code override


 
    float Nama() {
        System.out.println("Nama : "+this.Nama) ;
        return 0;
    }

    float GajiPokok() {
        System.out.println("GajiPokok "+ this.GajiPokok);
        return 0;
    }

code override lainnya

 @Override
    float Nama() {
        return super.Nama();
    }
    @Override
    float GajiPokok() {
        return super.GajiPokok();
    }




    @Override
    float Nama() {
        return super.Nama();
    }

    @Override
    float GajiPokok() {
        return super.GajiPokok();
    }


## menggunakan setter getter

code setter getter 

    public void setNama(String Nama){
        this.Nama = Nama;
    }
    public void  setGajiPokok(double GajiPokok){
        this.GajiPokok = GajiPokok;
    }
    public String getNama(){
        return this.Nama;
    }
    public double getGajiPokok(){
        return this.GajiPokok;
    }
    void cetakinfo(){
        System.out.println("Nama : "+getNama());
        System.out.println("GajiPokok : "+ getGajiPokok());
    }

code setter getter lainnya

 //setter
    public void setBonus(double Bonus){
        this.Bonus = Bonus;
    }
    public double getBonus(){
        return this.Bonus;
    }


    void cetakInfo() {
        super.cetakinfo();
        System.out.println("Bonus = " + getBonus());

    }



    //setter
    public void settunjangan(double Tunjangan){
        this.Tunjangan = Tunjangan;
    }
    public double gettunjangan(){
        return this.Tunjangan;
    }
    void cetakInfo() {
        super.cetakinfo();
        System.out.println("Tunjangan : " + gettunjangan());

    }


    pada setter getter penggunaan super.cetakinfo(); digunakan untuk memanggil setter getter di class utama atau class pegawai.


    penggunaan overload

    public class MainConstruktor {
    public static void main(String[] args) {
        manager manager = new manager(8000000);
        programmer anto = new programmer(7000000);

        manager.cetakinfo();
        System.out.println("Tunjangan : "+ manager.gettunjangan()+"\n");

        anto.cetakinfo();
        System.out.println("Bonus : " + anto.getBonus());




    }
}


pada manager.cetakinfo(); ini menggunakan overload agar class sebelumnya terpanggil dan terpilih sesuai apa yang ingin di print orang yang menjalankan program java ini. 


hasil akhir terdapat di img = Screenshot1,
                              Screenshot2,
                              Screenshot3,
                              Screenshot4,
                              Screenshot5,

pada kode sebelum penambahan constructor sudah tidak diperlukan lagi, karena nilai-nilai untuk fields pegawai bersangkutan sudah dikirim melalui parameter pada constructor. Dari contoh ini terlihat bahwa dengan adanya constructor instansiasi object dan pemberian nilai pada fields yang dimiliki object tersebut menjadi lebih sederhana.

sekian dan terima kasih

by.BAGAS DWI PRASETYO (312110053) 