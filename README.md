# Baby-PortraitPromptGenerator<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Detailed Baby Portrait Prompt Generator</title>
<style>
  body { 
    box-sizing: border-box;
    font-family: 'Arial', sans-serif; 
    background: linear-gradient(135deg, #2f2335, #533b57); 
    color: #fff; 
    padding: 20px; 
    min-height: 100vh; 
    margin: 0; 
  }
  .brand-header {
    text-align: center;
    margin-bottom: 30px;
  }
  .brand-header h1 { 
    color: #ffadad; 
    font-size: 3rem; 
    text-shadow: 0 0 15px #ff6f91; 
    margin-bottom: 10px;
    font-weight: bold;
  }
  .brand-header h2 {
    color: #fff;
    font-size: 1.8rem;
    margin-bottom: 0;
    font-weight: normal;
  }
  .container { 
    max-width: 900px; 
    margin: auto; 
    background: rgba(0,0,0,0.85); 
    padding: 30px; 
    border-radius: 15px; 
    box-shadow: 0 0 40px #ff6f91, inset 0 0 25px rgba(255,111,145,0.15); 
    border: 2px solid rgba(255,111,145,0.5);
  }
  .form-group { 
    margin-bottom: 25px; 
  }
  label { 
    display: block; 
    margin-bottom: 8px; 
    font-weight: bold; 
    color: #ffadad; 
    font-size: 1.1rem;
  }
  select, textarea, button { 
    width: 100%; 
    padding: 14px; 
    border-radius: 10px; 
    border: 2px solid #6b4151; 
    font-size: 16px; 
    background: linear-gradient(145deg, #442d3e, #553849); 
    color: #fff; 
    transition: all 0.3s; 
    box-sizing: border-box;
  }
  select:focus, textarea:focus { 
    outline: none; 
    border-color: #ff6f91; 
    box-shadow: 0 0 15px rgba(255,111,145,0.6);
  }
  select[multiple] {
    height: 140px;
  }
  select option {
    padding: 8px;
    background: #463545;
    color: #fff;
  }
  select option:checked {
    background: #ff6f91;
    color: #240018;
  }
  textarea {
    height: 200px; 
    resize: vertical; 
    font-family: 'Courier New', Courier, monospace; 
    line-height: 1.5; 
    background: #3a2735; 
    border-color: #7a5062; 
    color: #f8d7da;
  }
  button {
    background: #ff6f91; 
    color: white; 
    font-weight: bold; 
    cursor: pointer; 
    margin-top: 20px; 
    font-size: 18px; 
    border: 2px solid #7a5062;
    text-transform: uppercase;
    letter-spacing: 1px;
  }
  button:hover {
    background: #ff4382;
  }
  .btn-group { 
    display: flex; 
    gap: 12px; 
    flex-wrap: wrap;
  }
  .copy-btn { 
    background: linear-gradient(145deg, #38d39f, #279170); 
    margin-top: 10px; 
    font-size: 16px;
  }
  .copy-btn:hover {
    background: linear-gradient(145deg, #63eeb9, #38d39f);
  }
  .instructions {
    background: rgba(255, 173, 173, 0.1);
    border: 2px solid rgba(255, 173, 173, 0.3);
    border-radius: 10px;
    padding: 20px;
    margin-bottom: 30px;
  }
  .instructions h3 {
    color: #ffadad;
    margin-top: 0;
    margin-bottom: 15px;
    font-size: 1.3rem;
  }
  .instructions ol {
    color: #fff;
    line-height: 1.6;
  }
  .instructions li {
    margin-bottom: 8px;
  }
  .instructions strong {
    color: #ffadad;
  }
  .prompt-output { 
    margin-top: 20px; 
    white-space: pre-wrap;
  }
  .thank-you {
    max-width: 900px;
    margin: 30px auto;
    background: rgba(255, 173, 173, 0.15);
    border: 2px solid rgba(255, 173, 173, 0.4);
    border-radius: 15px;
    padding: 25px;
    text-align: center;
  }
  .thank-you h3 {
    color: #ffadad;
    margin-top: 0;
    margin-bottom: 15px;
    font-size: 1.5rem;
    text-shadow: 0 0 10px #ff6f91;
  }
  .thank-you p {
    color: #fff;
    line-height: 1.6;
    margin-bottom: 10px;
  }
  .thank-you .signature {
    color: #ffadad;
    font-style: italic;
    margin-top: 15px;
    margin-bottom: 0;
  }
</style>
</head>
<body>
<div class="brand-header">
  <h1>🌟 House of Star Designs 🌟</h1>
  <h2>Baby Portrait Prompt Generator for Microsoft Designer</h2>
</div>
<div class="container">
  <div class="instructions">
    <h3>🎨 How to Use This Generator:</h3>
    <ol>
      <li><strong>Fill out the form:</strong> Select options from each dropdown menu to customize your baby portrait</li>
      <li><strong>Multi-select options:</strong> Hold Ctrl (PC) or Cmd (Mac) to select multiple items in Props, Floral Crowns, and Art Effects</li>
      <li><strong>Generate your prompt:</strong> Click "Generate Prompt" to create your custom AI prompt</li>
      <li><strong>Try random combinations:</strong> Click "Random Prompt" for surprise combinations</li>
      <li><strong>Copy and use:</strong> Click "Copy Prompt" and paste it into Microsoft Designer for amazing results!</li>
    </ol>
  </div>
  
  <form id="promptForm" onsubmit="return false;">
    <div class="form-group">
      <label for="hairstyle">Hairstyle:</label>
      <select id="hairstyle" required>
        <option value="">Choose a hairstyle...</option>
        <option>knotless curly puffs</option>
        <option>double buns with floral crown</option>
        <option>loose floral afro</option>
        <option>thick curly hair with daisies</option>
        <option>long curls with lilies</option>
        <option>tiny pigtails with ribbons</option>
        <option>soft baby waves</option>
        <option>crown braid with flowers</option>
        <option>messy top knot</option>
        <option>butterfly clips in curls</option>
        <option>space buns with glitter</option>
        <option>french braided pigtails</option>
        <option>loose ringlets</option>
        <option>half-up bow style</option>
        <option>twisted side braid</option>
        <option>bubble ponytail</option>
        <option>flower headband with loose hair</option>
        <option>mini dutch braids</option>
        <option>curly bob with bangs</option>
        <option>pearl hair accessories</option>
        <option>wispy baby curls</option>
        <option>rainbow hair clips</option>
      </select>
    </div>
    <div class="form-group">
      <label for="skinTone">Skin Tone:</label>
      <select id="skinTone" required>
        <option value="">Choose a skin tone...</option>
        <option>deep brown</option>
        <option>rich chocolate</option>
        <option>warm mahogany</option>
        <option>medium brown</option>
        <option>honey brown</option>
        <option>light caramel</option>
        <option>warm beige</option>
        <option>golden</option>
        <option>peachy</option>
        <option>rosy</option>
        <option>fair</option>
        <option>porcelain</option>
        <option>olive</option>
        <option>warm tan</option>
        <option>bronze</option>
      </select>
    </div>
    <div class="form-group">
      <label for="outfit">Outfit:</label>
      <select id="outfit" required>
        <option value="">Choose an outfit...</option>
        <option>red sweater and white boots</option>
        <option>emerald green overalls</option>
        <option>blue onesie</option>
        <option>pastel dress</option>
        <option>rainbow tutu and white top</option>
        <option>soft pink romper with ruffles</option>
        <option>yellow sunflower dress</option>
        <option>white cotton onesie with animal prints</option>
        <option>lavender cardigan and cream pants</option>
        <option>denim overalls with floral shirt</option>
        <option>coral polka dot dress</option>
        <option>mint green bubble romper</option>
        <option>peach frilly skirt and white blouse</option>
        <option>striped sailor outfit</option>
        <option>butterfly wing costume</option>
        <option>soft gray hoodie and leggings</option>
        <option>cherry print summer dress</option>
        <option>cream knit sweater and bloomers</option>
      </select>
    </div>
    <div class="form-group">
      <label for="pose">Pose:</label>
      <select id="pose" required>
        <option value="">Choose pose...</option>
        <option>seated pose, legs bent</option>
        <option>seated feeding birds</option>
        <option>gently holding puppy</option>
        <option>seated with hands in lap</option>
      </select>
    </div>
    <div class="form-group">
      <label for="background">Background:</label>
      <select id="background" required>
        <option value="">Choose background...</option>
        <option>bright spring garden</option>
        <option>lush grass and flowerbed</option>
        <option>basket filled with flowers</option>
        <option>soft mossy ground</option>
      </select>
    </div>
    <div class="form-group">
      <label for="props">Props / Friends (hold Ctrl/Cmd for multi-select):</label>
      <select id="props" multiple>
        <option>songbirds perched near hands</option>
        <option>gentle doves</option>
        <option>basket of flowers</option>
        <option>puppy (white and brown, fluffy)</option>
        <option>butterflies fluttering around</option>
      </select>
    </div>
    <div class="form-group">
      <label for="floral">Floral Crowns (hold Ctrl/Cmd for multi-select):</label>
      <select id="floral" multiple>
        <option>yellow daisies</option>
        <option>white lilies</option>
        <option>mixed spring blossoms</option>
        <option>large green and pink flowers</option>
      </select>
    </div>
    <div class="form-group">
      <label for="season">Season / Atmosphere:</label>
      <select id="season" required>
        <option value="">Choose a season...</option>
        <option>spring</option>
        <option>summer</option>
        <option>early autumn</option>
      </select>
    </div>
    <div class="form-group">
      <label for="effects">Art Effects (hold Ctrl/Cmd for multi-select):</label>
      <select id="effects" multiple>
        <option>high-gloss finish</option>
        <option>realistic plastic shine</option>
        <option>soft painterly shadows</option>
        <option>vivid color details</option>
        <option>gentle glowing light</option>
        <option>foil shimmer accents</option>
        <option>iridescent highlights</option>
      </select>
    </div>
    <div class="btn-group">
      <button onclick="generatePrompt()">✨ Generate Prompt</button>
      <button onclick="randomPrompt()">🎲 Random Prompt</button>
    </div>
  </form>
  <div class="form-group prompt-output">
    <label for="output">Your AI Prompt for Microsoft Designer:</label>
    <textarea id="output" rows="7" readonly></textarea>
    <button class="copy-btn" onclick="copyPrompt()">📋 Copy Prompt</button>
  </div>
</div>

<div class="thank-you">
  <h3>💖 Thank You for Using House of Star Designs! 💖</h3>
  <p>We hope this generator helps you create beautiful, magical baby portraits! Your creativity brings joy to the world, and we're honored to be part of your artistic journey.</p>
  <p><strong>Happy Creating! ✨</strong></p>
  <p class="signature">- The House of Star Designs Team</p>
</div>

<script>
function generatePrompt() {
  const hairstyle = document.getElementById('hairstyle').value;
  const skinTone = document.getElementById('skinTone').value;
  const outfit = document.getElementById('outfit').value;
  const pose = document.getElementById('pose').value;
  const background = document.getElementById('background').value;
  const props = Array.from(document.getElementById('props').selectedOptions).map(o => o.value).join(', ');
  const floral = Array.from(document.getElementById('floral').selectedOptions).map(o => o.value).join(', ');
  const season = document.getElementById('season').value;
  const effects = Array.from(document.getElementById('effects').selectedOptions).map(o => o.value).join(', ');

  if (!hairstyle || !skinTone || !outfit || !pose || !background || !season) {
    alert('Please fill in all required fields!');
    return;
  }

  let prompt = `Create a detailed kawaii chibi baby portrait, with ${hairstyle} hairstyle and ${skinTone} skin, wearing a ${outfit}. ` +
    `The baby is in a ${pose} in a ${background}. ` +
    `Props include: ${props.length ? props : "none"}. ` +
    `Floral details: ${floral.length ? floral : "none"}. ` +
    `Scene has a ${season} garden vibe. ` +
    `Apply these art effects: ${effects.length ? effects : "soft painterly light, high-gloss shine"}. ` +
    `Main style: highly detailed, adorable, Bratz and chibi inspired, studio-lit, ultra-glossy finish.`;

  document.getElementById('output').value = prompt;
}

function randomPrompt() {
  const hairstyles = ['knotless curly puffs', 'double buns with floral crown', 'loose floral afro', 'thick curly hair with daisies', 'long curls with lilies', 'tiny pigtails with ribbons', 'soft baby waves', 'crown braid with flowers', 'messy top knot', 'butterfly clips in curls', 'space buns with glitter', 'french braided pigtails', 'loose ringlets', 'half-up bow style', 'twisted side braid', 'bubble ponytail', 'flower headband with loose hair', 'mini dutch braids', 'curly bob with bangs', 'pearl hair accessories', 'wispy baby curls', 'rainbow hair clips'];
  const skinTones = ['deep brown', 'rich chocolate', 'warm mahogany', 'medium brown', 'honey brown', 'light caramel', 'warm beige', 'golden', 'peachy', 'rosy', 'fair', 'porcelain', 'olive', 'warm tan', 'bronze'];
  const outfits = ['red sweater and white boots', 'emerald green overalls', 'blue onesie', 'pastel dress', 'rainbow tutu and white top', 'soft pink romper with ruffles', 'yellow sunflower dress', 'white cotton onesie with animal prints', 'lavender cardigan and cream pants', 'denim overalls with floral shirt', 'coral polka dot dress', 'mint green bubble romper', 'peach frilly skirt and white blouse', 'striped sailor outfit', 'butterfly wing costume', 'soft gray hoodie and leggings', 'cherry print summer dress', 'cream knit sweater and bloomers'];
  const poses = ['seated pose, legs bent', 'seated feeding birds', 'gently holding puppy', 'seated with hands in lap'];
  const backgrounds = ['bright spring garden', 'lush grass and flowerbed', 'basket filled with flowers', 'soft mossy ground'];
  const propsArr = ['songbirds perched near hands', 'gentle doves', 'basket of flowers', 'puppy (white and brown, fluffy)', 'butterflies fluttering around'];
  const floralArr = ['yellow daisies', 'white lilies', 'mixed spring blossoms', 'large green and pink flowers'];
  const seasons = ['spring', 'summer', 'early autumn'];
  const effectsArr = ['high-gloss finish', 'realistic plastic shine', 'soft painterly shadows', 'vivid color details', 'gentle glowing light', 'foil shimmer accents', 'iridescent highlights'];

  function pickRandom(arr) {
    return arr[Math.floor(Math.random() * arr.length)];
  }
  function pickMultiple(arr, count) {
    let set = new Set();
    while (set.size < count && set.size < arr.length) {
      set.add(pickRandom(arr));
    }
    return Array.from(set);
  }

  document.getElementById('hairstyle').value = pickRandom(hairstyles);
  document.getElementById('skinTone').value = pickRandom(skinTones);
  document.getElementById('outfit').value = pickRandom(outfits);
  document.getElementById('pose').value = pickRandom(poses);
  document.getElementById('background').value = pickRandom(backgrounds);
  document.getElementById('season').value = pickRandom(seasons);

  const propsSelect = document.getElementById('props');
  const selectedProps = pickMultiple(propsArr, Math.floor(Math.random() * 3) + 1);
  Array.from(propsSelect.options).forEach(option => {
    option.selected = selectedProps.includes(option.value);
  });

  const floralSelect = document.getElementById('floral');
  const selectedFloral = pickMultiple(floralArr, Math.floor(Math.random() * 2) + 1);
  Array.from(floralSelect.options).forEach(option => {
    option.selected = selectedFloral.includes(option.value);
  });

  const effectsSelect = document.getElementById('effects');
  const selectedEffects = pickMultiple(effectsArr, Math.floor(Math.random() * 3) + 2);
  Array.from(effectsSelect.options).forEach(option => {
    option.selected = selectedEffects.includes(option.value);
  });

  generatePrompt();
}

function copyPrompt() {
  const promptText = document.getElementById('output').value;
  if (!promptText) {
    alert('Please generate a prompt first!');
    return;
  }
  navigator.clipboard.writeText(promptText).then(function() {
    alert('Prompt copied to clipboard!');
  }).catch(function() {
    const prompt = document.getElementById('output');
    prompt.select();
    prompt.setSelectionRange(0, 99999);
    document.execCommand('copy');
    alert('Prompt copied to clipboard!');
  });
}
</script>

<script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'9884f6f2b2bfa1e6',t:'MTc1OTQxNjEyOC4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
