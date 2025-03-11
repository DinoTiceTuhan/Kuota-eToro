# Kuota-eToro
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tabel Kuota Investasi</title>
    <style>
        /* Global Styles */
        body {
            font-family: 'Poppins', sans-serif;
            background: url('https://assets.onecompiler.app/43baft393/43bafrz9s/%E2%80%94Pngtree%E2%80%94abstract%20wallpaper%20with%20bitcoin%20intertwined_15835147.jpg') center/cover no-repeat fixed;
            color: white;
            text-align: center;
            margin: 0;
            padding: 0;
        }

        .dark-mode {
            background: #121212;
            color: white;
        }

        /* Toggle Button */
        .toggle-container {
            position: absolute;
            top: 20px;
            right: 20px;
        }

        .toggle-btn {
            padding: 10px;
            background: #32CD32;
            color: white;
            border: none;
            cursor: pointer;
            font-weight: bold;
            border-radius: 5px;
            transition: background 0.3s ease;
        }

        .toggle-btn:hover {
            background: #228B22;
        }

        /* Input Container */
        .input-container {
            margin-top: 30px;
            padding: 20px;
            background-color: rgba(0, 0, 0, 0.7);
            border-radius: 15px;
            box-shadow: 0px 0px 15px rgba(0, 255, 127, 0.7);
            display: flex;
            justify-content: space-between;
            max-width: 450px;
            margin: 30px auto;
        }

        .input-container > div {
            width: 45%;
        }

        .input-container label {
            font-size: 16px;
            font-weight: bold;
            margin-bottom: 5px;
        }

        .input-container input {
            padding: 10px;
            font-size: 16px;
            width: 75%;
            text-align: center;
            border-radius: 5px;
            border: none;
            background-color: rgba(255, 255, 255, 0.3);
            color: white;
        }

        /* Container */
        .table-container {
            width: 150%;
            max-width: 1000px;
            margin: 30px auto;
            background: rgba(0, 0, 0, 0.7);
            padding: 30px;
            border-radius: 30px;
            box-shadow: 0px 0px 15px rgba(0, 255, 127, 0.7);
            position: relative;
            overflow: hidden;
        }

        /* Table Styling */
        table {
            width: 100%;
            border-collapse: collapse;
            background: rgba(255, 255, 255, 0.2);
            color: white;
            border-radius: 10px;
            overflow: hidden;
            margin-top: 10px;
        }

        th, td {
            border: 1px solid rgba(255, 255, 255, 0.2);
            padding: 12px;
            text-align: center;
        }

        th {
            background-color: rgba(50, 205, 50, 0.9);
            color: white;
        }

        .status-tersedia {
            color: #32CD32;
            font-weight: bold;
        }

        .status-tidak-tersedia {
            color: #FF4500;
            font-weight: bold;
        }

        /* Etoro Image */
        .etoro-image-container {
            width: 80%;
            max-width: 600px;
            margin: 20px auto;
        }

        .etoro-image-container img {
            width: 100%;
            border-radius: 10px;
        }
    </style>
</head>
<body>

<div class="toggle-container">
    <button class="toggle-btn" onclick="toggleDarkMode()">Toggle Dark Mode</button>
</div>

<!-- Form Input Kuota & Jumlah Investasi -->
<div class="input-container">
    <div>
        <label for="kuota1">Kuota 1:</label>
        <input type="number" id="kuota1" value="3" min="0" max="10" onchange="updateStatus(1)">
        <label for="kuota2">Kuota 2:</label>
        <input type="number" id="kuota2" value="2" min="0" max="10" onchange="updateStatus(2)">
        <label for="kuota3">Kuota 3:</label>
        <input type="number" id="kuota3" value="0" min="0" max="10" onchange="updateStatus(3)">
        <label for="kuota4">Kuota 4:</label>
        <input type="number" id="kuota4" value="4" min="0" max="10" onchange="updateStatus(4)">
        <label for="kuota5">Kuota 5:</label>
        <input type="number" id="kuota5" value="0" min="0" max="10" onchange="updateStatus(5)">
    </div>

    <div>
        <label for="jumlah1">Jumlah Investasi 1:</label>
        <input type="number" id="jumlah1" class="investment-input" value="8000000" onchange="updateJumlahInvestasi(1)">
        <label for="jumlah2">Jumlah Investasi 2:</label>
        <input type="number" id="jumlah2" class="investment-input" value="30000000" onchange="updateJumlahInvestasi(2)">
        <label for="jumlah3">Jumlah Investasi 3:</label>
        <input type="number" id="jumlah3" class="investment-input" value="50000000" onchange="updateJumlahInvestasi(3)">
        <label for="jumlah4">Jumlah Investasi 4:</label>
        <input type="number" id="jumlah4" class="investment-input" value="80000000" onchange="updateJumlahInvestasi(4)">
        <label for="jumlah5">Jumlah Investasi 5:</label>
        <input type="number" id="jumlah5" class="investment-input" value="100000000" onchange="updateJumlahInvestasi(5)">
    </div>
</div>

<div class="table-container">
    <h2>Kuota Investasi Online Cryptocurrency</h2>
    
    <!-- Gambar eToro -->
    <div class="etoro-image-container">
        <img src="https://assets.onecompiler.app/43baft393/43bafrz9s/eToro-Slashes-Spread-To-Bump-Up-Market-Liquidity.jpg" alt="eToro Logo">
    </div>

    <table>
        <thead>
            <tr>
                <th>TANGGAL</th>
                <th>JUMLAH INVESTASI</th>
                <th>KUOTA</th>
                <th>STATUS</th>
                <th>KETERANGAN</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td id="tanggal1"></td>
                <td id="investasi1">Rp 8.000.000</td>
                <td id="kuota1-cell">3</td>
                <td id="status1" class="status-tersedia">✔</td>
                <td id="keterangan1" class="status-tersedia">TERSEDIA</td>
            </tr>
            <tr>
                <td id="tanggal2"></td>
                <td id="investasi2">Rp 30.000.000</td>
                <td id="kuota2-cell">2</td>
                <td id="status2" class="status-tersedia">✔</td>
                <td id="keterangan2" class="status-tersedia">TERSEDIA</td>
            </tr>
            <tr>
                <td id="tanggal3"></td>
                <td id="investasi3">Rp 50.000.000</td>
                <td id="kuota3-cell">0</td>
                <td id="status3" class="status-tidak-tersedia">✘</td>
                <td id="keterangan3" class="status-tidak-tersedia">TIDAK TERSEDIA</td>
            </tr>
            <tr>
                <td id="tanggal4"></td>
                <td id="investasi4">Rp 80.000.000</td>
                <td id="kuota4-cell">4</td>
                <td id="status4" class="status-tersedia">✔</td>
                <td id="keterangan4" class="status-tersedia">TERSEDIA</td>
            </tr>
            <tr>
                <td id="tanggal5"></td>
                <td id="investasi5">Rp 100.000.000</td>
                <td id="kuota5-cell">0</td>
                <td id="status5" class="status-tidak-tersedia">✘</td>
                <td id="keterangan5" class="status-tidak-tersedia">TIDAK TERSEDIA</td>
            </tr>
        </tbody>
    </table>
</div>

<script>
    function toggleDarkMode() {
        document.body.classList.toggle("dark-mode");
    }

    function updateStatus(row) {
        const kuota = document.getElementById(`kuota${row}`).value;
        const statusCell = document.getElementById(`status${row}`);
        const keteranganCell = document.getElementById(`keterangan${row}`);
        const kuotaCell = document.getElementById(`kuota${row}-cell`);

        if (kuota == 0) {
            statusCell.innerHTML = "✘";
            statusCell.className = "status-tidak-tersedia";
            keteranganCell.innerHTML = "TIDAK TERSEDIA";
            keteranganCell.className = "status-tidak-tersedia";
        } else if (kuota >= 1 && kuota <= 10) {
            statusCell.innerHTML = "✔";
            statusCell.className = "status-tersedia";
            keteranganCell.innerHTML = "TERSEDIA";
            keteranganCell.className = "status-tersedia";
        }

        kuotaCell.innerHTML = kuota;
    }

    function updateJumlahInvestasi(row) {
        const investasi = document.getElementById(`jumlah${row}`).value;
        const investasiCell = document.getElementById(`investasi${row}`);
        investasiCell.innerHTML = "Rp " + new Intl.NumberFormat().format(investasi);
    }

    // Set today's date in each row with the format DD-MM-YYYY
    const today = new Date();
    const formattedDate = today.getDate().toString().padStart(2, '0') + "-" + (today.getMonth() + 1).toString().padStart(2, '0') + "-" + today.getFullYear();
    document.getElementById("tanggal1").innerHTML = formattedDate;
    document.getElementById("tanggal2").innerHTML = formattedDate;
    document.getElementById("tanggal3").innerHTML = formattedDate;
    document.getElementById("tanggal4").innerHTML = formattedDate;
    document.getElementById("tanggal5").innerHTML = formattedDate;
</script>

</body>
</html>
