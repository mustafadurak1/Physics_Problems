<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Mechanics I - Relative Velocity Visualization</title>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/1.4.0/p5.js"></script>
    <style>
        body { font-family: sans-serif; display: flex; flex-direction: column; align-items: center; background: #f0f2f5; }
        .controls { background: white; padding: 20px; border-radius: 8px; box-shadow: 0 2px 10px rgba(0,0,0,0.1); margin: 20px; }
        .data { margin-top: 10px; font-weight: bold; color: #1a73e8; }
        canvas { border-radius: 8px; border: 2px solid #ddd; }
    </style>
</head>
<body>
    <h2>Problem 5: Boat Crossing a River</h2>
    <div class="controls">
        <label>River Speed (East): </label>
        <input type="range" id="riverSpeed" min="0" max="4" step="0.1" value="2">
        <br><br>
        <label>Boat Speed (Still Water): </label>
        <input type="range" id="boatSpeed" min="2.1" max="8" step="0.1" value="5">
        <div class="data" id="stats"></div>
    </div>

    <script>
        let boatY = 350;
        let angle;
        let v_net;

        function setup() {
            createCanvas(600, 400);
        }

        function draw() {
            background(240);
            
            // Draw River
            fill(173, 216, 230);
            noStroke();
            rect(0, 50, 600, 300);
            
            // Draw Banks
            fill(139, 69, 19);
            rect(0, 0, 600, 50);
            rect(0, 350, 600, 50);

            let v_r = parseFloat(document.getElementById('riverSpeed').value);
            let v_b = parseFloat(document.getElementById('boatSpeed').value);

            // Calculation
            angle = asin(v_r / v_b);
            v_net = v_b * cos(angle);
            let angleDeg = (angle * 180 / PI).toFixed(1);

            document.getElementById('stats').innerHTML = 
                `Heading Angle: ${angleDeg}° West of North <br> Resultant North Speed: ${v_net.toFixed(2)} m/s`;

            // Draw Vector Diagram (Static Reference)
            push();
            translate(50, 300);
            stroke(0); strokeWeight(2);
            line(0,0, 0, -v_net * 20); // Resultant
            stroke(255, 0, 0);
            line(0,0, v_r * 20, 0); // River
            stroke(0, 128, 0);
            line(v_r * 20, 0, 0, -v_net * 20); // Boat Heading
            pop();

            // Animate Boat
            boatY -= (v_net / 2);
            if (boatY < 50) boatY = 350;

            // Draw the Boat
            push();
            translate(300, boatY);
            rotate(-angle);
            fill(255, 100, 0);
            stroke(0);
            triangle(-10, 15, 10, 15, 0, -15); // Simple boat shape
            pop();
            
            // Water Flow Lines
            stroke(255, 255, 255, 150);
            for(let i=0; i<5; i++) {
                let y = 100 + i*50;
                line((frameCount*v_r)%600, y, (frameCount*v_r)%600 + 30, y);
            }
        }
    </script>
</body>
</html>
