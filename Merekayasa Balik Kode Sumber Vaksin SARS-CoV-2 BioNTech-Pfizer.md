# Merekayasa Balik Kode Sumber Vaksin SARS-CoV-2 BioNTech/Pfizer

(artikel asli ditulis oleh Bert Hubert)

Selamat datang! Pada artikel ini, kita akan mengamati kode sumber dari vaksin mRNA BioNTech/Pfizer SARS-CoV-2 berdasarkan ciri-ciri.

> * Saya menghaturkan terima kasih banyak kepada sejumlah besar orang yang
> meluangkan waktu untuk mempratinjau artikel ini untuk memastikan keterbacaan
> dan ketepatan. Seluruh kesalahan tetaplah milik saya, namun saya akan dengan
> senang hati menerima tanggapan Anda segera pada bert@hubertnet.nl atau
> [@PowerDNS_Bert](https://twitter.com/PowerDNS_Bert)*

Pernyataan ini mungkin agak mengejutkan - vaksin adalah sebuah cairan yang disuntikkan ke lengan. Bagaimana bisa kita membicarakan kode sumber (source code)? 

Ini adalah suatu pertanyaan bagus, sekarang kita mulai dengan bagian kecil dari kode sumber vaksin BioNTech/Pfizer ini, juga disebut sebagai [BNT162b2](https://id.wikipedia.org/wiki/BNT162b2), alias Tozinameran [alias Comirnaty](https://twitter.com/PowerDNS_Bert/status/1342109138965422083).

<center>
<img src="https://berthub.eu/articles/bnt162b2.png">

500 karakter pertama dari mRNA BNT162b2. Sumber: [World Health Organization](https://mednet-communities.net/inn/db/media/docs/11889.doc)
</center>

Pada pusat vaksin mRNA BNT162b, terdapat kode digital ini. Kode ini sepanjang 4284 karakter, sehingga dapat dimuat dalam sejumlah tweet. Pada permulaan proses produksi vaksin, seseorang mengunggah kode ini ke sebuah printer DNA (memang ada), yang kemudian mengkonversi byte dalam disket menjadi molekul DNA asli.

<center>
<img src="https://berthub.eu/articles/bioxp-3200.jpg">

Printer DNA BioXp 3200 produk [Codex DNA](https://codexdna.com/products/bioxp-system/)
</center>

Dari mesin tersebut keluarlah sejumlah kecil DNA, yang setelah diproses secara biologis dan kimiawi menjadi RNA (akan dibahas lebih jauh nanti) di dalam botol kecil vaksin. Dosis 30 mikrogram vaksin ini mengandung 30 mikrogram RNA. Di samping itu, ada juga sistem pengemasan berlemak yang menyalurkan mRNA kepada sel tubuh kita.

RNA adalah versi 'memori bekerja' yang volatil dari DNA. DNA diumpamakan sebagai flash disk-nya biologi. DNA sangat tahan lama, secara internal bersifat rendundan dan andal. Namun sebagaimana komputer tidak mengeksekusi kode secara langsung dari flash disk, sebelum sesuatu terjadi, kode diduplikasikan ke sebuah sistem yang lebih cepat dan serbaguna namun juga tidak tahan lama.

Umpamanya, jika pada komputer kita mengenal RAM, pada biologi kita mengenal RNA. Kemiripan ini begitu jelas. Tidak seperti flash disk, RAM sangat mudah menghilang kecuali bila diurus dengan penuh perhatian. Begitu juga dengan alasan vaksin mRNA Pfizer/BioNTech harus disimpan dalam pembeku yang paling dingin; RNA bersifat tidak tahan lama.

Tiap karakter RNA memiliki bobot seberat 0.53&middot;10⁻²¹ gram, yang berarti
ada 6&middot;10¹⁶ karakter dalam tiap dosis vaksin 30 mikrogram. Dinyatakan dalam byte, jumlahnya sekitar 25 petabyte, namun dapat juga dikatakan bahwa jumlah ini mengandung 2000 miliar pengulangan dari 4284 karakter yang sama. Kandungan informatif sebenarnya dari vaksin ini hanyalah lebih dari satu kilobyte.  [SARS-CoV-2 sendiri](https://www.ncbi.nlm.nih.gov/projects/sviewer/?id=NC_045512&tracks=[key:sequence_track,name:Sequence,display_name:Sequence,id:STD649220238,annots:Sequence,ShowLabel:false,ColorGaps:false,shown:true,order:1][key:gene_model_track,name:Genes,display_name:Genes,id:STD3194982005,annots:Unnamed,Options:ShowAllButGenes,CDSProductFeats:true,NtRuler:true,AaRuler:true,HighlightMode:2,ShowLabel:true,shown:true,order:9]&v=1:29903&c=null&select=null&slim=0) memiliki bobot sekitar 7.5 kilobyte.

Bagian tersingkat dari latar belakangnya
------------------------------
DNA adalah sebuah kode digital. Tidak seperti komputer yang menggunakan 0 dan 1 (sistem biner), pada organisme digunakan A, C, G, dan U/T (nukleotida, nukleosida, atau basa).


Pada komputer kita menyimpan 0 dan 1 sebagai kehadiran dan ketiadaan suatu muatan, tegangan, transisi magnetik, modulasi sinyal, ataupun perubahan pada daya pemantulan. Singkatnya, 0 dan 1 bukanlah sebuah konsep abstrak - mereka hadir sebagai elektron dan pada banyak wujud fisik lainnya.

Pada organisme, A, C, G, dan U/T adalah molekul yang disimpan sebagai rantai dalam DNA (atau RNA).

Pada komputer, kita mengelompokkan 8 bit sebagai sebuah byte, dan byte adalah unit khas dari data yang diproses.

Organisme mengelompokkan 3 nukleotida menjadi sebuah kodon, dan kodon ini adalah unit khas dari pemrosesan. Tiap kodon mengandung 6 bit informasi (2 bit tiap karakter DNA, 3 karakter = 6 bit. Ini artinya 2⁶ = 64 nilai kodon yang berbeda).

Cukup digital sejauh ini. Apabila ragu, [silakan buka dokumen WHO](https://mednet-communities.net/inn/db/media/docs/11889.doc) dengan kode digital ini untuk melihatnya sendiri.

> *Bahan bacaan lebih lanjut [tersedia di
> sini](https://berthub.eu/articles/posts/what-is-life/) - tautan ini ('What
> is life') mungkin dapat membantu Anda memahami lebih jauh tentang artikel ini.
> Atau, jika Anda suka video, saya punya [materi dua jam](https://berthub.eu/dna).*

Jadi apa FUNGSI kode tersebut?
--------------------------
Gagasan sebuah vaksin ialah melatih sistem imun tubuh kita untuk melawan sebuah patogen, tanpa menyebabkan kita jatuh sakit. Secara historis ini dilakukan dengan menyuntikkan sebuah virus yang dilemahkan, dipadukan dengan sebuah adjuvan untuk "menakuti" sistem imun kita agar bekerja. Ini adalah sebuah teknik analog pasti yang melibatkan milyaran telur (atau serangga). Teknik ini juga membutuhkan keberuntungan besar dan waktu yang lama. Kadangkala virus berbeda (tidak terkait) juga digunakan dalam prosesnya.

Vaksin mRNA memenuhi hal yang sama (mengedukasi sistem imun kita) namun dengan cara yang serupa dengan laser. Maksud saya ialah dalam kedua pengertiannya - sangat sempit namun sangat kuat.

Jadi beginilah cara kerjanya. Sesuntik vaksin mRNA mengandung materi genetis bersifat volatil yang mendeskripsikan protein spike SARS-CoV-2 yang terkenal itu. Melalui langkah kimiawi yang cerdik, vaksin tersebut mampu menyalurkan materi genetis ini menuju beberapa sel tubuh kita.

Sel-sel ini kemudian mulai memproduksi protein spike SARS-CoV-2 dalam jumlah yang cukup besar hingga sistem imun kita mulai bekerja. Berkonfrontasi dengan protein spike dan (yang paling penting) pertanda bahwa sel-sel ini telah dikuasai, sistem imun kita menciptakan sebuah respon kuat untuk melawan beragam aspek dari protein spike ini dan proses produksinya.

Dan inilah penjelasan dari vaksin yang 95% efisien ini.

Kode sumbernya!
----------------
[Mari kita mulai dari paling awal, ini adalah tempat awal yang paling bagus](https://youtu.be/jp0opnxQ4rY?t=8). Dokumen WHO di atas mencantumkan gambar penting ini:

<center>
<img src="https://berthub.eu/articles/vaccine-toc.png">
</center>

Ini adalah semacam daftar isi. Kita akan mulai dari bagian "cap", yang sungguh digambarkan sebagai sebuah topi kecil.

Sebagaimana kita tidak bisa memasukkan opcode ke dalam file suatu komputer dan menjalankannya begitu saja, sistem operasi biologis membutuhkan header, memiliki linker dan hal-hal seperti konvensi panggilan.

Kode vaksin ini dimulai dengan dua nukleotida ini:

```
GA
```

Nukleotida ini dapat dibandingkan persis dengan tiap [executable DOS dan Windows yang dimulai dengan MZ](https://en.wikipedia.org/wiki/DOS_MZ_executable), atau script UNIX yang dimlau dengan [`#!`](https://en.wikipedia.org/wiki/Shebang_(Unix)). Baik dalam organisme maupun sistem operasi, kedua karakter ini tidak akan dieksekusi dengan cara apapun. Namun kedua karakter ini harus ada di sana, bila tidak maka kode tidak akan berjalan sama sekali.

"Topi" mRNA tersebut [menyimpan sejumlah fungsi](https://en.wikipedia.org/wiki/Five-prime_cap#Function). Pertama, ia menandai kode sebagai berasal dari inti sel. Dalam kasus ini tentu saja bukan begitu adanya, kode ini berasal dari vaksinasi. Namun kita tak perlu memberitahukan sel tubuh kita. Topi tersebut membuat kode ini tampak sah, sehingga melindunginya dari kemungkinan lenyap.

Dua nukleotida GA pertama juga secara kimiawi sedikit berbeda dari keseluruhan lain RNA. Ini artinya, pada nukleotida GA ini terdapat out-of-band signaling.

Ujung five-prime yang tidak tertranslasi
------------------------------------
Ada keanehan di sini. Molekul RNA hanya bisa dibaca pada satu arah. Yang membingungkan, bagian di mana pembacaan dimulai disebut sebagai 5' atau five-prime. Pembacaan berhenti pada 3' atau akhiran three-prime.

Organisme terdiri dari protein (atau hal-hal yang tersusun dari protein), dan protein ini dijelaskan di dalam RNA. Ketika RNA dikonversikan menjadi protein, ini disebut translasi.

Di sini kita memiliki ujung 5' yang tak tertranslasi (UTR), sehingga bagian ini tidak masuk ke dalam protein:

```
GAAΨAAACΨAGΨAΨΨCΨΨCΨGGΨCCCCACAGACΨCAGAGAGAACCCGCCACC
```

Di sinilah kejutan pertama kita. Karakter normal RNA adalah A, C, G, dan U. U juga ditulis sebagai T di dalam DNA. Namun di sini kita menemukan Ψ, ada apa sebenarnya ini?

Inilah salah satu keistimewaan vaksin. Tubuh kita menjalankan suatu sistem antivirus yang kuat, atau kata lainnya "asli". Karena inilah, sel tubuh kita amat tidak ramah terhadap RNA asing dan mencoba sebisa mungkin menghancurkannya sebelum RNA tersebut melakukan sesuatu.

Ini adalah suatu masalah bagi vaksin RNA ini - ia harus mencari celah untuk memasuki sistem imun kita. Melalui bertahun-tahun eksperimen, ditemukan bahwa jika U pada RNA diganti dengan sebuah molekul yang dimodifikasi sedikit, sistem imun kita tidak akan tertarik melawannya. Asli.

Sehingga pada vaksin BioNTech/Pfizer, setiap U diubah oleh 1-methyl-3'-pseudoridylyl, ditandai dengan Ψ. Uniknya ialah walaupun Ψ pengganti ini menenangkan sistem imun kita, ia diterima sebagai U normal oleh bagian relevan sel tubuh.

Dalam keamanan komputer dikenal juga trik serupa - terkadang kita dapat mengirimkan versi sedikit rusak dari sebuah pesan yang membingungkan firewall dan sistem keamanan, namun masih diterima oleh server backend - yang kemudian bisa diretas.

Kita sekarang menuai manfaat dari riset ilmiah mendasar dari masa lampau. Para [penemu](https://twitter.com/PennMedicine/status/1341766354232365059) teknik Ψ harus berjibaku agar riset [mereka](https://www.statnews.com/2020/11/10/the-story-of-mrna-how-a-once-dismissed-idea-became-a-leading-technology-in-the-covid-vaccine-race/) dibiayai dan diterima. Kita harus bersyukur, dan saya yakin [riset ini akan diganjar penghargaan Nobel dalam waktu yang akan tiba](https://twitter.com/PowerDNS_Bert/status/1329861047168225281).

> Banyak orang telah menanyakan, bisakah virus juga menggunakan teknik Ψ
> untuk menaklukkan sistem imun kita? Singkat kata, ini sangat tidak mungkin
> terjadi. Organisme tidak punya sistem untuk mengembangkan nukleotida
> 1-methyl-3'-pseudoridylyl. Virus bergantung pada sistem organisme untuk me-
> reproduksi diri mereka sendiri, dan fasilitas ini tidak tersedia secara alami.
> Vaksin mRNA meluruh cepat di dalam tubuh, dan tidak ada kemungkinan RNA ber-Ψ
> mereplikasi dengan Ψ yang masih utuh. "[No, Really, mRNA Vaccines Are Not Going To Affect Your
> DNA](https://www.deplatformdisease.com/blog/no-really-mrna-vaccines-are-not-going-to-affect-your-dna)" juga merupakan bahan bacaan bagus.

Oke, kembali ke UTR 5'. Apa fungsi 51 karakter ini? Sebagaimana segalanya pada organisme, hampir tidak ada yang memiliki satu fungsi persis.

Ketika sel kita perlu *mentranslasi* RNA ke bentuk protein, ini dilakukan oleh ribosom. Ribosom berfungsi seperti printer 3D bagi protein. Ia menelan seuntai RNA dan berdasarkan untaian itu mengeluarkan string asam amino, yang kemudian melipat menjadi sebuah protein.

<center>
<img src="images/Protein_translation.gif">
           
Sumber: Pengguna Wikipedia [Bensaccount](https://en.wikipedia.org/wiki/User:Bensaccount)
</center>

Inilah yang terjadi, sebagaimana yang digambarkan pada animasi di atas. Pita hitam di bawah adalah RNA. Pita yang muncul pada bidang hijau adalah protein yang dibentuk. Bidang-bidang melayang keluar-masuk adalah asam amino dengan adaptor untuk menyesuaikan asam tersebut pada RNA.

Ribosom ini perlu menempel pada untai RNA secara fisik agar dapat berfungsi. Sekali menempel, ia akan mulai membentuk protein berdasarkan RNA yang ditelannya kemudian. Dari sinilah, bisa dibayangkan bahwa ia belum membaca bagian yang "diduduki" ribosom ini. Ini hanyalah salah satu fungsi UTR: sebagai zona landasan ribosom. UTR menyediakan aliran masuk bagi ribosom.

Di samping itu, UTR juga menyimpan metadata: kapankah translasi terjadi? Dan berapa banyak? Untuk vaksin, mereka memilah UTR paling segera yang dapat mereka temui, diambil dari [gen alfa globin](https://www.tandfonline.com/doi/full/10.1080/15476286.2018.1450054). Gen ini diketahui memproduksi protein dengan kuat. Di masa lampau, para ilmuwan sudah menemukan cara mengoptimalkan UTR ini lebih jauh (berdasarkan dokumen WHO di atas), jadi ini bukanlah UTR alfa globin. Ia lebih baik.

Peptida sinyal glikoprotein S
---------------------------------
Sebagaimana yang dituliskan, tujuan vaksin ini adalah merangsang sel untuk menghasilkan jumlah besar protein spike SARS-CoV-2. Hingga sejauh ini, kita telah menemui metadata dan "konvensi panggilan" pada kode sumber vaksin. Namun sekarang kita memasuki daerah protein virus yang sebenarnya.

Namun, kita masih memiliki satu lapis metadata. Begitu ribosom (dari animasi di atas) telah membuat sebuah protein, protein tersebut masih harus pergi ke suatu tempat. Ini dikodekan pada "peptida sinyal glikoprotein S (urutan pimpinan yang diperpanjang)".

Cara melihat ini adalah pada awalan protein terdapat semacam label alamat - dikodekan sebagai bagian dari protein itu sendiri. Pada kasus ini tertentu, peptida sinyal mengatakan bahwa protein ini harus keluar dari sel melalui "retikulum endoplasma". Bahkan keanehannya melampaui Star Trek!

"Peptida sinyal" ini tidak begitu panjang, namun jika kita periksa kodenya, ada perbedaan antara RNA virus dan RNA vaksin:

(Catat bahwa untuk perbandingan, saya telah mengganti modifikasi Ψ dengan RNA reguler U)

```
           3   3   3   3   3   3   3   3   3   3   3   3   3   3   3   3
Virus:   AUG UUU GUU UUU CUU GUU UUA UUG CCA CUA GUC UCU AGU CAG UGU GUU
Vaksin:  AUG UUC GUG UUC CUG GUG CUG CUG CCU CUG GUG UCC AGC CAG UGU GUU
               !   !   !   !   ! ! ! !     !   !   !   !   !            
```

Apa yang terjadi sebenarnya? Bukan tanpa sengaja saya mencantumkan RNA dalam 3 huruf berkelompok masing-masing. Tiga karakter RNA membentuk satu kodon. Dan tiap kodon mengkodekan satu asam amino tertentu. Peptida sinyal di dalam vaksin ini mengandung jumlah asam amino *sama persis* dengan pada virus itu sendiri.

Jadi bagaimana bisa RNA-nya berbeda?

Ada 4³=64 kodon berbeda, karena ada 4 karakter RNA, dan tiap kodon memiliki tiga dari karakter tersebut. Namun hanya ada 20 asam amino berbeda. Ini berarti kodon ganda mengkode asam amino yang sama.

Organisme menggunakan tabel hampir universal berikut untuk memetakan kodon RNA ke asam amino:

<center>
<img src="https://berthub.eu/articles/rna-codon-table.png">
           
[Tabel kodon RNA](https://en.wikipedia.org/wiki/DNA_and_RNA_codon_tables) (Wikipedia)
</center>

Pada tabel ini, kita dapat melihat bahwa modifikasi pada vaksin (UUU -> UUC) adalah semuanya *identik*. Kode RNA vaksin ini berbeda, namun menghasilkan asam amino dan protein yang sama.

Jika kita perhatikan seksama, kita bisa melihat bahwa sebagian besar perubahan tersebut terjadi pada posisi kodon ketiga, ditandai dengan angka 3 di atas. Dan jika kita memeriksa tabel kodon universal di atas, kita bisa melihat bahwa posisi ketiga ini seringkali tidak penting dalam jenis asam amino apa yang dihasilkan.

Sehingga, perubahan-perubahannya identik, namun mengapa mereka ada di sana? Dilihat dari dekat, kita bisa melihat bahwa semua perubahan *kecuali satu* mengarah pada lebih banyak C dan G.

Jadi mengapa begitu? Seperti yang ditulis sebelumnya, sistem imun kita tidak ramah terhadap RNA "eksogen", yaitu kode RNA yang berasal dari luar sel. Untuk menghindari deteksi, U pada RNA sudah digantikan oleh Ψ.

Namun, ternyata RNA dengan jumlah G dan C [yang lebih banyak](https://www.nature.com/articles/nrd.2017.243) juga [dikonversikan ke dalam protein secara lebih efisien](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC1463026/), 

Dan ini dimungkinkan dalam RNA vaksin dengan mengganti banyak karakter menjadi G dan C pada tempat yang memungkinkan. 

> I'm slightly fascinated by the *one* change that did not lead to an
> additional C or G, the CCA -> CCU modification. If anyone knows the reason,
> please let me know! Note that I'm aware that some codons are more common
> than others in the human genome, but [I also read that this does not
> influence translation speed a
> lot](https://journals.plos.org/plosgenetics/article?id=10.1371/journal.pgen.1006024).

> Saya sedikit tertarik pada *satu* perubahan yang tidak mengarah pada
> C atau G tambahan, modifikasi CCA -> CCU. Jika ada yang tahu alasannya,
> beritahukan saya! Catat bahwa saya tahu bahwa beberapa kodon lebih umum
> daripada yang lainnya pada genom manusia, namun [saya juga membaca bahwa
> ini tidak mempengaruhi banyak kecepatan translasi](https://journals.plos.org/plosgenetics/article?id=10.1371/journal.pgen.1006024).

Protein spike yang sesungguhnya
------------------------
3777 karakter selanjutnya dari RNA vaksin ini juga "dioptimisasi" kodonnya untuk menambahkan banyak C dan G. Agar tidak terlalu panjang saya tidak menuliskan seluruh kodenya, namun kita akan menyimak satu bagian khusus. Inilah bagian yang membuatnya berfungsi, bagian yang akan benar-benar menolong kita kembali ke kehidupan normal:

```
                  *   *
          L   D   K   V   E   A   E   V   Q   I   D   R   L   I   T   G
Virus:   CUU GAC AAA GUU GAG GCU GAA GUG CAA AUU GAU AGG UUG AUC ACA GGC
Vaksin:  CUG GAC CCU CCU GAG GCC GAG GUG CAG AUC GAC AGA CUG AUC ACA GGC
          L   D   P   P   E   A   E   V   Q   I   D   R   L   I   T   G
           !     !!! !!        !   !       !   !   !   ! !              
```

Di sini, kita melihat perubahan RNA umumnya yang identik. Contohnya, pada kodon pertama kita bisa melihat bahwa CUU diubah menjadi CUG. Ini menambahkan G lain ke dalam vaksin, yang kita ketahui membantu meningkatkan produksi protein. Baik CUU maupun CUG mengkodekan asam amino L atau Leusin, jadi tidak ada yang berubah di dalam protein tersebut.

Jika kita membandingkan protein spike di dalam vaksin, semua perubahannya identik seperti ini... kecuali dua, dan inilah yang kita lihat di atas.

Kodon ketiga dan keempat di atas mewakili perubahan aktual. Asam amino K dan V di situ diganti menjadi P atau Prolin. Untuk K, ini membutuhkan tiga perubahan ("!!!") dan untuk V ini membutuhkan hanya dua ("!!").

**Ternyata kedua perubahan ini sangat meningkatkan efisiensi vaksin**.

Apa yang terjadi kali ini? Jika kita melihat partikel SARS-CoV-2 yang asli, kita dapat melihat bahwa protein spike ini, tentu saja, memiliki banyak duri:

<center>
<img src="https://berthub.eu/articles/sars-em.jpg" width="420" height="280">

[Partikel virus SARS](https://id.wikipedia.org/wiki/Koronavirus_sindrom_pernapasan_akut_berat) (Wikipedia)
</center>

Duri-duri tersebut terpasang pada tubuh virus (protein nukleokapsid tersebut). Namun masalahnya, vaksin ini hanya menciptakan duri-duri tersebut, dan mereka tidak terpasang pada tubuh virus apapun.

Ternyata, tanpa modifikasi, protein spike yang berdiri bebas runtuh ke dalam struktur berbeda. Jika disuntikkan sebagai vaksin, ini tentu saja akan menyebabkan tubuh untuk mengembangkan imunitas... namun hanya untuk melawan protein spike yang runtuh tersebut.

Dan SARS-CoV-2 yang sesungguhnya muncul dengan spike yang berduri tersebut. Vaksin ini tidak akan berjalan begitu mulus jika terjadi.

Jadi apa yang harus dilakukan? Pada tahun [2017 dijelaskan bagaimana meletakkan substitusi prolin ganda pada tempat yang tepat](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5584442/) akan menyebabkan protein SARS-CoV-1 dan protein S MERS mengambil pengaturan pra-fusi mereka, tanpa menjadi bagian dari keseluruhan virus. Ini terjadi karena prolin adalah asam amino yang sangat kaku. Ia berfungsi sebagai semacam belat, menstabilisasi protein dalam kondisi yang diperlukan untuk diberikan kepada sistem imun tubuh.

[Mereka](https://twitter.com/goodwish916) yang [menemukan](https://twitter.com/KizzyPhD) ini sudah selayaknya mendapatkan penghargaan. Mereka boleh saja menyombongkan diri mereka. [Dan itu semua memang sudah sepantasnya begitu](https://twitter.com/McLellan_Lab/status/1291077489566142464).

> Tambahan! Saya baru saja dikontak [laboratorium McLellan](https://twitter.com/McLellan_Lab/status/1291077489566142464)
> , salah satu kelompok di balik penemuan prolin ini. Mereka berkata bahwa
> mereka tak bisa bergembira terlebih dahulu karena pandemi yang ada, na-
> mun mereka senang telah berjasa dalam produksi vaksin ini. Mereka juga
> menekankan pentingnya kelompok, pekerja dan sukarelawan lainnya.

Akhir dari protein, langkah lanjutan
----------------------------------
-Jika kita mencari-cari lebih jauh sumber kodenya, kita dapat menemukan modifikasi kecil pada akhir protein spike:

```
          V   L   K   G   V   K   L   H   Y   T   s             
Virus:   GUG CUC AAA GGA GUC AAA UUA CAU UAC ACA UAA
Vaksin:  GUG CUG AAG GGC GUG AAA CUG CAC UAC ACA UGA UGA 
          V   L   K   G   V   K   L   H   Y   T   s   s          
               !   !   !   !     ! !   !          ! 
```

Pada akhiran protein kita menemukan sebuah kodon "stop", ditandai dengan huruf s kecil. Ini adalah cara "sopan" untuk memberitahukan bahwa inilah ujung akhir protein. Virus aslinya menggunakan kodon stop UAA, dan sebagai perbandingan, vaksin ini menggunakan dua kodon stop UGA.

Ujung 3' yang tak tertranslasi
--------------------------
Sebagaimana halnya ribosom membutuhkan jalan-masuk pada akhir ujung 5', di mana kita menemukan "ujung five-prime yang tak tertranslasi", pada akhir ujung kode protein kita menemukan konstruksi serupa yang bernama 3' UTR.

Banyak yang bisa dituliskan mengenai 3' UTR ini, namun berdasarkan [penjelasan Wikipedia](https://en.wikipedia.org/wiki/Three_prime_untranslated_region): "Bidang 3' yang tidak tertranslasi memainkan peran penting dalam ekspresi gen dengan mempengaruhi lokalisasi, stabilitas, ekspor, dan efisiensi translasi dari sebuah mRNA ... **bahkan dengan pemahaman kita terkait 3' UTR sekarang ini, mereka masih merupakan misteri relatif**".

Yang kita ketahui adalah 3' UTR tertentu sangat berhail mempromosikan ekspresi protein. Berdasarkan dokumen WHO di atas, 3' UTR dari vaksin BioNTech/Pfizer ini diambil dari "penguat amino-terminal dari mRNA split (AES, amino-terminal enhancer of split) dan RNA ribosomal 12S mitokondrial untuk memberikan stabilitas RNA dan ekspresi proten total yang tinggi". Untuk itu saya ucapkan, kerja bagus.

<center>
<img src="https://berthub.eu/articles/vaccine.jpg">
</center>


AAAAAAAAAAAAAAAAAAAAAA-Akhir dari ini semua
----------------------------------------
Ujung akhir mRNA ini terpoliadenilasi. Ini hanya bentuk unik untuk mengatakan bahwa ia berakhiran dengan banyak AAAAAAAAAAAAAAAAAAA. Bahkan mRNA tampaknya juga sudah kenyang dengan tahun 2020.

mRNA bisa digunakan berulang kali, namun seiring waktu, ia juga kehilangan banyak A pada akhirnya. Begitu semua A habis, mRNA ini tak lagi berfungsi dan dibuang. Dengan begini, ekor poli-A adalah perlindungan dari penurunan demikian.

Penelitian telah dilakukan untuk mencari tahu apa jumlah optimal dari A pada akhiran ini untuk vaksin mRNA. Saya membaca pada literatur terbuka bahwa jumlahnya mencapai 120 atau lebih.

Vaksin BNT162b2 berakhiran dengan:

```
                                     ****** ****
UAGCAAAAAA AAAAAAAAAA AAAAAAAAAA AAAAGCAUAU GACUAAAAAA AAAAAAAAAA 
AAAAAAAAAA AAAAAAAAAA AAAAAAAAAA AAAAAAAAAA AAAAAAAAAA AAAA
```

Ini adalah 30 A, kemudian sebuah "penghubung 10 nukleotida" (GCAUAUGACU), diikuti 70 A lainnya.

Saya mencurigai bahwa apa yang kita lihat di sini adalah hasil dari optimisasi lebih jauh dari proprietor untuk meningkatkan ekspresi protein lebih jauh.

Ringkasan
-----------
Dengan ini, kita sekarang tahu isi mRNA persis dari vaksin BNT162b2, dan secara garis besar kita mengerti mengapa mereka ada:

 * "Topi" untuk memastikan RNA terlihat seperti mRNA biasa
 * Ujung 5' tak tertranslasi (UTR) yang sukses dan teroptimalisasi
 * Peptida sinyal dengan kodon teroptimisasi untuk mengirimkan protein spike ke tempat yang tepat (diduplikasikan 100% dari virus asli)
 * Versi kodon teroptimisasi dari spike asli, dengan dua substitusi kodon untuk memastikan protein muncul dalam bentuk tepat
 * Ujung 3' tak tertranslasi yang sukses dan teroptimalisasi
 * Ekor poli-A yang misterius dengan "penghubung" yang tak bisa dijelaskan

Optimalisasi kodon ini menambahkan banyak G dan C ke dalam mRNA. Sementara itu, menggunakan Ψ (1-methyl-3'-pseudoridylyl) sebagai pengganti U membantu menghindari sistem imun kita, sehingga mRNA dapat bertempat cukup lama sehingga kita dapat melatih sistem imun kita.

Referensi lebih jauh
-----------------------
Pada tahun 2017 saya menggelar presentasi dua jam mengenai DNA, yang bisa dilihat [di sini](https://berthub.eu/dna). Sebagaimana artikel ini, presentasi ini dirancang untuk mereka yang berkutat di ilmu komputer.

Di samping itu, saya sudah lama membuka halaman tentang "[DNA untuk programmer](https://berthub.eu/amazing-dna)" sejak tahun 2001.

Anda mungkin juga dapat menikmati [perkenalan pada sistem imun kita yang menakjubkan](https://berthub.eu/articles/posts/immune-system/).

Akhir kata, [daftar artikel blog saya ini](https://berthub.eu/articles) juga banyak yang membahas DNA, SARS-CoV-2, dan COVID.
