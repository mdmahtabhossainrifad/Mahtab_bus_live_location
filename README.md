<!DOCTYPE html>
<html lang="bn">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>Mahtab Bus Live</title>

  <link
    rel="stylesheet"
    href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css"
  />

  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #f5f5f5;
    }

    .header {
      background: #111827;
      color: white;
      padding: 15px;
      text-align: center;
    }

    .header h2 {
      margin: 0;
    }

    .header p {
      margin: 5px 0 0;
      font-size: 13px;
    }

    #map {
      height: calc(100vh - 86px);
      width: 100%;
    }
  </style>
</head>

<body>

  <div class="header">
    <h2>🚌 Mahtab Bus Live</h2>
    <p>Live Bus Tracking Map</p>
  </div>

  <div id="map"></div>

  <script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"></script>

  <script>
    const map = L.map("map").setView([23.65, 90.60], 12);

    L.tileLayer(
      "https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png",
      {
        maxZoom: 19,
        attribution: "© OpenStreetMap contributors"
      }
    ).addTo(map);

    L.marker([23.65, 90.60])
      .addTo(map)
      .bindPopup("<b>Mahtab Bus Live</b><br>Map is ready!")
      .openPopup();
  </script>

</body>
</html>
