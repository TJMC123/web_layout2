# web_layout2<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple Web Layout</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            margin: 0;
            padding: 0;
        }
        .nav-bar {
            background-color: red;
            display: flex;
            padding: 10px 20px;
        }
        .nav-item {
            position: relative;
            margin-right: 20px;
        }
        .nav-item a {
            color: blueviolet;
            text-decoration: none;
            padding: 10px 15px;
            display: block;
        }
        .nav-item a:hover {
            background-color: whitesmoke;
        }
        .dropdown, .sub-dropdown {
            display: none;
            position: absolute;
            background-color: red;
            min-width: 160px;
            top: 100%;
            left: 0;
            z-index: 1;
        }
        .dropdown a, .sub-dropdown a {
            padding: 10px 15px;
        }
        .nav-item:hover .dropdown {
            display: block;
        }
        .dropdown-item:hover .sub-dropdown {
            display: block;
            left: 100%;
            top: 0;
        }
    </style>
</head>
<body>
    <nav class="nav-bar">
        <div class="nav-item"><a href="#">Home</a></div>
        <div class="nav-item"><a href="#">About</a></div>
        <div class="nav-item">
            <a href="#">Services</a>
            <div class="dropdown">
                <a href="#">Web Design</a>
                <div class="dropdown-item">
                    <a href="#">Development</a>
                    <div class="sub-dropdown">
                        <a href="#">Frontend</a>
                        <a href="#">Backend</a>
                    </div>
                </div>
                <a href="#">SEO</a>
                <a href="#">Marketing</a>
            </div>
        </div>
        <div class="nav-item"><a href="#">Contact</a></div>
    </nav>
</body>
</html>


