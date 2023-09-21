<!DOCTYPE html>
<html>
<head>
    <title>Simple Calculator</title>
    <style>
        /* Add some basic CSS for styling */
        #calculator {
            width: 300px;
            margin: 50px auto;
            border: 1px solid #ccc;
            padding: 10px;
            border-radius: 5px;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.2);
        }
        input[type="text"] {
            width: 100%;
            padding: 10px;
            font-size: 18px;
        }
        input[type="button"] {
            width: 45px;
            height: 45px;
            font-size: 18px;
            margin: 5px;
        }
    </style>
</head>
<body>
    <div id="calculator">
        <input type="text" id="display" readonly>
        <table>
            <tr>
                <td><input type="button" value="7" onclick="addToDisplay('7')"></td>
                <td><input type="button" value="8" onclick="addToDisplay('8')"></td>
                <td><input type="button" value="9" onclick="addToDisplay('9')"></td>
                <td><input type="button" value="/" onclick="addToDisplay('/')"></td>
            </tr>
            <tr>
                <td><input type="button" value="4" onclick="addToDisplay('4')"></td>
                <td><input type="button" value="5" onclick="addToDisplay('5')"></td>
                <td><input type="button" value="6" onclick="addToDisplay('6')"></td>
                <td><input type="button" value="*" onclick="addToDisplay('*')"></td>
            </tr>
            <tr>
                <td><input type="button" value="1" onclick="addToDisplay('1')"></td>
                <td><input type="button" value="2" onclick="addToDisplay('2')"></td>
                <td><input type="button" value="3" onclick="addToDisplay('3')"></td>
                <td><input type="button" value="-" onclick="addToDisplay('-')"></td>
            </tr>
            <tr>
                <td><input type="button" value="0" onclick="addToDisplay('0')"></td>
                <td><input type="button" value="." onclick="addToDisplay('.')"></td>
                <td><input type="button" value="=" onclick="calculate()"></td>
                <td><input type="button" value="+" onclick="addToDisplay('+')"></td>
            </tr>
            <tr>
                <td colspan="4"><input type="button" value="C" onclick="clearDisplay()"></td>
            </tr>
        </table>
    </div>
    <script>
        // JavaScript functions to handle calculator operations

        // Function to add a character to the display
        function addToDisplay(value) {
            document.getElementById('display').value += value;
        }

        // Function to calculate the result and update the display
        function calculate() {
            try {
                document.getElementById('display').value = eval(document.getElementById('display').value);
            } catch (error) {
                document.getElementById('display').value = 'Error';
            }
        }

        // Function to clear the display
        function clearDisplay() {
            document.getElementById('display').value = '';
        }
    </script>
</body>
</html>

