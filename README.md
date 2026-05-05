<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Voting Chamber</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f4f7f6;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }
        .container {
            background: white;
            padding: 2rem;
            border-radius: 15px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
            width: 400px;
            text-align: center;
        }
        h1 {
            color: #2c3e50;
            margin-bottom: 1.5rem;
            border-bottom: 2px solid #3498db;
            padding-bottom: 10px;
        }
        .member-card {
            display: flex;
            justify-content: space-between;
            align-items: center;
            background: #fff;
            padding: 10px 15px;
            margin-bottom: 10px;
            border: 1px solid #ddd;
            border-radius: 8px;
            transition: 0.3s;
        }
        .member-card:hover {
            border-color: #3498db;
            background-color: #f0f9ff;
        }
        .name {
            font-weight: bold;
            font-size: 1.1rem;
            color: #34495e;
        }
        .vote-btn {
            background-color: #3498db;
            color: white;
            border: none;
            padding: 8px 15px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 0.9rem;
        }
        .vote-btn:hover {
            background-color: #2980b9;
        }
        .results {
            margin-top: 20px;
            padding-top: 15px;
            border-top: 1px dashed #ccc;
        }
        .count {
            font-weight: bold;
            color: #e67e22;
        }
    </style>
</head>
<body>

<div class="container">
    <h1>Voting Chamber</h1>
    
    <div id="voting-section">
        <div class="member-card">
            <span class="name">Rudransh Soni</span>
            <button class="vote-btn" onclick="castVote('Rudransh')">Vote</button>
        </div>
        <div class="member-card">
            <span class="name">Rajveer Soni</span>
            <button class="vote-btn" onclick="castVote('Rajveer')">Vote</button>
        </div>
        <div class="member-card">
            <span class="name">Rudra Soni</span>
            <button class="vote-btn" onclick="castVote('Rudra')">Vote</button>
        </div>
        <div class="member-card">
            <span class="name">Tanishka Soni</span>
            <button class="vote-btn" onclick="castVote('Tanishka')">Vote</button>
        </div>
    </div>

    <div class="results">
        <h3>Live Results</h3>
        <p>Rudransh: <span id="count-Rudransh" class="count">0</span></p>
        <p>Rajveer: <span id="count-Rajveer" class="count">0</span></p>
        <p>Rudra: <span id="count-Rudra" class="count">0</span></p>
        <p>Tanishka: <span id="count-Tanishka" class="count">0</span></p>
    </div>
</div>

<script>
    // Vote counts store karne ke liye object
    let votes = {
        Rudransh: 0,
        Rajveer: 0,
        Rudra: 0,
        Tanishka: 0
    };

    function castVote(member) {
        // Count badhana
        votes[member]++;
        
        // UI update karna
        document.getElementById('count-' + member).innerText = votes[member];
        
        // Sweet alert ya simple alert (Optional)
        console.log("Voted for " + member);
    }
</script>

</body>
</html>
w
