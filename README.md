## AIM:
To design a web application for a standard calculator with minimum five operations.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for creating attractive colors.

### Step 4:
Write JavaScript program for implementing five different operations.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :

### CAlC.HTML
```
<html>
<head>
    <title>Simple Calculator</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }

        #calculator-container {
            background-color: #b82d2d;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(156, 125, 201, 0.2);
        }

        input[type="text"] {
            width: 100%;
            padding: 10px;
            margin: 5px 0;
            color: rgb(44, 46, 47); 
        }

        table {
            margin-top: 10px;
        }

        button {
            padding: 10px 20px;
            font-size: 20px;
        }

        /* Define colors for operators */
        button[data-operator="+"] {
            background-color: #99e1e2;
        }

        button[data-operator="-"] {
            background-color: #7ed787;
        }

        button[data-operator="*"] {
            background-color: #ece6eb;
        }

        button[data-operator="/"] {
            background-color: #3a2123;
        }

        button[data-operator="%"] {
            background-color: #400254;
        }

        button[data-operator="sqrt"] {
            background-color: #afca6f;
        }
    </style>
</head>
<body>
    <div id="calculator-container">
        <h1>Calculator</h1>
        <input type="text" id="display" readonly>
        <table>
            <tr>
                <td><button onclick="appendToDisplay('1')">1</button></td>
                <td><button onclick="appendToDisplay('2')">2</button></td>
                <td><button onclick="appendToDisplay('3')">3</button></td>
                <td><button data-operator="+" onclick="appendToDisplay('+')" style="color: white;">+</button></td>
            </tr>
            <tr>
                <td><button onclick="appendToDisplay('4')">4</button></td>
                <td><button onclick="appendToDisplay('5')">5</button></td>
                <td><button onclick="appendToDisplay('6')">6</button></td>
                <td><button data-operator="-" onclick="appendToDisplay('-')" style="color: white;">-</button></td>
            </tr>
            <tr>
                <td><button onclick="appendToDisplay('7')">7</button></td>
                <td><button onclick="appendToDisplay('8')">8</button></td>
                <td><button onclick="appendToDisplay('9')">9</button></td>
                <td><button data-operator="*" onclick="appendToDisplay('*')" style="color: white;">*</button></td>
            </tr>
            <tr>
                <td><button onclick="appendToDisplay('0')">0</button></td>
                <td><button data-operator="%" onclick="appendToDisplay('%')">%</button></td>
                <td><button data-operator="sqrt" onclick="calculateSquareRoot()">√</button></td>
                <td><button data-operator="/" onclick="appendToDisplay('/')" style="color: white;">/</button></td>
            </tr>
            <tr>
                <td colspan="3"><button onclick="clearDisplay()">C</button></td>
                <td><button onclick="calculateResult()">=</button></td>
            </tr>
        </table>
    </div>
    <script>
        function appendToDisplay(value) {
            document.getElementById('display').value += value;
        }

        function clearDisplay() {
            document.getElementById('display').value = '';
        }

        function calculateResult() {
            try {
                document.getElementById('display').value = eval(document.getElementById('display').value);
            } catch (error) {
                document.getElementById('display').value = 'Error';
            }
        }

        function calculateSquareRoot() {
            const inputValue = document.getElementById('display').value;
            const result = Math.sqrt(parseFloat(inputValue));
            document.getElementById('display').value = result;
        }
    </script>
</body>
</html>
```

## OUTPUT:
![Screenshot 2023-11-15 204953](https://github.com/Kathir-2703/FWAD-EXP-8/assets/64436376/15516a0f-368b-47fa-85a9-dd9a90bd2449)

## RESULT:
The program for designing a standard calculator using HTML and CSS is executed successfully.
