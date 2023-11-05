# PERMAINAN TIC TAC TOE

Pada praktikum modul 6 diberikan program untuk membuat permainan TicTacToe. Pemulis mengimplementasikan modul '**tkinter**' dalam bahasa pemograman Python untuk membuat program, permaian Tic-Tac-Toe sederhana.\
Berikut merupakan penjelasan dari setiap bagian program:
1. Import modul tkinter:\
   Program diawali dengan mengimpor modul **tkinter** dengan alias **tk**. Modul ini digunakan untuk membuat GUI (Graphical User Interface).
2. Deklarasi Kelas GameState:\
   Kelas **GameState** digunakan untuk mendefinisikan beberapa konstanta yang merepresentasikan status permainan. Ada empat kemungkinan status permainan, yaitu:
   - **PLAYING** (sedang berlangsung)
   - **DRAW** (seri)
   - **CROSS_WON** (X menang)
   - **NOUGHT_WON** (O menang)
3. Deklarasi Kelas Seed:\
   Kelas **Seed** digunakan untuk mendefinisikan konstanta yang merepresentasikan jenis isi dari sel-sel dalam papan permainan. Ada tiga kemungkinan isi sel:
   - **EMPTY** (kosong)
   - **CROSS** (X)
   - **NOUGHT** (O)
4. Deklarasi Kelas Cell:\
   Kelas **Cell** merepresentasikan sel dalam papan permainan. Setiap sel memiliki tiga atribut:
   - **content** untuk menunjukkan isi sel (berdasarkan kelas **Seed**)
   - **row** untuk menunjukkan baris sel
   - **col** untuk menunjukkan kolom sel\

    Kelas Cell memiliki tiga metode:
     - **clear** untuk mengosongkan isi sel
     - **paint** untuk menggambar sel di dalam elemen canvas dengan menggunakan tkinter. Sel yang berisi "X" digambar dengan garis-garis merah, dan sel yang berisi "O" digambar dengan lingkaran biru.
5. Deklarasi Kelas Board:\
   Kelas **Board** merepresentasikan papan permainan Tic-Tac-Toe. Kelas ini memiliki atribut **cells** yang berupa matriks 3x3 dari objek-objek **Cell**. Kelas Board memiliki beberapa metode:
   - **init** untuk mengosongkan sel-sel di papan permainan.
   - **is_draw** untuk mengecek apakah permainan berakhir seri (semua sel terisi).
   - **has_won** untuk mengecek apakah ada pemain yang menang dengan melihat baris, kolom, atau diagonal papan permainan.
   - **paint** untuk menggambar papan permainan ke dalam elemen canvas dengan menggunakan objek Cell.
6. Deklarasi Kelas GameMain:\
   Kelas **GameMain** adalah kelas utama program yang mengatur permainan dan tampilan GUI. Kelas ini memiliki beberapa atribut konstan yang digunakan untuk mengatur tampilan, seperti ukuran sel, lebar garis, dan sebagainya. Kelas GameMain memiliki beberapa metode:
   - **_ _ init _ _** untuk inisialisasi GUI dan papan permainan.
   - **init_game** untuk memulai permainan dengan mengosongkan sel-sel di papan.
   - **update_game** untuk memeriksa apakah ada pemain yang menang atau permainan berakhir seri.
   - **paint** untuk menggambar papan permainan di dalam elemen canvas.
   - **handle_click** untuk menangani klik mouse pengguna dan mengisi sel dengan "X" atau "O" sesuai giliran pemain.
7. Membuat instance Tkinter:\
   Program membuat instance dari kelas **Tk** dari modul tkinter sebagai root window.
8. Membuat instance GameMain:\
   Program membuat instance dari kelas **GameMain** dengan menggunakan root window sebagai parent.
9. Binding Event Click:\
   Program menggunakan metode **bind** untuk menghubungkan event klik kiri mouse (**"<Button-1>"**) ke metode **handle_click**.
10. Memulai Loop Utama:\
    Program memanggil metode **mainloop()** untuk memulai loop utama GUI, yang akan menangani interaksi pengguna dan pembaruan tampilan.

Program ini menciptakan permainan Tic-Tac-Toe yang dapat dimainkan melalui GUI. Pemain dapat mengklik sel-sel pada papan permainan, dan permainan akan memeriksa siapa yang menang atau apakah permainan berakhir seri.
