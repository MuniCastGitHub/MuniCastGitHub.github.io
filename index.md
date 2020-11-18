<!DOCTYPE html>

<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE-edge">
    <title>MuniTrends</title>
    <meta name="description" content="">
    <meta name="viewport" content="width-device-width, initial-scale-1">
    <link rel="stylesheet" href="style.css">
</head>

<body>
    <div class="page">
        <div class="sidebar-background"></div>
        <div class="logo-main-box" id="logo-wrapper">
            <img src="logo-white.png" alt="" class="logo-main">
        </div>
        <ul class="nav-head">
            <li class="left-stack" id="li-logo"><a href="#" class="nav-button" id="home-button"><img src="logo-head.png" alt="Home" class="logo-head" id="logo-head"></a></li>
            <li class="right-stack"><a href="#" class="nav-button">Login</a></li>
            <li class="right-stack"><a href="#" class="nav-button">Subscribe</a></li>
            <li class="right-stack"><a href="#" class="nav-button">Contact</a></li>
        </ul>
        <ul class="page-tabs">
            <li class="page-tab"><button class="tab-button dropdown-button">Key Indicators</button></li>
            <ul class="subcategory" id="dropdowncontent">
                <li class="page-tab"><button class="tab-button">Demographics</button></li>
                <li class="page-tab"><button class="tab-button">Employment and Jobs</button></li>
                <li class="page-tab"><button class="tab-button">Manufacturing Production</button></li>
                <li class="page-tab"><button class="tab-button">Inflation and <br>Price Indices</button></li>
                <li class="page-tab"><button class="tab-button">Real Estate Values</button></li>
                <li class="page-tab"><button class="tab-button">State Revenue Trends</button></li>
                <li class="page-tab"><button class="tab-button">Retail Sales and Inventory</button></li>
                <li class="page-tab"><button class="tab-button">Travel and Tourism</button></li>
                <li class="page-tab"><button class="tab-button">Other</button></li>
            </ul>
            <li class="page-tab"><a class="tab-button">2020 Report</a></li>
            <li class="page-tab"><a class="tab-button">FTE and Payroll</a></li>
            <li class="page-tab"><a class="tab-button">Municast</a></li>
            <li class="page-tab"><a class="tab-button">Sources</a></li>
            <li class="page-tab"><a class="tab-button" id="FRED">FRED Data</a></li>
        </ul>
        <div class="main-content">
            <div class="iframe-box">
                <div class="embed-container"><iframe src="https://fred.stlouisfed.org/graph/graph-landing.php?g=xUnk&width=670&height=475" scrolling="no" frameborder="0" style="overflow:hidden;" allowTransparency="true" loading="lazy"></iframe></div>
                <script src="https://fred.stlouisfed.org/graph/js/embed.js" type="text/javascript"></script>
            </div>
            <div class="iframe-box">
                <div class="embed-container"><iframe src="https://fred.stlouisfed.org/graph/graph-landing.php?g=xUpo&width=670&height=475" scrolling="no" frameborder="0" style="overflow:hidden;" allowTransparency="true" loading="lazy"></iframe></div>
                <script src="https://fred.stlouisfed.org/graph/js/embed.js" type="text/javascript"></script>
            </div>

            <div class="iframe-box">
                <div class="embed-container"><iframe src="https://fred.stlouisfed.org/graph/graph-landing.php?g=xUsC&width=670&height=475" scrolling="no" frameborder="0" style="overflow:hidden;" allowTransparency="true" loading="lazy"></iframe></div>
                <script src="https://fred.stlouisfed.org/graph/js/embed.js" type="text/javascript"></script>
            </div>
            <div class="iframe-box">
                <div class="embed-container"><iframe src="https://fred.stlouisfed.org/graph/graph-landing.php?g=xUsF&width=670&height=475" scrolling="no" frameborder="0" style="overflow:hidden;" allowTransparency="true" loading="lazy"></iframe></div>
                <script src="https://fred.stlouisfed.org/graph/js/embed.js" type="text/javascript"></script>
            </div>
            <div class="iframe-box">
                <div class="embed-container"><iframe src="https://fred.stlouisfed.org/graph/graph-landing.php?g=xUsZ&width=670&height=475" scrolling="no" frameborder="0" style="overflow:hidden;" allowTransparency="true" loading="lazy"></iframe></div>
                <script src="https://fred.stlouisfed.org/graph/js/embed.js" type="text/javascript"></script>
            </div>
        </div>
    </div>
</body>

<script>
    //STICKY ANIMATIONS
    window.addEventListener("scroll", function() {
        let logo = document.getElementById("li-logo");
        let logoimg = document.getElementById("logo-head");
        let logolink = document.getElementById("home-button");
        let yValue = document.getElementById("logo-wrapper").clientHeight;
        if (window.pageYOffset < yValue) {
            logoimg.classList.add("slideout");
            logoimg.classList.remove("slidein");
            logolink.classList.add("slideout");
            logolink.classList.remove("slidein");

        } else {
            logo.classList.add("is-visible");
            logoimg.classList.remove("slideout");
            logoimg.classList.add("slidein");
            logolink.classList.remove("slideout");
            logolink.classList.add("slidein");
        }
    });

    //DROPDOWN SIDEBAR
    var dropdown = document.getElementsByClassName("dropdown-button");
    var i;
    for (i = 0; i < dropdown.length; i++) {
        dropdown[i].addEventListener("click", function() {
            this.classList.toggle("nav-button-active");
            var dropdownContent = document.getElementById("dropdowncontent");
            if (dropdownContent.style.display === "block") {
                dropdownContent.style.display = "none";
            } else {
                dropdownContent.style.display = "block";
            }
        });
    }
</script>

</html>
