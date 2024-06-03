Baik, saya akan memfokuskan pada penjelasan fitur dan penggunaan library `lafzi.js-browser` di dalam README.md:

# lafzi.js-browser

`lafzi.js-browser` adalah versi browser-compatible dari library `lafzi.js`, yang memberikan cara mudah untuk mencari ayat-ayat Al-Quran menggunakan pelafalan Latin.

## Fitur

- Pencarian ayat Al-Quran menggunakan pelafalan Latin
- Mendukung mode pencarian "verse" (ayat) dan "non-verse"
- Pengaturan ambang batas kesamaan hasil pencarian (0.3 - 0.95)
- Opsi untuk menyoroti hasil pencarian pada teks ayat
- Opsi untuk menampilkan beberapa hasil pencarian dalam satu ayat

## Penggunaan

```javascript
const options = {
  query: 'kunfayakun',
  mode: 'v', // "v" untuk ayat, "nv" untuk non-ayat
  threshold: 0.95, // Ambang batas kesamaan (0.3 - 0.95)
  isHilight: true, // Menyoroti hasil pencarian
  multipleHighlightPos: false, // Izinkan beberapa sorotan dalam satu ayat
};

lafziJs(options).then((results) => {
  console.log(results);
});
```
Jangan lupa menyertakan lib js-nya.
```html
<script src="https://cdn.jsdelivr.net/gh/agusibrahim/lafzijs-browser@master/lafzi.min.js"></script>
```

## Opsi

- `query`: Kueri pencarian (pelafalan Latin).
- `mode`: Mode pencarian, "v" untuk ayat atau "nv" untuk non-ayat.
- `threshold`: Ambang batas kesamaan untuk hasil pencarian (antara 0.3 dan 0.95).
- `isHilight`: Apakah menyoroti hasil pencarian dalam teks ayat.
- `multipleHighlightPos`: Apakah mengizinkan beberapa sorotan dalam satu ayat yang sama.

## Contoh

Anda dapat menemukan contoh penggunaan library di direktori `example/`. Untuk menjalankan contoh, ikuti langkah-langkah berikut:

1. Salin repository:
   ```
   git clone https://github.com/your-username/lafzi.js-browser.git
   ```
2. Instal dependensi:
   ```
   cd lafzi.js-browser
   npm install
   ```
3. Jalankan server pengembangan:
   ```
   npm start
   ```
4. Buka browser Anda dan navigasi ke `http://localhost:8080`.

## Lisensi

Proyek ini dilisensikan di bawah [Lisensi MIT](LICENSE).