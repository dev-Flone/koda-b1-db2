# ERD E-Wallet
``` mermaid
erDiagram
    direction TB

    USER ||--|{ TRANSAKSI: "melakukan (pengirim)"
    USER ||--|{ TRANSAKSI: "menerima (penerima)"
    USER ||--|{ TOP-UP: melakukan

    TRANSAKSI {
        int id_transaksi PK
        int id_user FK
        int id_penerima FK
        int jumlah_transaksi
        string status
        date tanggal_transaksi
    }
    TOP-UP {
        int id_top-up PK
        int norek_user FK
        int jumlah_topup
        date tanggal_topup
    }
    USER {
        int id_user PK
        int norek_user FK
        string nama_user
        int saldo
    }

```