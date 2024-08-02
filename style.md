#CSS

```style.css

*{
    padding:0;
    margin:0;
    overflow: hidden;
}
a{
    text-decoration: none;
    color:black;
}
body{
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: #f0f0f0;
    height: 100vh;
}
.weather-app{
    height: 100vh;
    width:100vw;
    text-align: center;
} 
.weather-app h1{
    font-family: "DM Serif Display", serif;
    font-weight: 400;
    font-style: normal;
    font-style: italic;
    padding:10px;
    margin:30px 0 10px 0;

}
#city{
    font-family: "DM Serif Display", serif;
    padding:10px;
    width:100%;
    margin: 50px 7.5px 10px ;
    box-shadow: 0 0 15px rgba(0, 0, 0, 0.256);    
    border-radius: 1px solid #ddd;
    border-radius: 20px;
}
button{
    font-family: "DM Serif Display", serif;
    padding: 30px 30px;
    border: none;
    color: white;
    border-radius: 4px;
    cursor: pointer;
    margin-top:10px;
}
button:hover{
    background: #0155b0;
    box-shadow: 0 0 20px rgba(0, 49, 123, 0.7);
    animation: ease-in-out;
}
#weatherData{
    /* display:none; */
    margin-top: 20px;
}

```