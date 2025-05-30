# mango-juice-form
Mango juice sensory evaluation form

<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Sensory Evaluation Form - Mango Juice</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 40px;
        }
        h1, h2 {
            text-align: center;
        }
        .presenter {
            text-align: center;
            font-size: 1.2em;
            margin-bottom: 30px;
        }
        form {
            max-width: 700px;
            margin: auto;
        }
        label {
            font-weight: bold;
            margin-top: 15px;
            display: block;
        }
        select, textarea {
            width: 100%;
            padding: 8px;
            font-size: 1em;
            margin-bottom: 20px;
        }
        button {
            padding: 10px 20px;
            font-size: 1em;
            margin-top: 20px;
        }
        .scale-guide {
            background-color: #f9f9f9;
            border-left: 5px solid #2196F3;
            padding: 10px 20px;
            margin: 20px 0;
        }
    </style>
</head>
<body>

    <h1>Sensory Evaluation Form</h1>
    <h2>Mango Juice</h2>

    <div class="presenter">
        <p><strong>Presenter:</strong> Anwaar Ahmad</p>
        <p><strong>Roll Number:</strong> 2024-FSTR-005</p>
    </div>

    <div class="scale-guide">
        <p><strong>5-point Hedonic Scale:</strong></p>
        <ul>
            <li>5 – Like extremely</li>
            <li>4 – Like moderately</li>
            <li>3 – Neither like nor dislike</li>
            <li>2 – Dislike moderately</li>
            <li>1 – Dislike extremely</li>
        </ul>
    </div>

    <form id="evaluationForm">
        <label for="color">Color (1–5):</label>
        <select id="color" name="color">
            <option value="5">5 – Like extremely</option>
            <option value="4">4 – Like moderately</option>
            <option value="3">3 – Neither like nor dislike</option>
            <option value="2">2 – Dislike moderately</option>
            <option value="1">1 – Dislike extremely</option>
        </select>

        <label for="taste">Taste (1–5):</label>
        <select id="taste" name="taste">
            <option value="5">5 – Like extremely</option>
            <option value="4">4 – Like moderately</option>
            <option value="3">3 – Neither like nor dislike</option>
            <option value="2">2 – Dislike moderately</option>
            <option value="1">1 – Dislike extremely</option>
        </select>

        <label for="aroma">Aroma (1–5):</label>
        <select id="aroma" name="aroma">
            <option value="5">5 – Like extremely</option>
            <option value="4">4 – Like moderately</option>
            <option value="3">3 – Neither like nor dislike</option>
            <option value="2">2 – Dislike moderately</option>
            <option value="1">1 – Dislike extremely</option>
        </select>

        <label for="texture">Texture (1–5):</label>
        <select id="texture" name="texture">
            <option value="5">5 – Like extremely</option>
            <option value="4">4 – Like moderately</option>
            <option value="3">3 – Neither like nor dislike</option>
            <option value="2">2 – Dislike moderately</option>
            <option value="1">1 – Dislike extremely</option>
        </select>

        <label for="overall">Overall Acceptability (1–5):</label>
        <select id="overall" name="overall">
            <option value="5">5 – Like extremely</option>
            <option value="4">4 – Like moderately</option>
            <option value="3">3 – Neither like nor dislike</option>
            <option value="2">2 – Dislike moderately</option>
            <option value="1">1 – Dislike extremely</option>
        </select>

        <label for="comments">Additional Comments:</label>
        <textarea id="comments" name="comments" rows="4"></textarea>

        <button type="button" onclick="downloadForm()">Download Evaluation</button>
    </form>

    <script>
        function downloadForm() {
            const color = document.getElementById("color").value;
            const taste = document.getElementById("taste").value;
            const aroma = document.getElementById("aroma").value;
            const texture = document.getElementById("texture").value;
            const overall = document.getElementById("overall").value;
            const comments = document.getElementById("comments").value;

            const content = `
Sensory Evaluation Form - Mango Juice

Presenter: Anwaar Ahmad
Roll Number: 2024-FSTR-005

Using 5-point Hedonic Scale:
5 – Like extremely
4 – Like moderately
3 – Neither like nor dislike
2 – Dislike moderately
1 – Dislike extremely

Color: ${color}
Taste: ${taste}
Aroma: ${aroma}
Texture: ${texture}
Overall Acceptability: ${overall}

Additional Comments:
${comments}
`;

            const blob = new Blob([content], { type: "text/plain" });
            const url = URL.createObjectURL(blob);
            const link = document.createElement("a");
            link.href = url;
            link.download = "Mango_Juice_Evaluation.txt";
            link.click();
            URL.revokeObjectURL(url);
        }
    </script>

</body>
</html>
 
