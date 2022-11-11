# Web-Monetization-API-Tutorial-How-to-Add-Microtransactions-to-a-Website

https://raw.githubusercontent.com/RodrigoMvs123/Web-Monetization-API-Tutorial-How-to-Add-Microtransactions-to-a-Website/main/README.md

https://github.com/RodrigoMvs123/Web-Monetization-API-Tutorial-How-to-Add-Microtransactions-to-a-Website/blame/main/README.md

https://www.youtube.com/watch?v=XwzcrhhyDkc


https://interledger.org/

Payment Pointers 
$ania.wallet.exemple 
$ania.wallet.exemple/.well-known/pay 

https://wallet.uphold.com/login

https://coil.com/

https://help.coil.com/docs/membership/coil-extension/index.html

https://coil.com/auth/membership-signup

https://www.hostinger.com/
https://hpanel.hostinger.com/domains/domain-checker

https://unsplash.com/

https://www.hostinger.com/hosting/ania-kubow.online
File manager 
Dashboard 
public.html
drag and drop files on Hostinger 
ania-kubol.online ( Copy and Paste on the browser )
inspect the page 
Stream Payments ( https://coil.com/ )

            App.js ( copy ) 
File manager 
Dashboard 
public.html
App.js ( Paste and Save ) 
ania-kubow.online ( https:// ) 



public_html ( App.js ) 
const link = document.querySelector('link [rel="monetization"]')
 
let total = 0 
let scale
 
link.addEventListener("monetization", (e) => { 
    // Display to user if monetazation is on
    const monetizationDisplay = document.getElementById ("monetization-info")
    monetizationDisplay.textContent = "Monetized"
    monetizationDisplay.classList.add("monetized")
    monetizationDisplay.classList.remove("not-monetized")
 
    // Show exclusive content to the user if monetization is on
    document.getElementById("exclusive").classList.remove("hidden")
 
    // Implement micropayment counter and display it to our user 
    const { amount, assetCode, assetScale} = e
 
    if ( total == 0 ) {
        scale= assetScale
        document.getElementById(currency).innerText = assetCode
    }
    total += Number(amount)
    const formattedTotal = total (total * Math.pow(10, -scale)).toFixed(scale)
    document.getElementById("total").inner.Text = formattedTotal 
})



public_html ( Index.js )
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Web Monetization</title>
    <link 
    
          rel="monetization"
          href="https://wallet.uphold.com/login"
    >
    <link rel="stylesheet" href="Styles.Css">
</head>
<body>
    <header>
        <div class="info-container">
            <div class="logo-container">
            <h2>+</h2>
 
            </div>
            <div id="monetization-info" class="not-monetized">
                Not Monetized
            </div>
        </div>
        <div class="title info">
            <h1>Welcome to my Photo Blog</h1>
            <p>Use monetization in order to see hidden content</p>
            <p>With your help, you have supported me by <span id="total">0</span><span id="currency"></span></p>
        </div>
    </header>
<div class="article-container">
    <hr/>
    <section>
 
    <article>
 
        <h2>Wineglass Bay, Australia</h2>
        <img> src="https://images.unsplash.com/photo-1667926964370-840afdde03e1?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxlZGl0b3JpYWwtZmVlZHwzfHx8ZW58MHx8fHw%3D&auto=format&fit=crop&w=500&q=60" alt="A photo of wineglass bay Australia"
        <p>
            Around 80% of Australia's premium wine is produced in South Australia 
            by over 700 wineries. In 2017-18, South Australia's wine industry 
            generated more than $2.15 billion in revenue.
        </p>
    </article>
 
    <article id="exclusive" class="hidden">
 
        <h2>Giveaway for my loyal readers!</h2>
        <img> src="https://images.unsplash.com/photo-1667979014768-8f03a6703ab3?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxlZGl0b3JpYWwtZmVlZHwyOHx8fGVufDB8fHx8&auto=format&fit=crop&w=500&q=60" alt="A photo of the mountains"
        <p>
            Anyone viewing this width web monetization on has the chance to win 
            this trip ! I have never been but I hear such wonderful things. 
            Please make sure to send to me a postcard when you get there. Best of luck in this competition.
        </p>
    </article>
 
    <article>
 
        <h2>Village of Reine</h2>
        <img> src="https://images.unsplash.com/photo-1667731989765-1c03361cc740?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxlZGl0b3JpYWwtZmVlZHwzNXx8fGVufDB8fHx8&auto=format&fit=crop&w=500&q=60" alt="A photo of a flower"
        <p>
            The breathtaking village of Reine is located on the island of Moskenesaya on 
            northern Norway´s lofoten archipelago.
        </p>
    </article>
 
    <article>
 
        <h2>Orchard Spring Lane, Merlion, Singapore</h2>
        <img> src="https://images.unsplash.com/photo-1667924743664-689b4d5bab13?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxlZGl0b3JpYWwtZmVlZHw0MHx8fGVufDB8fHx8&auto=format&fit=crop&w=500&q=60" alt="A photo of the merlion"
        <p>
            The Merlion´s fish-like body symbolises Singapore´s origins as a fishing village,
            known as Temasek a name with comes from same root as the world tasek ('Lake' in Malay ).
        </p>
    </article>
 
    <article>
 
        <h2>Long Tail Alley</h2>
        <img> src="https://images.unsplash.com/photo-1667853003724-fd11b2f8863b?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxlZGl0b3JpYWwtZmVlZHw4Mnx8fGVufDB8fHx8&auto=format&fit=crop&w=500&q=60" alt="A photo of the lake"
        <p>
           Today long-tail boats can be found on numerous Thai waterways, from the floating markets
           and the canals of Bangkok to the estuaries and deltas of the Gulf of Thailand. 
        </p>
    </article>
 
    <article>
 
        <h2>Seoul, South Korea</h2>
        <img> src="https://images.unsplash.com/photo-1667833270216-534aab3d2da7?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxlZGl0b3JpYWwtZmVlZHwxMzR8fHxlbnwwfHx8fA%3D%3D&auto=format&fit=crop&w=500&q=60" alt="A photo of a office"
        <p>
            Seoul is known for its vibrant districts, eclectic fashion scene, delicious street food,
            and for been the birthplace of K-pop and Hallyu. Despite been a technologically advanced 
            country, Seoul is still famous for its historical sites and traditional culture. 
        </p>
    </article>
 
    </section>
</div>
<script src="app.js"></script>
</body>
</html>


 
public_html ( Style.Css )
@import url('https://fonts.googleapis.com/css2?family=Hind+Siliguri:wat@300;400;600,700&display=swap);
 
* {
    font-family: 'Hind Siliguri', sans-serif; 
}
 
body {
    margin: 0;
    padding: 0;
}
 
header {
    background-color: #fadad1;
    widht: 100%;
}
 
 
header .title-info {
    height: 400px;
    text-align: center;
    display: flex;
    flex-direction: column;
    justify-content: center;
}
 
header .info-container {
    width: 100%;
    display: flex;
    justify-content: space-between;
 
}
 
header .info-container #monetization-info {
    color: #e7e7e7;
    padding: 10px;
    border-radius: 10px;
    width: 140px;
    margin: 20px;
    text-align: center;
}
 
.not-monetized {
    background-color: #f14261;
 
}
 
.monetized {
    background-color: #4c8456;
    
}
 
.logo-container {
    padding: 0 20px;
 
}
 
hr {
    margin-bottom: 40px;
}
 
section: {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
 
}
 
article {
    border-radius: 10px;
    box-shadow: rgba(99, 99, 99, 0.2) 0 2px 8px 0;
    padding: 10px;
    display: flex;
    flex-direction: column;
    max-width: 400px;
    margin: 10px;
    color: #717070;
}
 
article img {
    width 100%;
 
}
 
.hidden {
    display: none;
}
 
#exclusive {
    background-color: #ee899b;
 
}




