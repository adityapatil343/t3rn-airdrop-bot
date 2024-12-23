# Auto Bridge Bot

Auto Bridge Bot adalah script Python untuk mengelola transaksi otomatis antar jaringan blockchain menggunakan Web3. Script ini mendukung jaringan seperti OP Sepolia, Base Sepolia, dan jaringan lain.

## Fitur
- **Transaksi Otomatis**: Mengirimkan transaksi otomatis antar jaringan yang dipilih.
- **Estimasi Gas**: Menghitung gas yang diperlukan untuk setiap transaksi.
- **Pemantauan Saldo**: Menampilkan saldo ETH dan BRN setelah transaksi berhasil.
- **Interaksi dengan Explorer**: Memberikan tautan langsung ke explorer blockchain untuk setiap transaksi.
- **Menu Interaktif**: Memilih jaringan dan mode operasi secara langsung melalui terminal.

## Prasyarat
Sebelum menjalankan script, pastikan Anda telah menginstal dan mengonfigurasi:

1. **Python** (Versi 3.7 atau lebih baru)
2. **Dependensi Python**:
   - `web3`
   - `eth_account`
3. **File Konfigurasi**:
   - `data_bridge.py`: Berisi data untuk setiap bridge.
   - `keys_and_addresses.py`: Berisi kunci pribadi, alamat, dan label akun.

## Instalasi
1. Clone repository ini:
   ```bash
   git clone https://github.com/adhe222/T3rn-bot.git
   cd T3rn-bot
   ```

2. Instal dependensi:
   ```bash
   pip install web3 eth_account
   ```

3. Konfigurasi file:
   - Lengkapi `data_bridge.py` dengan data bridge.
   - Masukkan kunci pribadi dan alamat ke dalam `keys_and_addresses.py`.

## Penggunaan
1. Jalankan script dengan perintah:
   ```bash
   python t3rn-bot.py
   ```

2. Pilih salah satu opsi di menu:
   - **1**: OP -> Base Sepolia
   - **2**: Base -> OP Sepolia
   - **3**: Jalankan semua transaksi secara berulang.

3. Script akan memproses transaksi dan menampilkan hasilnya di terminal, termasuk:
   - Alamat pengirim
   - Gas yang digunakan
   - Nomor blok
   - Saldo ETH dan BRN
   - Tautan ke explorer blockchain
### `keys_and_addresses.py`
Contoh format:
```python
private_keys = [
    "0xYourPrivateKey1",
    "0xYourPrivateKey2"
]

my_addresses = [
    "0xYourAddress1",
    "0xYourAddress2"
]

labels = [
    "Account 1",
    "Account 2"
]
```

### `data_bridge.py`
Contoh data bridge:
```nano data_bridge.py
data_bridge = {
    "OP - BASE": "0xDataForOPToBaseBridge",
    "BASE - OP": "0xDataForBaseToOPBridge"
}
```
## Catatan Keamanan
- Jangan pernah membagikan kunci pribadi Anda.
- Pastikan file konfigurasi hanya diakses oleh Anda.
- Gunakan jaringan testnet (seperti Sepolia) untuk pengujian sebelum menerapkan di mainnet.
source: https://github.com/airdropinsiders/t3rn-bot

## Lisensi
Proyek ini dilisensikan di bawah lisensi MIT. Anda bebas menggunakan, memodifikasi, dan mendistribusikannya.
