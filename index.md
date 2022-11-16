<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="style.css" />
    <script src="https://code.jquery.com/jquery-3.6.1.min.js" integrity="sha256-o88AwQnZB+VDvE9tvIXrMQaPlFFSUTR+nldQm1LuPXQ=" crossorigin="anonymous"></script>

    <title>Watsonisite-Information about Crypto</title>
</head>

<body>
    <img id="logo" src="LOGO.png" alt="Watsonisite-Information about Crypto" />
    <div id="landingPage">
        <p id="CryptoTitle">crypto</p>
        <nav>
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">Features</a></li>
                <li><a href="#">About Us</a></li>
            </ul>
        </nav>
        <div id="heroSection">
            <p id="heroText">
                <span id="crypt">Exclusive Crypto<br> Analysis & Trending<br> Currencies</span>
            </p>
            <p id="heroDescription">
                Get all the up-to-date information from Watsonsite.
            </p>
            <p id="Information">Cryptocurrencies have been a major trend that is fast crossing all borders. With the growing interest in Bitcoin and Ethereum, many people want to invest in the trending cryptocurrency market with its huge potential.
                <br> → Watsonsite is a site that includes information about cryptocurrencies, the trends, the price, and the performance of the particular cryptocurrencies. <br> → Watsonsite gives you access to dozens of cryptocurrency resources and analysis
                on digital currencies.
            </p>
            <button id="Trending">Trending</button>
        </div>
        <div id="imageSection"> <img src="crypto-removebg-preview.png" />
        </div>
        <div class="coin-list">
            <div class="coin">
                <img src="Bitcoin.png">
                <div>
                    <h3>$<span id="bitcoin"></span></h3>
                    <p>Bitcoin</p>
                </div>
            </div>
            <div class="coin">
                <img src="Ethereum.png">
                <div>
                    <h3>$<span id="ethereum"></span></h3>
                    <p>Ethereum</p>
                </div>
            </div>
            <div class="coin">
                <img src="Dogecoin.png">
                <div>
                    <h3>$<span id="dogecoin"></span></h3>
                    <p>Dogecoin</p>
                </div>
            </div>
        </div>
    </div>
    <div class="hero">
        <p>Subscribe for more updates</p>
        <form name="submit-to-google-sheet">
            <input type="email" name="Email" placeholder="Your Email ID" required>
            <button type="submit"><img src="Send.png" width="30px" ></button>
        </form>
        <span id="msg"><p2></p2></span>
    </div>
    </div>
    <script>
        const scriptURL = 'https://script.google.com/macros/s/AKfycbxunoI_l3676dWxbgpK6Hb5ooTuEQoYLQE0HGYDD5Byy3H7bS6ex6qphl54pXMLxQLU_w/exec'
        const form = document.forms['submit-to-google-sheet']
        const msg = document.getElementById("msg")

        form.addEventListener('submit', e => {
            e.preventDefault()
            fetch(scriptURL, {
                    method: 'POST',
                    body: new FormData(form)
                })
                .then(response => {
                    msg.innerHTML = "Thank You for Subscribing!"
                    setTimeout(function() {
                        msg.innerHTML = ""
                    }, 5000)
                    form.reset()
                })
                .catch(error => console.error('Error!', error.message))
        })
    </script>
</body>
<script src="script.js"></script>

</html>

<!-- Gmail id for Google Sheets is
Gmail: yokaifuuu@gmail.com
Password: kaifu1234 -->
