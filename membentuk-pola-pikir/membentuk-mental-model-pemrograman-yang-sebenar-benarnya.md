# Membentuk Pola Pikir
## Membentuk Mental Model Pemrograman Yang "Sebenar-benarnya"
Ketika kita pertama kali mempelajari suatu hal, sering kali kita mencari sebuah perumpamaan dari hal yang kita ketahui, kemudian kita hubungkan dengan apa yang dipelajari.

Pada tahap awal, menurut saya ini memang diperlukan, dan bahkan bukan suatu hal yang bisa kita kendalikan. Akan tetapi, perlu diingat bahwa perumpamaan yang kita gunakan bisa jadi tidaklah sama persis dengan yang kenyataannya.

Sebagai contoh, saat awal belajar pemrograman, saya melihat di dalam `if` adalah sebuah "kondisi" dengan format perbandingan antara dua hal, jika dia benar, maka kode di dalamnya akan jalan.

```js
// 1 tidak sama dengan 2, benar!
if (1 != 2) {
	console.log('Halo!')
}
```

Ketika dihadapkan hal yang sesuai dengan apa yang saya tangkap, tidak ada masalah, saya bisa memahami beberapa penggunaan `if` lainnya.

```js
// Jika nama = bambang, maka akan jalan!
if (nama == 'Bambang') {
	console.log('Nama kamu Bambang!');
}
```

Namun, hal ini jadi masalah ketika `if` ini diisi dengan hal lain. Misalnya, diisi sebuah teks dan angka.

```js
// Loh, ini kan bukan "kondisi", kok jalan??
if (2 && 'a') {
	console.log('A');
}

// Ini diisi angka dan huruf juga, tapi kok ga jalan??
if (0 && 'b') {
	console.log('B');
}
```

Ternyata, setelah saya belajar lebih lanjut, yang sebenarnya dibaca oleh komputer bukan lah sebuah teks "kondisi" dengan format perbandingan dua hal, melainkan sebuah jenis data `boolean` yang nilainya antara `true` atau `false`.

Jika `true`, maka dia baru jalan. Dan `true`/`false` ini pun juga bisa kita pakai tanpa menulis sebuah "kondisi"!

```js
if (true) {
	console.log('Jalan!');
}
```

Tapi, kalau harus `boolean` yang mana antara `true` atau `false`, lalu kenapa `1 != 2` tadi bisa jalan?

Ternyata saya temui lagi, ketika kita coba mencetak "kondisi", nanti secara otomatis akan dikonversi menjadi sebuah `boolean`!

```js
console.log(1 != 2);
// Output: true
```

Kemudian hal itu juga saya praktikan ke jenis data lainnya, seperti huruf dan angka, menggunakan bantuan function `Boolean()`  bawaan Javascript untuk mengkonversinya.

```js
console.log(Boolean(2));
// Output: true

console.log(Boolean(0));
// Output: false

console.log(Boolean('a'));
// Output: true
```

Sejak saat itu saya mulai menyadari bahwa saat belajar, sebisa mungkin hindarilah asumsi-asumsi yang kamu dapat dari perumpamaan, dan segeralah berusaha untuk mencari referensi lebih banyak agar bisa mendapat pemahaman yang sebenar-benarnya.