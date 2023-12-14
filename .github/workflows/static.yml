<!DOCTYPE html>
<html lang="en">
    <head>
        <title>URL Shortener</title>
      <style>
        body {
    background-image:url("https://bit.ly/3uXy1cw");
    font-family: Garamond, serif;
    
    margin: 0;
}

.outdiv {
    display: flex;
    flex-direction: row;
    justify-content: center;
    height: 100vh;
}

.innerdiv {
    align-self: center;
    width: 70%;
    padding: 20px;
    background-color:#6088c3;
    border-radius: 163px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    border: 49px solid azure;
}

h1 {
    font-size: 32px;
    margin-bottom: 20px;
    text-align: center;
}

form {
    display: flex;
    align-items: center;
    margin-bottom: 20px;
}

label {
    font-size: 18px;
    margin-right: 15px;
}

input[type="text"] {
    flex-grow: 1;
    height: 40px;
    border: none;
    border-radius: 5px;
    padding: 0 10px;
    font-size: 18px;
    border-radius: 79px;
    border: 3px solid rebeccapurple;
}

button[type="submit"] {
    height: 40px;
    border: none;
    border-radius: 163px;
    background-color: #ff0000;
    color: #fff;
    padding: 0 20px;
    font-size: 18px;
    cursor: pointer;
}

#result {
    font-size: 18px;
    text-align: center;
    color: #007;
    display: none;
    margin-top: 20px;
}

#level {
    text-align: center;
    align-items: center;
    justify-content: center;
}
      </style>
      
<b:skin><![CDATA[
<style>
body {
  background-color: #f0f0f0;
}
</style>
]]>
</b:skin>

    </head>
    <body >
        <div class="outdiv">
            <div class="innerdiv">
                <div id="level">
                    <h1>Link Shortener</h1>
                </div>
                <form>
                  <label for="url"><b>Enter URL:</b></label><br></br>
                    <input type="text" id="url" name="url" placeholder="https://google.com" style="font-family: Garamond, serif;"><br></br></input>
                    <button type="submit" id="submit-btn">Shorten</button>
                </form>
                <div id="result"></div>
            </div>
        </div>
        <script>
                  const form = document.querySelector('form');
const input = document.querySelector('#url');
const resultDiv = document.querySelector('#result');

form.addEventListener('submit', async (e) => {
    e.preventDefault();

    const url = input.value;

    const response = await fetch('https://api-ssl.bitly.com/v4/shorten', {
        method: 'POST',
        headers: {
            'Content-Type': 'application/json',
            'Authorization': 'Bearer 26774534336cb4f2fe40e511bd90e285d9e9042d'
        },
        body: JSON.stringify({
            long_url: url
        })
    });

    const data = await response.json();
    const shortUrl = data.link;

          resultDiv.innerHTML = <p><b>Short URL:</b> <b><a href="${shortUrl}" target="_blank" style="color:red">${shortUrl}</a></b></p>;
    resultDiv.style.display = 'block';
});
</script>
    </body>
</html>
