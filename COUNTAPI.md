1.) SET UP YOUR HTML, CSS, & JavaScript

<h1>This site has been visited <span id="visits"></span> times.</h1>

2.) CREATE A NAMESPACE

https://api.countapi.xyz/create?namespace={name of your website}&enable_reset=1


3.) ADD THIS SCRIPT IN THE TOP OF YOUR INDEX.HTML FILE

 <script async src="https://api.countapi.xyz/hit/{namespace}/{key}?callback=websiteVisits"></script>


4.) ADD THIS FUNCTION IN YOUR SCRIPT.JS FILE 

function websiteVisits(response) {
    document.querySelector("#visits").textContent = response.value;
}


* BONUS 

5.) RESET THE VALUE OF YOUR KEY

https://api.countapi.xyz/set/{namespace}/{key}?value={whatever you want, most likely 0}


6.) VIEW THE CURRENT VALUE OF YOUR KEY

https://api.countapi.xyz/get/{namespace}/{key}