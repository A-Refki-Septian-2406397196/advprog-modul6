## Reflection 1

Di bagian ini, saya akhirnya paham kalau web server itu intinya cuma "mendengarkan" koneksi lewat address dan port tertentu. Karena biasanya pakai framework yang serba instan, saya jadi jarang melihat proses aslinya secara langsung. Lewat fungsi handle_connection, saya baru tahu kalau request browser itu aslinya cuma aliran data yang dibaca baris demi baris; meskipun belum muncul apa-apa di layar, rasanya seru bisa melihat koneksi beneran masuk ke program. Saya juga makin terbayang kenapa browser bisa kirim banyak request sekaligus untuk satu halaman saja. Pokoknya ini fondasi penting buat memahami cara server dan browser "ngobrol" tanpa bantuan framework besar.

## Reflection 2

Di tahap ini, web server buatan saya mulai terasa nyata karena akhirnya bisa menampilkan halaman HTML. Saya jadi paham kalau server harus mengirim response dengan format yang benar—seperti status_line dan Content-Length—supaya bisa dibaca browser. Ternyata, sekadar menampilkan satu halaman pun butuh struktur HTTP yang rapi. Saya juga belajar bagaimana file HTML dibaca dari proyek lalu dikirim sebagai body response. Intinya, hal-hal yang terlihat simpel di browser ternyata punya proses yang cukup detail di sisi server.

## Reflection 3

Di milestone ini, saya belajar kalau server harus bisa mengecek request untuk menentukan response yang pas, misalnya membedakan halaman utama dan 404. Di sinilah logika routing mulai terasa meski masih sederhana. Saya juga paham pentingnya refactoring supaya proses baca request dan penyusunan response lebih terpisah dan rapi. Intinya, menulis kode yang sekadar "jalan" itu belum cukup; struktur yang bagus sangat penting agar program tetap mudah dikembangkan saat makin besar.

## Reflection 4

Di bagian ini, saya akhirnya melihat langsung kelemahan server single-threaded lewat simulasi slow response. Begitu request /sleep jalan, semua antrean lain ikut tertahan karena satu thread cuma bisa memproses satu hal dalam satu waktu. Saya jadi paham bentuk nyata bottleneck yang selama ini cuma teori: kalau ada satu proses lambat, seluruh server jadi tidak responsif. Eksperimen ini penting banget karena memberi alasan logis kenapa kita butuh concurrency dalam membangun server yang andal.

## Reflection 5

