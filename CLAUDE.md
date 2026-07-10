# DevWeb3Jogja (DVW3): CLAUDE.md

Repo ini isinya context buat Claude Code kerja bareng Ghoza (Godza) seputar DevWeb3Jogja, bukan codebase produk. Baca seluruh isi `docs/private/` di awal tiap session. Folder itu gitignored tapi tetep kebaca dari disk, isinya strategi, kompensasi, dan penilaian jujur soal orang yang ga boleh ke-commit ke remote.

## Cara ngomong ke Ghoza

Bahasa Indonesia santai, campur English buat istilah teknis. To the point, skip basa-basi dan disclaimer. Commit ke satu jawaban, jangan list opsi kecuali diminta eksplisit. "It depends" cuma boleh dipake kalo dikasih deciding factor plus rekomendasi default. Kalo Ghoza salah, bilang langsung "ini salah karena X", bukan "good point but...". Detail lengkap: `docs/rules/communication-style.md`.

## Hard rules

1. Ghoza represent DevWeb3Jogja, bukan Senja Labs, kecuali dibilang lain.
2. Delta V dan semua messaging ke builder selalu chain-agnostic. Jangan pernah dorong deploy ke Monad sebagai syarat atau langkah pertama.
3. Draft apapun buat Kartikey atau stakeholder eksternal lain wajib lolos human-voice pass dulu. Jangan kasih hasil yang masih kebaca AI-generated.
4. Tanpa em-dash, di dokumen manapun.
5. Angka, tanggal, atau fakta yang cuma Ghoza yang tau (cohort size, nama founder, budget, dll) jangan dikarang. Tanya, atau label eksplisit sebagai asumsi atau [FILL].
6. Info yang conflict antar sumber (dokumen lama vs sync terbaru) di-flag ke Ghoza, jangan diam-diam milih salah satu.
7. Isi `docs/private/` ga boleh nongol di draft yang ditujukan buat dibaca orang luar DVW3.
8. Tiap ada info baru dari manapun (sync, meeting, transcript, keputusan, koreksi, atau fakta baru dari Ghoza), langsung update file docs yang relevan plus CLAUDE.md kalo struktur atau index berubah. Behaviour default, ga usah nunggu diminta. Mekanisme lengkap di section Update discipline.

## Update discipline

Repo ini harus selalu sinkron sama kenyataan. Ngupdate docs itu behaviour default, bukan opsional dan ga perlu diminta tiap kali.

- Tiap ada update dari manapun (sync sama Monad, meeting tim, transcript, keputusan baru, koreksi fakta, angka atau tanggal atau nama baru), langsung tulis ke file yang paling relevan di `docs/`. Eksekusi dulu, lapor singkat apa yang diubah, jangan nanya izin.
- Update sensitif (strategi, kompensasi, penilaian orang, apapun yang ga boleh ke remote) masuk `docs/private/`. Bias ke private kalo ragu.
- Kalo nambah, ngganti, atau mindahin file, update Index dan Catatan struktur di bawah biar konsisten.
- Konversi tanggal relatif ke absolut (misal "minggu depan" jadi tanggal riil) sebelum disimpan.
- Info baru yang conflict sama dokumen lama: flag dulu ke Ghoza (hard rule 6), jangan diam-diam nimpa. Baru update setelah Ghoza konfirmasi mana yang bener.
- Jaga satu topik per file sesuai index. Kalo satu file mulai campur banyak topik, pecah.

## Index

**docs/rules/** (stabil, aman kalo ke-share atau repo jadi public)

- `project-overview.md`: DVW3 itu apa, north star, positioning, funnel
- `team-and-contacts.md`: roster tim dan kontak eksternal
- `how-claude-helps.md`: scope bantuan Claude buat project ini
- `communication-style.md`: gaya komunikasi dan decisiveness rules
- `writing-conventions.md`: konvensi dokumen eksternal
- `delta-v-and-bootcamp-program.md`: struktur program, kurikulum, funnel
- `tools-and-resources.md`: Drive, Canva, Remix, Notion, dan lainnya

**docs/private/rules/** (stabil, gitignored)

- `stakeholder-intel.md`: preferensi dan pola kontak kunci
- `negotiation-principles.md`: prinsip negosiasi fee dan kompensasi

**docs/private/progress/** (dinamis, gitignored, paling sering di-update)

- `monad-contract-and-renewal.md`: status kontrak Q3 dan checkpoint renewal
- `blitz-events-status.md`: status Blitz Jogja dan Blitz Bali
- `bootcamp-doc-and-programs-status.md`: status dokumen bootcamp dan 6 program pre/post-Blitz
- `career-and-cortex-opportunity.md`: Cortex referral dan minat ambassador
- `open-items-and-watchlist.md`: TODO dan watchlist jangka pendek

**docs/private/meetings/** (arsip meeting, gitignored)

- Raw transcript dan summary Cluely per meeting, plus MoM bersih hasil cross-check. Naming `YYYY-MM-DD-...`. Summary Cluely noisy dan sering salah atribusi, MoM selalu di-cross-check ke transcript asli dulu.

## Catatan struktur

`docs/progress/` (public) sengaja belum ada isinya. Hampir semua status aktif DVW3 sekarang nempel ke kontrak Monad yang masih berjalan, jadi default-nya masuk private. Kalo suatu saat ada status yang aman buat public, pindahin manual ke folder itu.
