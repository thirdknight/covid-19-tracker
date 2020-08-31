<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=C">
  <link rel="stylesheet" href="./styles.css">
  <title>COVID 19</title>
</head> 
<body>
   <div id="root">
    <header>
      <h1>CORONAVIRUS TRACKER</h1>
      <h3>Confirmed Cases and Deaths by Country, Territory, or Conveyance</h3>
        <div class="content">    
          <p> <img src="./icons/icon-yellow.png">: > 100</p>
          <p> <img src="./icons/icon-blue.png">: 100 - 999</p>
          <p> <img src="./icons/icon-red.png">: > 1000</p>
        </div>
    </header>
    <main>
      <div id="map" class="map"> </div>
    </main>
  </div>
<!-- Chanbe the API googlemaps -->
<script src="https://maps.googleapis.com/maps/api/js?key=AIzaSyC92D4UvNjgeeLLWqXLcXzqHWoR5zdvBAo"></script>
<script>
  // Variables
  let yellowIcon = document.createElement("img");
  yellowIcon.src = './icons/icon-yellow.png';
  let blueIcon = document.createElement("img");
  blueIcon.src = './icons/icon-blue.png';
  let redIcon = document.createElement("img");
  redIcon.src = './icons/icon-red.png';

  const $map = document.querySelector('#map');
  const map = new window.google.maps.Map($map, {
    center: {
      lat: 0,
      lng: 0,
    },
    zoom: 3,
    minZoom: 2,
    maxZoom: 7,
    gestureHandling: "greedy"
  })
  renderData()
  
  async function getData() {
    const response = await fetch('https://wuhan-coronavirus-api.laeyoung.endpoint.ainize.ai/jhu-edu/latest');
    const data = await response.json()
    // console.log(data);
    return data
  }

  const popup = new window.google.maps.InfoWindow()

  function renderExtraData({ confirmed, deaths, recovered, provincestate, countryregion}) {
    return `
      <div>
        <p><strong> ${provincestate} - ${countryregion}</strong></p>
        <p>confirmed: ${ confirmed.toLocaleString() }</p>
        <p>deaths: ${deaths}</p>
        <p>recovered: ${recovered}</p>
      </div>  
    `
  }

  async function renderData() {
    const data = await getData(); 
    data.forEach(item => {
      const marker = new window.google.maps.Marker({
        position: {
          lat: item.location.lat,
          lng: item.location.lng
        },
        map,
        icon: ''
      });
      if(item.confirmed === 0 || item.confirmed === undefined) {  
        marker.setMap(null);
      }  
      if(item.confirmed > 0) {
        marker.icon = yellowIcon.src;
      }
      if(item.confirmed > 100) {
        marker.icon = blueIcon.src;
      }
      if(item.confirmed > 1000) {
        marker.icon = redIcon.src;
      }
      marker.addListener('click', () => {
        popup.setContent(renderExtraData(item));
        popup.open(map, marker) 
      });
    })
  }
</script>

</body>
</html>

