<!DOCTYPE html>
<html lang="sv">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tabell med 2300 rutor</title>
    <style>
        /* Styla hela tabellen */
        table {
            border-collapse: collapse;
            width: 100%;
        }

        /* Styla varje cell i tabellen */
        td {
            width: 1cm;
            height: 1cm;
            border: 1px solid black;
            text-align: center;
            vertical-align: middle;
        }
    </style>
</head>
<body>

    <table id="myTable"></table>

    <script>
        // Variabel för antalet rutor
        const totalCells = 2300;
        const rows = 50;  // Antal rader
        const cols = 46;  // Antal kolumner

        // Skapa tabellen
        function createTable() {
            let table = document.getElementById('myTable');
            
            let cellCount = 0;
            
            // Skapa rader och celler
            for (let i = 0; i < rows; i++) {
                let row = table.insertRow(i);
                
                for (let j = 0; j < cols; j++) {
                    let cell = row.insertCell(j);
                    cell.textContent = ++cellCount;
                }
            }
        }

        // Anropa funktionen för att skapa tabellen
        createTable();
    </script>
</body>
</html>
