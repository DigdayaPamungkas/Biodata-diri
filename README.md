<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Biodata Mahasiswa</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        :root {
            --primary: #2563eb;
            --secondary: #60a5fa;
            --accent: #dbeafe;
            --text: #1e293b;
            --bg: #f8fafc;
        }

        body {
            background-color: var(--bg);
            color: var(--text);
            line-height: 1.6;
        }

        .container {
            max-width: 800px;
            margin: 40px auto;
            padding: 0 20px;
        }

        .profile-card {
            background: white;
            border-radius: 16px;
            overflow: hidden;
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
        }

        .header {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            padding: 40px 20px;
            text-align: center;
            position: relative;
        }

        .header h1 {
            font-size: 1.8rem;
            margin-bottom: 10px;
        }

        .profile-image {
            width: 200px;
            height: 200px;
            border-radius: 100%;
            border: 4px solid white;
            margin: 0 auto 10px;
            display: block;
            transition: transform 0.3s ease;
            cursor: pointer;
        }

        .profile-image:hover {
            transform: scale(1.1);
        }

        .tab-container {
            background: white;
            padding: 15px;
            display: flex;
            justify-content: center;
            gap: 10px;
            border-bottom: 1px solid #e2e8f0;
        }

        .tab-button {
            padding: 10px 20px;
            border: none;
            background: none;
            color: var(--text);
            cursor: pointer;
            border-radius: 8px;
            transition: all 0.3s ease;
        }

        .tab-button:hover {
            background: var(--accent);
        }

        .tab-button.active {
            background: var(--primary);
            color: white;
        }

        .content {
            padding: 30px;
        }

        .tab-content {
            display: none;
        }

        .tab-content.active {
            display: block;
            animation: fadeIn 0.5s ease;
        }

        .info-group {
            margin-bottom: 20px;
        }

        .info-item {
            padding: 12px;
            margin-bottom: 10px;
            border-radius: 8px;
            background: var(--bg);
            display: flex;
            align-items: center;
            transition: transform 0.3s ease;
        }

        .info-item:hover {
            transform: translateX(10px);
            background: var(--accent);
        }

        .info-label {
            font-weight: 600;
            width: 140px;
            color: var(--primary);
        }

        .achievement {
            background: var(--bg);
            padding: 15px;
            border-radius: 8px;
            margin-bottom: 15px;
            transition: all 0.3s ease;
        }

        .achievement:hover {
            transform: translateY(-5px);
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
        }

        .achievement h3 {
            color: var(--primary);
            margin-bottom: 5px;
        }

        .semester-info {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 15px;
            margin-bottom: 20px;
        }

        .semester-card {
            background: var(--bg);
            padding: 15px;
            border-radius: 8px;
            text-align: center;
            transition: all 0.3s ease;
        }

        .semester-card:hover {
            transform: translateY(-5px);
            background: var(--accent);
        }

        .ipk {
            font-size: 1.5rem;
            font-weight: bold;
            color: var(--primary);
            margin-top: 5px;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(10px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @media (max-width: 600px) {
            .info-item {
                flex-direction: column;
                align-items: flex-start;
            }
            
            .info-label {
                width: 100%;
                margin-bottom: 5px;
            }

            .tab-container {
                flex-wrap: wrap;
            }

            .tab-button {
                width: calc(50% - 5px);
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="profile-card">
            <div class="header">
                <img src="Gambar WhatsApp 2024-11-11 pukul 16.31.04_0cdee289.jpg" alt="Profile" Profil" class="profile-image">
                <h1>Digdaya Pamungkas</h1>
                <p>Teknik Informatika - Angkatan 2023</p>
            </div>

            <div class="tab-container">
                <button class="tab-button active" onclick="showTab('pribadi')">Data Pribadi</button>
                <button class="tab-button" onclick="showTab('akademik')">Akademik</button>
                <button class="tab-button" onclick="showTab('prestasi')">Prestasi</button>
            </div>

            <div class="content">
                <div id="pribadi" class="tab-content active">
                    <div class="info-group">
                        <div class="info-item">
                            <div class="info-label">NIM</div>
                            <div>2310010402</div>
                        </div>
                        <div class="info-item">
                            <div class="info-label">Tempat Lahir</div>
                            <div>Banjarmasin</div>
                        </div>
                        <div class="info-item">
                            <div class="info-label">Tanggal Lahir</div>
                            <div>21 November 2005</div>
                        </div>
                        <div class="info-item">
                            <div class="info-label">Alamat</div>
                            <div>Jl. Tembus Mantuil Gg. Perintis</div>
                        </div>
                        <div class="info-item">
                            <div class="info-label">Email</div>
                            <div>digdayabjm223@gmail.com</div>
                        </div>
                    </div>
                </div>

                <div id="akademik" class="tab-content">
                    <div class="semester-info">
                        <div class="semester-card">
                            <h3>Semester 1</h3>
                            <div class="ipk">3.85</div>
                        </div>
                        <div class="semester-card">
                            <h3>Semester 2</h3>
                            <div class="ipk">3.70</div>
                        </div>
                        <div class="semester-card">
                            <h3>IPK</h3>
                            <div class="ipk">3.90</div>
                        </div>
                    </div>

                    <div class="info-group">
                        <div class="info-item">
                            <div class="info-label">Program Studi</div>
                            <div>Teknik Informatika</div>
                        </div>
                        <div class="info-item">
                            <div class="info-label">Fakultas</div>
                            <div>Fakultas Teknik</div>
                        </div>
                        <div class="info-item">
                            <div class="info-label">Dosen Pengajar</div>
                            <div>Yusup Indra Wijaya, S.kom., M.Kom.</div>
                        </div>
                    </div>
                </div>

                <div id="prestasi" class="tab-content">
                    <div class="achievement">
                        <h3>Sertifikat Operator Komputer Madya</h3>
                        <p>2023 - Pelatihan Kompetensi</p>
                    </div>
                    <div class="achievement">
                        <h3>Kompetensi Sains Nasionaly</h3>
                        <p>2021 - Tingkat Kota Banjarmasin</p>
                    </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        function showTab(tabId) {
            // Sembunyikan semua konten tab
            document.querySelectorAll('.tab-content').forEach(content => {
                content.classList.remove('active');
            });
            
            // Hapus kelas active dari semua tombol
            document.querySelectorAll('.tab-button').forEach(button => {
                button.classList.remove('active');
            });
            
            // Tampilkan konten tab yang dipilih
            document.getElementById(tabId).classList.add('active');
            
            // Tambah kelas active ke tombol yang diklik
            event.currentTarget.classList.add('active');
        }
    </script>
</body>
</html>