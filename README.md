<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>PUZZLE II</title>

<style>
    body {
        margin: 0;
        min-height: 100vh;
        display: flex;
        align-items: center;
        justify-content: center;
        background: #090909;
        color: #eee;
        font-family: Georgia, serif;
    }

    .box {
        width: min(90%, 520px);
        text-align: center;
    }

    h1 {
        letter-spacing: 6px;
        font-size: 22px;
        font-weight: normal;
    }

    p {
        color: #888;
        font-family: monospace;
        font-size: 13px;
    }

    .black-box {
        margin: 35px auto 0;
        padding: 28px;
        background: #000;
        border: 1px solid #222;
        box-shadow: 0 0 25px rgba(0,0,0,.8);
    }

    input {
        width: 90%;
        box-sizing: border-box;
        padding: 14px;
        background: #111;
        border: 1px solid #333;
        color: white;
        text-align: center;
        font-family: monospace;
        outline: none;
    }

    button {
        margin-top: 12px;
        padding: 11px 25px;
        background: #111;
        border: 1px solid #444;
        color: #aaa;
        cursor: pointer;
    }

    button:hover {
        color: white;
        border-color: #777;
    }

    #result {
        margin-top: 20px;
        min-height: 20px;
        font-family: monospace;
    }
</style>
</head>

<body>

<div class="box">

    <h1>PUZZLE II</h1>

    <p>the previous answer is required</p>

    <div class="black-box">

        <div style="margin-bottom:15px;color:#666;">
            PUT PREVIOUS ANSWER HERE
        </div>

        <input
            id="answer"
            placeholder="none"
            autocomplete="off"
        >

        <br>

        <button onclick="checkAnswer()">
            ENTER
        </button>

        <div id="result">none</div>

    </div>

</div>

<script>

function checkAnswer() {

    const input =
        document.getElementById("answer")
        .value
        .trim()
        .toLowerCase();

    const result =
        document.getElementById("result");

    // PLACEHOLDER FOR NOW
    // The real "Wasted"
