# Tugas-1-Pemrograman-Internet-membuat-input-nilai-mahasiswa-dengan-php-dan-html-css-

<?php
     if (isset($_GET['submit'])){
        $nilaitugas = $_GET['nilaitugas'];
        $nilaiuts = $_GET['nilaiuts'];
        $nilaiuas = $_GET['nilaiuas'];

        $nilaiakhir = ($nilaitugas + $nilaiuts + $nilaiuas)/3;
            
        if($nilaiakhir>80)
            $predikat="A";
        else if($nilaiakhir>=80)
            $predikat="B+";
        else if($nilaiakhir>71)
            $predikat="B";
        else if ($nilaiakhir>65)
            $predikat="C+";
        else if($nilaiakhir>60)
            $predikat="C";
        else if($nilaiakhir>55)
            $preddikat="D";
        else
            $predikat="E";
    }
    
?>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <link rel="stylesheet" href="Tugas 1.css">

    <title>Membuat Nilai</title>
</head>
<body>
    <h1 class = "judul" Align = "Center" style="font-size: 200%;">
    Penilaian Mahasiswa Matakuliah Pemrograman Internet
    </h1>

    <div class="container">
        <form action="Tugas.php" method="get">
            <label for = "nama">Nama Lengkap </label>
            <input type="text" id = "nama" name = "nama" value = <?php if(isset($_GET['submit'])){echo $_GET['nama'];} ?>>

            <br>

            <label for = "nim">Nim </label>
            <input type="text" id = "nim" name = "nim" value = <?php if(isset($_GET['submit'])){echo $_GET['nim'];} ?>>

            <br>
             
            <div class="form-group">
            <label for = "nilaitugas">Nilai Tugas </label>
            <input type="text" id = "nilaitugas" name = "nilaitugas" value = <?php if(isset($_GET['submit'])){echo $_GET['nilaitugas'];} ?>>
            
            <br>

            <label for = "nilaiuts">Nilai UTS </label>
            <input type="text" id = "nilaiuts" name = "nilaiuts" value = <?php if(isset($_GET['submit'])){echo $_GET['nilaiuts'];} ?>>

            <br>

            <label for = "nilaiuas">Nilai UAS </label>
            <input type="text" id = "nilaiuas" name = "nilaiuas" value = <?php if(isset($_GET['submit'])){echo $_GET['nilaiuas'];} ?>>

            <br>

            <label for = "nilaiakhir">Nilai Akhir </label>
            <input type="text" id = "nilaiakhir" name = "nilaiakhir" value = <?php if(isset($nilaiakhir))echo$nilaiakhir?>>

            <br>

            <label for = "predikat">Predikat </label>
            <input type="text" id = "predikat" name = "predikat" value = <?php if(isset($predikat))echo $predikat?>>

            
            <div class="submit">
            <button type="submit" name="submit">Click</button>
            </div>
        </form>

    </div>
    
    </body>
</html>
