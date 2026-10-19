# ERD E-Wallet
``` mermaid
erDiagram
    direction TB

    USER ||--|{ TRANSAKSI: "melakukan (pengirim)"
    USER ||--|{ TRANSAKSI: "menerima (penerima)"
    USER ||--|{ TOP_UP: melakukan

    TRANSAKSI {
        int id_transaksi PK
        int id_pengirim FK "merujuk ke id_user sebagai pengirim"
        int id_penerima FK "merujuk ke id_user sebagai penerima"
        int nominal_transaksi
        string status
        date tanggal_transaksi
    }
    TOP_UP {
        int id_top-up PK
        int id_user FK
        int nominal_topup
        date tanggal_topup
    }
    USER {
        int id_user PK
        int norek_user FK
        string nama_user
        int saldo
    }

```