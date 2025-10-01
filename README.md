# warin18.github.io
<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Online Shopping vs. Community</title>
    <style>
        /* Global Reset and Layout */
        body { font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; margin: 0; overflow: hidden; display: flex; justify-content: center; align-items: center; height: 100vh; background-color: #f4f4f4; }
        .slide-container { width: 100vw; height: 100vh; position: relative; }
        .slide {
            flex-shrink: 0; width: 100vw; height: 100vh; display: none; flex-direction: column; 
            justify-content: center; align-items: center; text-align: center; padding: 5%;
            box-sizing: border-box; color: #333; position: absolute; top: 0; left: 0;
            transition: transform 0.5s ease-in-out;
        }
        .slide.active { display: flex; transform: translateX(0); }
        .slide:not(.active) { transform: translateX(100%); }

        /* Typography and Styling */
        h1 { font-size: 3.8em; color: #007bff; margin-bottom: 0.2em; }
        h2 { font-size: 2.2em; color: #555; margin-top: 0.5em; }
        p, li { font-size: 1.5em; max-width: 80%; line-height: 1.4; }
        .data { font-size: 4.5em; font-weight: bold; margin: 0.1em 0; }
        .feature { font-size: 1.7em; margin: 0.8em 0; list-style: none; padding: 0; }
        .highlight-g { color: #2ecc71; font-weight: bold; } /* Green for Growth */
        .highlight-r { color: #e74c3c; font-weight: bold; } /* Red for Risk */

        /* Custom Styles for Specific Slides (Color Coding) */
        .slide:nth-child(1) { background-color: #e6f7ff; } 
        .slide:nth-child(3) { background-color: #e8f8f5; } 
        .slide:nth-child(4) { background-color: #fae3e3; } 
        .slide:nth-child(6) { background-color: #fcf3cf; } 
    </style>
</head>
<body>

<div class="slide-container">
    <div class="slide active">
        <h1>THE DIGITAL DILEMMA</h1>
        <h2>Online Shopping vs. Local Communities</h2>
        <p style="font-size:2.5em;">**DOES CONVENIENCE DESTROY COMMUNITY?**<br>(ความสะดวกสบาย ทำลายชุมชนจริงหรือ?)</p>
        <p style="font-size:1.2em; margin-top: 1.5em;">*Key Concept: Creative Destruction & Neutral Guide*</p>
    </div>

    <div class="slide">
        <h1>THE CORE CONFLICT</h1>
        <p style="font-size:2.5em;">The economic efficiency of <span class="highlight-g">LOW PRICES</span></p>
        <p style="font-size:3em; margin: 0.5em 0;">$\leftrightarrow$</p>
        <p style="font-size:2.5em;">Clashes with the stability of <span class="highlight-r">LOCAL JOBS & TAX BASE</span></p>
        <p style="font-size:1.2em; margin-top: 3em;">*We must explore both sides with equal enthusiasm.*</p>
    </div>

    <div class="slide">
        <h1>PERSPECTIVE A: PROGRESS & INCLUSION</h1>
        <ul class="feature">
            <li><span class="highlight-g">ACCESS:</span> Unprecedented reach for the Elderly/Remote Areas. (Source 1)</li>
            <li><span class="highlight-g">EMPOWERMENT:</span> Rural Creamery saw <span class="data" style="color:#2ecc71;">+150%</span> Sales Growth. (Source A)</li>
            <li><span class="highlight-g">JOBS:</span> Job <span style="font-weight: bold;">Transition</span> to higher-paying Logistics & Tech roles. (Source 2)</li>
        </ul>
    </div>

    <div class="slide">
        <h1>PERSPECTIVE B: THE FINANCIAL & SOCIAL COST</h1>
        <p style="font-size:2.2em;">Immediate Economic Damage is measurable:</p>
        <p class="data"><span style="color:#e74c3c;">-4%</span></p>
        <p style="font-size:1.8em; margin-bottom: 2em;">Sales Drop for local stores near E-commerce centers. (Source 2)</p>
        <p class="warning">Losing <span style="font-weight: bold;">Municipal Funding</span> for Schools & Roads. (Source 3)</p>
    </div>

    <div class="slide">
        <h1>EROSION OF THE SOCIAL FABRIC</h1>
        <p style="font-size:2.2em;">Physical Stores are our **Social Anchors**.</p>
        <p class="feature">
            The loss removes a **Community Hub**.<br>
            Leads to <span class="highlight-r">negative social consequences</span> (Loss of belonging and interaction).
        </p>
        <p style="font-size:1.5em; color: #555;">(Example: The loss of a local bookstore removes a core community hub.)</p>
    </div>

    <div class="slide">
        <h1>THE SOLUTION: OMNI-CHANNEL</h1>
        <p style="font-size:2em;">The Future is blending Digital + Physical.</p>
        <p style="font-size:2.8em; font-weight: bold;">
            <span class="warning">TRANSACTION</span> 
            <span style="font-size:1.5em; color:#333;"> $\rightarrow$ </span> 
            <span class="highlight-g">EXPERIENCE</span>
        </p>
        <ul class="feature" style="margin-top: 1.5em;">
            <li><span class="highlight-g">Strategy:</span> Companies like Nike & Target use <span style="font-weight: bold;">BOPIS</span> (Buy Online, Pick Up In Store). (Source B)</li>
        </ul>
    </div>

    <div class="slide">
        <h1>WRAP UP</h1>
        <p style="font-size:2.5em;">The dilemma: <span class="highlight-g">Efficiency</span> VS <span class="highlight-r">Community</span>.</p>
        <p class="data" style="color:#007bff; font-size:4em;">The Balance Depends on Us.</p>
        <p style="font-size:1.8em; max-width: 80%;">
            Our spending choices determine the value we place on the digital click versus the **physical heart of our community**.
        </p>
        <p style="font-size:1.5em; margin-top: 3em;">THANK YOU.</p>
    </div>
</div>

<script>
    const slides = document.querySelectorAll('.slide');
    let currentSlide = 0;

    function showSlide(index) {
        slides.forEach((slide, i) => {
            slide.classList.remove('active');
            if (i === index) {
                slide.classList.add('active');
            }
        });
        currentSlide = index;
    }

    function nextSlide() {
        if (currentSlide < slides.length - 1) {
            showSlide(currentSlide + 1);
        }
    }

    function prevSlide() {
        if (currentSlide > 0) {
            showSlide(currentSlide - 1);
        }
    }

    document.addEventListener('keydown', (e) => {
        if (e.key === 'ArrowRight' || e.key === ' ' || e.key === 'Enter') {
            e.preventDefault(); 
            nextSlide();
        } else if (e.key === 'ArrowLeft' || e.key === 'Backspace') {
            e.preventDefault(); 
            prevSlide();
        }
    });

    // Initialize the first slide
    showSlide(currentSlide);
</script>

</body>
</html>
