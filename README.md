<!DOCTYPE html>
<html lang="tl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>EIM & ICT Tech-School Portal</title>
    <style>
        /* --- CSS STYLING --- */
        :root {
            --primary-color: #1e3a8a; /* Deep Blue */
            --electric-color: #eab308; /* Yellow */
            --ict-color: #06b6d4; /* Cyan */
            --dark-bg: #0f172a;
            --light-bg: #f8fafc;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: var(--light-bg);
            color: #334155;
        }

        /* Header & Navigation */
        header {
            background-color: var(--primary-color);
            color: white;
            padding: 1.5rem;
            text-align: center;
            box-shadow: 0 4px 6px -1px rgba(0,0,0,0.1);
        }

        header h1 {
            font-size: 2rem;
            margin-bottom: 0.5rem;
        }

        /* Main Layout */
        .container {
            max-width: 1200px;
            margin: 2rem auto;
            padding: 0 1rem;
        }

        .welcome-text {
            text-align: center;
            margin-bottom: 3rem;
        }

        .welcome-text h2 {
            font-size: 1.8rem;
            color: var(--primary-color);
        }

        /* Hub Cards Grid */
        .hub-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-bottom: 3rem;
        }

        .card {
            background: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 10px 15px -3px rgba(0,0,0,0.05);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            display: flex;
            flex-direction: column;
        }

        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 25px -5px rgba(0,0,0,0.1);
        }

        .card-header {
            padding: 1.5rem;
            color: white;
            font-size: 1.5rem;
            font-weight: bold;
            text-align: center;
        }

        .electric-header {
            background-color: var(--electric-color);
            color: #1e293b;
        }

        .ict-header {
            background-color: var(--ict-color);
        }

        .card-body {
            padding: 1.5rem;
            flex-grow: 1;
        }

        .card-body ul {
            list-style-type: none;
            margin-top: 1rem;
        }

        .card-body li {
            padding: 0.5rem 0;
            border-bottom: 1px solid #f1f5f9;
        }

        .card-body li::before {
            content: "🔹 ";
        }

        .card-footer {
            padding: 1.5rem;
            background-color: #f8fafc;
            text-align: center;
        }

        /* Interactive Button */
        .btn {
            display: inline-block;
            padding: 0.75rem 1.5rem;
            border: none;
            border-radius: 6px;
            font-weight: bold;
            cursor: pointer;
            text-decoration: none;
            transition: background 0.2s;
            width: 100%;
        }

        .btn-electric {
            background-color: var(--electric-color);
            color: #1e293b;
        }

        .btn-electric:hover {
            background-color: #ca8a04;
        }

        .btn-ict {
            background-color: var(--ict-color);
            color: white;
        }

        .btn-ict:hover {
            background-color: #0891b2;
        }

        /* Footer */
        footer {
            background-color: var(--dark-bg);
            color: #94a3b8;
            text-align: center;
            padding: 1.5rem;
            margin-top: 4rem;
            font-size: 0.9rem;
        }
    </style>
</head>
<body>

    <!-- Header Section -->
    <header>
        <h1>⚡ TechVoc Digital Portal 💻</h1>
        <p>Mataas na Paaralan ng Agham at Teknolohiya</p>
    </header>

    <!-- Main Content -->
    <div class="container">
        <div class="welcome-text">
            <h2>Pumili ng Iyong Linya ng Pag-aaral</h2>
            <p>I-click ang hub ng iyong strand para ma-access ang mga online learning simulators at modules.</p>
        </div>

        <div class="hub-grid">
            <!-- Electrician (EIM) Card -->
            <div class="card">
                <div class="card-header electric-header">
                    ⚡ Electrician Hub (EIM)
                </div>
                <div class="card-body">
                    <p>Dito matututunan ang tamang house wiring, industrial motor controls, at kaligtasan sa paghawak ng kuryente.</p>
                    <ul>
                        <li>Virtual House Wiring Simulator</li>
                        <li>TESDA NC II Mock Exam Reviewer</li>
                        <li>OHS Safety Signs & Symbols Quiz</li>
                    </ul>
                </div>
                <div class="card-footer">
                    <button class="btn btn-electric" onclick="openHub('Electrician')">Pumasok sa EIM Hub</button>
                </div>
            </div>

            <!-- ICT Card -->
            <div class="card">
                <div class="card-header ict-header">
                    💻 ICT Hub (Computer Systems)
                </div>
                <div class="card-body">
                    <p>Dito nakapokus ang pag-aaral sa software development, computer networking, hardware troubleshooting, at web design.</p>
                    <ul>
                        <li>Interactive Coding Sandbox (HTML/CSS)</li>
                        <li>Cisco Networking Basics & IP Addressing</li>
                        <li>PC Assembly Diagnostic Tree</li>
                    </ul>
                </div>
                <div class="card-footer">
                    <button class="btn btn-ict" onclick="openHub('ICT')">Pumasok sa ICT Hub</button>
                </div>
            </div>
        </div>
    </div>

    <!-- Footer Section -->
    <footer>
        <p>&copy; 2026 TechVoc School Portal. Lahat ng Karapatan ay Rezervado.</p>
    </footer>

    <!-- --- JAVASCRIPT --- -->
    <script>
        function openHub(hubName) {
            // Sa totoong website, pwede mo itong palitan ng `window.location.href = 'electrician.html'`
            alert("Papunta ka na sa " + hubName + " Hub! Dito mo makikita ang mga simulators at pagsusulit para sa iyong strand.");
        }
    </script>
</body>
</html>
