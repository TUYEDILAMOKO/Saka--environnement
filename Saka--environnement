<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>Mon site ESP32</title>
  <style>
    body { font-family: Arial; text-align: center; background-color: #f0f0f0; }
    h1 { color: #1a73e8; }
    p { font-size: 18px; color: #333; }
    #temperature { font-size: 24px; color: #e91e63; }
  </style>
</head>
<body>
  <h1>Données de mon ESP32</h1>
  <p>Température : <span id="temperature">--</span> °C</p>

  <script>
    async function fetchData() {
      try {
        const response = await fetch('https://api.jsonbin.io/b/TON_BIN_ID/latest'); // à remplacer plus tard
        const data = await response.json();
        document.getElementById('temperature').textContent = data.temperature;
      } catch (err) {
        console.log('Erreur:', err);
      }
    }
    setInterval(fetchData, 2000); // rafraîchit toutes les 2 sec
    fetchData(); // premier chargement
  </script>
</body>
</html>
