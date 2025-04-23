<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JavaScript & DOM (Document Object Model)</title>
    <style>
        body { font-family: Arial, sans-serif; margin: 20px; padding: 0; }
        h1 { color: #2980b9; }
        .box { width: 100px; height: 100px; background-color: #3498db; margin: 10px; }
        button { padding: 10px 20px; border: none; background-color: #2ecc71; color: white; cursor: pointer; }
    </style>
</head>
<body>
    <h1>JavaScript & DOM (Document Object Model)</h1>
    <p>Contoh manipulasi DOM dengan JavaScript:</p>
    <div class="box" id="colorBox"></div>
    <button onclick="changeColor()">Ubah Warna</button>

    <script>
        // Seleksi elemen DOM dan event handling
        function changeColor() {
            const box = document.getElementById('colorBox');
            box.style.backgroundColor = box.style.backgroundColor === 'tomato' ? '#3498db' : 'tomato';
        }
    </script>
</body>
</html>
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Manipulasi HTML + CSS dengan JavaScript</title>
    <style>
        body { font-family: Arial, sans-serif; padding: 20px; }
        #dynamicContent { padding: 10px; border: 1px solid #ddd; margin: 10px 0; }
        .highlight { color: white; background-color: #2980b9; padding: 5px; border-radius: 4px; }
        .hidden { display: none; }
        .animate { transition: all 0.3s ease; transform: scale(1.1); }
    </style>
</head>
<body>
    <h1>Manipulasi HTML + CSS dengan JavaScript</h1>

    <button onclick="changeContent()">Ubah Konten</button>
    <button onclick="toggleVisibility()">Tampilkan/Sembunyikan</button>
    <button onclick="addAnimation()">Animasi Efek</button>

    <div id="dynamicContent">Konten ini akan diubah secara dinamis.</div>

    <form onsubmit="validateForm(event)">
        <label for="name">Nama:</label>
        <input type="text" id="name" name="name" required>
        <button type="submit">Kirim</button>
    </form>

    <script>
        function changeContent() {
            const content = document.getElementById('dynamicContent');
            content.innerHTML = 'Konten telah diperbarui!';
            content.classList.toggle('highlight');
        }

        function toggleVisibility() {
            const content = document.getElementById('dynamicContent');
            content.classList.toggle('hidden');
        }

        function addAnimation() {
            const content = document.getElementById('dynamicContent');
            content.classList.toggle('animate');
        }

        function validateForm(event) {
            event.preventDefault();
            const name = document.getElementById('name').value;
            if (name.trim() === '') {
                alert('Nama tidak boleh kosong!');
            } else {
                alert('Formulir berhasil dikirim!');
            }
        }
    </script>

</body>
</html>
