...html
      <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dashboard layout</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="grid-container">
        <div class="header">Header</div>
        <div class="sidebar">Sidebar</div>
        <div class="main">Main Content</div>
        <div class="widget1">Widget1</div>
        <div class="widget2">widget2</div>
        <div class="footer">footer</div>
    </div>
</body>
</html>

...css
     body{
    margin: 0;
    font-style:Arial,Helvetica,sans-serif;
}

.grid-container{
    display: grid;
    grid-template-areas: 
    'header header header'
    'sidebar main main'
    'sidebar widget1 widget2'
    'footer footer footer';
     grid-gap: 10px;
     padding: 10px;
}

.grid-container > div{
    
    padding: 20px;
    border: 1px solid #ddd;
    text-align: center;
}
.header{
    grid-area: header;
    background-color: #ffdb4d;
}

.sidebar{
    grid-area: sidebar;
    background-color: #ff704d;
}

.main{
    grid-area: main;
    background-color: #4ca;
}

.widget1{
    grid-area: widget1;
    background-color: #f9e79f;
}

.widget2{
    grid-area:widget2;
    background-color: #82e0aa;
}

.footer{
    grid-area:footer;
    background-color: #bfc9ca;
}

@media (max-width:768px){
    .grid-container{
        grid-template-areas: 
        'header'
        'sidebar'
        'main'
        'widget1'
        'widget2'
        'footer';
    }
}
