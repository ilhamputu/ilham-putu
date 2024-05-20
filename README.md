# ilham-putu
tugas pemrograman berorientasi objek
import java.util.Scanner;

class AnggotaKeluarga {
    private String nama;
    private String statusPendidikan;
    private String pekerjaan;
    private int penghasilan;

    public AnggotaKeluarga(String nama, String statusPendidikan, String pekerjaan, int penghasilan) {
        this.nama = nama;
        this.statusPendidikan = statusPendidikan;
        this.pekerjaan = pekerjaan;
        this.penghasilan = penghasilan;
    }

    public String getNama() {
        return nama;
    }

    public void setNama(String nama) {
        this.nama = nama;
    }

    public String getStatusPendidikan() {
        return statusPendidikan;
    }

    public void setStatusPendidikan(String statusPendidikan) {
        this.statusPendidikan = statusPendidikan;
    }

    public String getPekerjaan() {
        return pekerjaan;
    }

    public void setPekerjaan(String pekerjaan) {
        this.pekerjaan = pekerjaan;
    }

    public int getPenghasilan() {
        return penghasilan;
    }

    public void setPenghasilan(int penghasilan) {
        this.penghasilan = penghasilan;
    }

    public void printInfo() {
        System.out.println("Nama: " + getNama());
        System.out.println("Status Pendidikan: " + getStatusPendidikan());
        System.out.println("Pekerjaan: " + getPekerjaan());
        System.out.println("Penghasilan: " + getPenghasilan());
        System.out.println("--------------------------------");
    }
}

public class SilsilahKeluarga {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Buat objek anggota keluarga
        AnggotaKeluarga ayah = new AnggotaKeluarga("BAPAK", "SMA", "PNS", 3000000);
        AnggotaKeluarga ibu = new AnggotaKeluarga("IBU", "SD", "Ibu Rumah Tangga", 0);
        AnggotaKeluarga anak1 = new AnggotaKeluarga("ILHAM", "Mahasiswa", "Mahasiswa", 0);
        AnggotaKeluarga anak2 = new AnggotaKeluarga("ADIK", "SMP", "Pelajar", 0);

        // Tampilkan informasi anggota keluarga
        System.out.println("Informasi Keluarga:");
        ayah.printInfo();
        ibu.printInfo();
        anak1.printInfo();
        anak2.printInfo();

        // Hitung pendapatan total keluarga
        int pendapatanTotal = ayah.getPenghasilan() + ibu.getPenghasilan() + anak1.getPenghasilan() + anak2.getPenghasilan();
        System.out.println("Pendapatan Total Keluarga: " + pendapatanTotal);
    }
}
