<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Devi Kalyani - Web Developer</title>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <style>
        /* General Styles */
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            color: #fff;
            background: #121212;
            text-align: center;
        }

        /* Header */
        header {
            background: #1e90ff;  /* Solid Blue */
            padding: 50px;
        }
        header h1 {
            margin: 0;
            font-size: 2.8em;
        }
        header p {
            font-size: 1.4em;
            margin-top: 10px;
        }

        /* Content Box */
        .container {
            max-width: 900px;
            margin: 40px auto;
            padding: 20px;
            background: rgba(30, 30, 30, 0.9);
            box-shadow: 0px 0px 15px rgba(30, 144, 255, 0.3);
            border-radius: 8px;
            text-align: left;
        }

        /* About Section */
        .about {
            text-align: center;
            margin-bottom: 30px;
        }
        .about h2 {
            color: #ffa500;
            font-size: 2em;
        }
        .about p {
            font-size: 1.2em;
            line-height: 1.6;
            color: #ddd;
        }

        /* Skills Section */
        .skills {
            text-align: center;
            padding: 20px;
        }
        .skills h2 {
            color: #ffa500;
            font-size: 2em;
        }

        /* Charts */
        .charts-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 30px;
            padding: 20px;
        }
        .chart-box {
            width: 45%;
            background: rgba(40, 40, 40, 0.8);
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0px 0px 10px rgba(255, 165, 0, 0.5);
        }

        /* Footer */
        footer {
            margin-top: 30px;
            padding: 20px;
            background: #1e90ff;  /* Solid Blue */
            color: white;
        }

        @media (max-width: 768px) {
            .chart-box {
                width: 100%;
            }
        }
    </style>
</head>
<body>

    <header>
        <h1>Devi Kalyani</h1>
        <p>Web Developer & Designer</p>
    </header>

    <div class="container">
        <!-- About Section -->
        <div class="about">
            <h2>About Me</h2>
            <p>Hello! I'm *Kalyani, a passionate web developer and designer with over **2 years of experience* in creating beautiful and functional websites.  
               I specialize in *front-end development* and have a keen eye for design.</p>
        </div>

        <!-- Skills Section -->
        <div class="skills">
            <h2>My Skills</h2>
        </div>

        <!-- Charts Section -->
        <div class="charts-container">
            <div class="chart-box">
                <canvas id="barChart"></canvas>
            </div>
            <div class="chart-box">
                <canvas id="pieChart"></canvas>
            </div>
        </div>
    </div>

    <footer>
        <p>© 2025 Devi Kalyani | Web Developer & Designer</p>
    </footer>

    <script>
        // Bar Chart with Multiple Colors
        var barCtx = document.getElementById('barChart').getContext('2d');
        var barChart = new Chart(barCtx, {
            type: 'bar',
            data: {
                labels: ['HTML & CSS', 'JavaScript & jQuery', 'Responsive Design', 'UI/UX Design', 'Git'],
                datasets: [{
                    label: 'Skill Proficiency (%)',
                    data: [90, 80, 85, 75, 70],
                    backgroundColor: [
                        '#ff4500',  // Orange Red
                        '#32cd32',  // Lime Green
                        '#ff1493',  // Deep Pink
                        '#1e90ff',  // Dodger Blue
                        '#9400d3'   // Dark Violet
                    ],
                    borderColor: '#fff',
                    borderWidth: 1
                }]
            },
            options: {
                responsive: true,
                scales: {
                    y: {
                        beginAtZero: true,
                        ticks: { color: '#fff' }
                    },
                    x: { ticks: { color: '#fff' } }
                },
                plugins: { legend: { labels: { color: '#fff' } } }
            }
        });

        // Pie Chart with Multiple Colors
        var pieCtx = document.getElementById('pieChart').getContext('2d');
        var pieChart = new Chart(pieCtx, {
            type: 'pie',
            data: {
                labels: ['HTML & CSS', 'JavaScript & jQuery', 'Responsive Design', 'UI/UX Design', 'Git'],
                datasets: [{
                    label: 'Skill Distribution',
                    data: [90, 80, 85, 75, 70],
                    backgroundColor: [
                        '#ff4500',  // Orange Red
                        '#32cd32',  // Lime Green
                        '#ff1493',  // Deep Pink
                        '#1e90ff',  // Dodger Blue
                        '#9400d3'   // Dark Violet
                    ],
                    borderColor: '#fff',
                    borderWidth: 1
                }]
            },
            options: {
                responsive: true,
                plugins: { legend: { labels: { color: '#fff' } } }
            }
        });
    </script>

</body>
</html>
