# Calculator-Project
<!DOCTYPE html>
            background-color: #4CAF50;
            color: white;
        }
        .equal:hover {
            background-color: #45a049;
        }
        .clear {
            background-color: #f44336;
            color: white;
        }
        .clear:hover {
            background-color: #d32f2f;
        }
    </style>
</head>
<body>
    <div class="calculator">
        <input type="text" id="result" disabled>
        <div class="buttons">
            <button onclick="appendValue('7')">7</button>
            <button onclick="appendValue('8')">8</button>
            <button onclick="appendValue('9')">9</button>
            <button onclick="appendValue('/')">/</button>
            <button onclick="appendValue('4')">4</button>
            <button onclick="appendValue('5')">5</button>
            <button onclick="appendValue('6')">6</button>
            <button onclick="appendValue('')"></button>
            <button onclick="appendValue('1')">1</button>
            <button onclick="appendValue('2')">2</button>
            <button onclick="appendValue('3')">3</button>
            <button onclick="appendValue('-')">-</button>
            <button onclick="appendValue('0')">0</button>
            <button onclick="appendValue('.')">.</button>
            <button onclick="calculate()" class="equal">=</button>
            <button onclick="appendValue('+')">+</button>
            <button onclick="clearResult()" class="clear">C</button>
        </div>
    </div>

    <script>
        function appendValue(value) {
            document.getElementById("result").value += value;
        }

        function calculate() {
            let result = document.getElementById("result").value;
            if (result) {
                document.getElementById("result").value = eval(result);
            }
        }

        function clearResult() {
            document.getElementById("result").value = '';
        }
    </script>
</body>
</html>
