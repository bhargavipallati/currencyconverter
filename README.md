# currencyconverter
#indian rupee value in 5 diff currencies using HTML
<html>

<head>
    <title>Currency Converter</title>
</head>
<style>
    body {
        background-color: rgb(213, 191, 248);
    }

    h1 {

        background: rgb(149, 234, 224);
        background: #00CC99;
        text-align: center;
        font-size: 38px;
        padding: 20px 1em;
        font-weight: bold;
        margin-left: 35%;
        margin-right: 35%;
        cursor: pointer;
        font-family: Times New Roman;
    }

    marquee {
        background: #00FFFF;
        font-size: 20px;
        padding-top: 6px;
        margin: 23px;
        margin-left: 35%;
        margin-right: 35%;
        cursor: pointer;
        align-self: center;
    }

    fieldset {
        justify-content: space-around;
        width: 45%;
        margin: auto;
        border: 1px solid #000;
        text-align: left;
        font-size: 20px;
        font-family: lato, sans-serif;
    }

    input {
        background: #fff;
        border: 1px solid #000;
        border-radius: 2px;
        border-width: 1px;
        color: #36454b;
        font-size: 15px;
        margin: 5px;
        margin-left: 25px;
        padding: 12px;
        display: inline-block;
    }

    button {
        width: 80px;
        height: 43px;
        font-weight: bold;
    }

    input[type=rest] {
        width: 95px;
        height: 43px;
        font-weight: bold;
    }
</style>




<body>
    <h1>Currency Converter</h1>
    <marquee>Welcome to the Online Currency Converter</marquee>

    <form name="converter">

        <fieldset>

            <label>IND Currency(Rupees):</label>
            <input type="text" id="ind">
            <button type="button" onclick="getInputValue();">Get Value</button><br><br>

            <br>
            <label>Dollar(American):</label>   
            <input id="doller"><br><br>


            <label>Rand(South africa):</label>
            <input id="rand"><br><br>

            <label>Won(Korea):</label>      
            <input id="Won"><br><br>

            <label>Riyal(Saudia):</label>
            <input id="Riyal"><br><br>

            <label>Diner(Kuwait):</label>
            <input id="Diner"><br><br>


            <input type="reset" value="Reset  Form">
            <p align ="center">You can press Reset Button for resetting the form</p>

        </fieldset>
    </form>
    <script>
        function getInputValue() {
            var valNum = document.getElementById("ind").value
            if (valNum <= 0)
                window.alert("Enter Value Greater than0");
            else {
                document.getElementById("doller").value = valNum / 77.48;
                document.getElementById("rand").value = (valNum / 4.94).toFixed(2);
                document.getElementById("Won").value = (valNum / 0.061).toFixed(2);
                document.getElementById("Riyal").value = (valNum / 20.66).toFixed(2);
                document.getElementById("Diner").value = (valNum / 553.36).toFixed(2)
            }
        }
    </script>
</body>

</html>
