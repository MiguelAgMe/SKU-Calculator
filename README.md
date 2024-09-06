<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Camera SKU Calculator</title>
</head>
<body>

<h1>Camera Setup SKU Calculator</h1>

<form id="cameraCalculator">
  <label for="cameraType">Select Camera Type:</label>
  <select id="cameraType">
    <option value="dashcam">Dashcam</option>
    <option value="multi-channel">Multi-Channel Camera</option>
  </select>

  <label for="channels">Number of Channels:</label>
  <select id="channels">
    <option value="1">1 Channel</option>
    <option value="2">2 Channels</option>
    <option value="3">3 Channels</option>
  </select>

  <label for="wireLength">Wire Length (meters):</label>
  <input type="number" id="wireLength" placeholder="Enter length in meters">

  <label for="licensePlan">License Plan:</label>
  <select id="licensePlan">
    <option value="basic">Basic</option>
    <option value="pro">Pro</option>
  </select>

  <label for="dataPlan">Data Plan:</label>
  <select id="dataPlan">
    <option value="5GB">5GB</option>
    <option value="10GB">10GB</option>
  </select>

  <button type="button" onclick="calculateSKU()">Calculate</button>
</form>

<p id="result"></p>

<script>
function calculateSKU() {
  const cameraType = document.getElementById("cameraType").value;
  const channels = document.getElementById("channels").value;
  const wireLength = document.getElementById("wireLength").value;
  const licensePlan = document.getElementById("licensePlan").value;
  const dataPlan = document.getElementById("dataPlan").value;

  // Example logic to map selections to SKUs
  let skus = `Camera Type: ${cameraType}\nChannels: ${channels}\nWire Length: ${wireLength} meters\nLicense Plan: ${licensePlan}\nData Plan: ${dataPlan}\n`;

  // Map this to specific SKUs
  let skuOutput = `SKU123-${cameraType}-${channels}-${licensePlan}-${dataPlan}`;

  document.getElementById("result").innerText = `Recommended SKU: ${skuOutput}`;
}
</script>

</body>
</html>
