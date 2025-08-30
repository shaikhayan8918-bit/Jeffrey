# Jeffrey
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Figma Workflow for Professional Web Designers</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        /* CSS Reset */
        *, *::before, *::after {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        html, body {
            overflow-x: hidden;
            scroll-behavior: smooth;
        }

        body {
            background-color: #0F111A;
            color: #E0E0E0;
            font-family: 'Inter', sans-serif;
            line-height: 1.6;
            -webkit-font-smoothing: antialiased;
            -moz-osx-font-smoothing: grayscale;
        }

        /* Main Container & Layout */
        .container {
            width: 100%;
            max-width: 800px;
            margin: 0 auto;
            padding: 0 20px;
        }

        section {
            padding: 80px 0;
            border-bottom: 1px solid #2a2e3c;
        }

        section:last-of-type {
            border-bottom: none;
        }

        /* Typography */
        h1, h2, h3 {
            font-weight: 700;
            line-height: 1.2;
            color: #FFFFFF;
        }

        h1 {
            font-size: 3rem;
            font-weight: 800;
            letter-spacing: -1.5px;
        }

        h2.fascination-headline {
            font-size: 2.25rem;
            font-weight: 700;
            margin-bottom: 40px;
            text-align: center;
            color: #d1d5db;
        }

        p {
            margin-bottom: 1.25rem;
            font-size: 1.125rem;
            color: #b0b4c3;
            max-width: 650px;
            margin-left: auto;
            margin-right: auto;
        }

        .preheader {
            font-size: 1rem;
            font-weight: 600;
            color: #2DD4BF;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 16px;
        }

        .subheader {
            font-size: 1.25rem;
            max-width: 600px;
            margin: 24px auto 32px;
            color: #b0b4c3;
        }
        
        strong {
            color: #fff;
            font-weight: 600;
        }

        /* Buttons */
        .cta-button {
            display: inline-block;
            background-color: #2DD4BF;
            color: #0F111A;
            font-size: 1.125rem;
            font-weight: 700;
            text-decoration: none;
            padding: 18px 36px;
            border-radius: 8px;
            transition: background-color 0.3s ease, transform 0.3s ease;
            box-shadow: 0 4px 15px rgba(45, 212, 191, 0.2);
        }

        .cta-button:hover {
            background-color: #27bda8;
            transform: translateY(-2px);
        }

        /* Hero Section */
        .hero {
            text-align: center;
            padding: 100px 0;
        }

        .vsl-container {
            margin: 0 auto;
            width: 100%;
            max-width: 720px;
            aspect-ratio: 16 / 9;
            background: #2a2e3c url('https://placehold.co/1280x720/0F111A/E0E0E0?text=Your+Designs,+Perfected') center center/cover;
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            position: relative;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
            margin-bottom: 40px;
        }

        .play-button {
            width: 80px;
            height: 80px;
            background-color: rgba(45, 212, 191, 0.9);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: transform 0.2s ease;
        }
        .vsl-container:hover .play-button {
            transform: scale(1.1);
        }

        .play-button::after {
            content: '';
            display: block;
            width: 0;
            height: 0;
            border-style: solid;
            border-width: 15px 0 15px 25px;
            border-color: transparent transparent transparent #0F111A;
            margin-left: 5px;
        }

        /* Content Sections */
        .problem, .origin, .solution, .product, .offer, .faq {
            text-align: center;
        }
        
        ul.benefits-list {
            list-style: none;
            padding: 0;
            margin: 40px auto;
            text-align: left;
            max-width: 650px;
        }

        ul.benefits-list li {
            font-size: 1.1rem;
            padding: 15px 15px 15px 45px;
            position: relative;
            margin-bottom: 12px;
            background-color: #1a1d29;
            border-radius: 8px;
            border-left: 3px solid #2DD4BF;
        }

        ul.benefits-list li::before {
            content: '✓';
            color: #2DD4BF;
            position: absolute;
            left: 15px;
            top: 50%;
            transform: translateY(-50%);
            font-weight: 700;
            font-size: 1.2rem;
        }
        
        .benefit-feature {
            display: block;
            font-weight: 600;
            color: #fff;
        }
        
        .benefit-emotion {
            color: #b0b4c3;
        }

        /* Offer Section */
        .offer-box {
            background-color: #1a1d29;
            border: 1px solid #2a2e3c;
            border-radius: 12px;
            padding: 40px;
            margin: 40px 0;
        }

        .price-strike {
            text-decoration: line-through;
            color: #777;
            font-size: 1.5rem;
            margin-right: 10px;
        }

        .price-main {
            font-size: 2.5rem;
            font-weight: 800;
            color: #2DD4BF;
        }
        
        .guarantee-box {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 20px;
            margin-top: 40px;
            background-color: #161822;
            padding: 20px;
            border-radius: 8px;
            border: 1px solid #2a2e3c;
            max-width: 500px;
            margin-left: auto;
            margin-right: auto;
        }
        
        .guarantee-icon {
            font-size: 2.5rem;
        }

        .guarantee-text {
            text-align: left;
            font-size: 0.95rem;
            color: #b0b4c3;
            margin: 0;
        }
        .guarantee-text strong {
            color: #fff;
        }

        /* FAQ Section */
        .faq-item {
            background-color: #1a1d29;
            border-radius: 8px;
            margin-bottom: 12px;
            text-align: left;
        }

        .faq-question {
            padding: 20px;
            font-weight: 600;
            cursor: pointer;
            position: relative;
            color: #fff;
        }
        
        .faq-question::after {
            content: '+';
            position: absolute;
            right: 20px;
            font-size: 1.5rem;
            transition: transform 0.3s;
        }

        .faq-answer {
            max-height: 0;
            overflow: hidden;
            padding: 0 20px;
            transition: max-height 0.5s ease, padding 0.5s ease;
        }
        
        .faq-answer p {
            padding-bottom: 20px;
            margin-bottom: 0;
            font-size: 1rem;
        }

        .faq-item.active .faq-question::after {
            transform: rotate(45deg);
        }

        .faq-item.active .faq-answer {
            max-height: 200px;
            padding-top: 0px;
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            h1 {
                font-size: 2.5rem;
            }
            h2.fascination-headline {
                font-size: 1.8rem;
            }
            section {
                padding: 60px 0;
            }
            .hero {
                padding: 60px 0;
            }
            .guarantee-box {
                flex-direction: column;
                text-align: center;
            }
            .guarantee-text {
                text-align: center;
            }
        }

    </style>
</head>
<body>

    <!-- HERO SECTION -->
    <section class="hero">
        <div class="container">
            <p class="preheader">For Freelance & Agency Web Designers</p>
            <h1>The A-to-Z Figma Workflow That Turns Messy Ideas Into Premium, High-Value Websites</h1>
            <p class="subheader">And do it without the endless revisions, the confusing handoffs, or that nagging voice asking if your designs are “good enough.”</p>
            <div class="vsl-container" aria-label="Course video placeholder">
                <div class="play-button"></div>
            </div>
            <a href="#offer" class="cta-button">Pre-Enroll Now & Save $200</a>
        </div>
    </section>

    <!-- PROBLEM IDENTIFICATION -->
    <section class="problem">
        <div class="container">
            <h2 class="fascination-headline">Does Your Design Process Feel More Like a Coin Toss?</h2>
            <p>One minute, you’re staring at a blank Figma canvas, feeling the pressure mount.</p>
            <p>The next, you’ve cobbled something together, but the logic is… shaky. The spacing is inconsistent. The handoff to WordPress feels like you’re trying to fit a square peg in a round hole.</p>
            <p>You’ve watched the YouTube tutorials. You bought that cheap course. But nothing sticks. Nothing gives you a repeatable <strong>system.</strong></p>
            <p>So you’re stuck.</p>
            <p>Stuck undercharging because you don't feel confident in your process. Stuck in that feast-or-famine cycle, praying the next client doesn't ask for something you can’t quite deliver.</p>
            <p>Stuck feeling like an imposter in a market full of designers who just seem to… get it.</p>
            <p>What if the problem isn’t your talent? What if it’s just your workflow?</p>
        </div>
    </section>

    <!-- ORIGIN STORY -->
    <section class="origin">
        <div class="container">
            <h2 class="fascination-headline">Generic Figma Courses Are Built for UI Designers—Not Web Builders.</h2>
            <p>That’s the core of the issue.</p>
            <p>Most Figma training out there is made for people designing mobile apps or complex software. They teach you about tools, but not about the actual job of building a real-world website in Elementor, Bricks, or Breakdance.</p>
            <p>They don’t show you how to build a design system that actually speeds up your development… instead of slowing it down.</p>
            <p>They don’t give you a battle-tested process for going from client brief to pixel-perfect WordPress site, every single time.</p>
            <p>We saw countless talented web designers hitting this exact wall. Their building skills were solid, but their design process was costing them time, money, and confidence.</p>
            <p>They were winging it. And it was keeping them from the clients and projects they deserved.</p>
            <p>So, we built the system we wished existed. One made by web designers, for web designers.</p>
        </div>
    </section>

    <!-- SOLUTION REVELATION -->
    <section class="solution">
        <div class="container">
            <h2 class="fascination-headline">A Repeatable System for Calm, Confident, & Profitable Web Design</h2>
            <p>This isn't about learning a few more Figma tricks. It’s about installing a complete, end-to-end operational workflow.</p>
            <p>A system that moves you from confused clicking to intentional creation. From freelancer to creative director.</p>
            <p>It’s built on a simple premise: a great website isn't just built in WordPress. It's born in Figma, with a clear, logical, and scalable process.</p>
            <p>Here’s what that looks like:</p>
            <ul class="benefits-list">
                <li>
                    <span class="benefit-feature">111+ Detailed, Step-by-Step Lessons</span>
                    <span class="benefit-emotion">Go from a blank page to a client-ready mockup, knowing exactly what to do next. You’ll feel the anxiety melt away and be replaced by calm control.</span>
                </li>
                <li>
                    <span class="benefit-feature">A Full Design System You Can Reuse Forever</span>
                    <span class="benefit-emotion">Stop making the same five buttons over and over. Build once, then deploy your system across projects in minutes, making you look like a seasoned pro.</span>
                </li>
                 <li>
                    <span class="benefit-feature">17+ Real-World Design Challenges</span>
                    <span class="benefit-emotion">Move from theory to practice. Finish each module with a tangible skill you've already proven you can execute, giving you undeniable confidence in your abilities.</span>
                </li>
                <li>
                    <span class="benefit-feature">Figma-to-Builder Mini-Courses (Elementor, Bricks, Breakdance)</span>
                    <span class="benefit-emotion">Finally bridge the gap. See exactly how your Figma designs translate into a clean, fast-loading WordPress site, ending the guesswork for good.</span>
                </li>
            </ul>
        </div>
    </section>

    <!-- PRODUCT INTRODUCTION -->
    <section class="product">
        <div class="container">
            <h2 class="fascination-headline">Introducing: The Complete Figma for Web Designers Course</h2>
            <p>This is the definitive workflow for WordPress designers who want to build better websites, faster, and charge more for them.</p>
            <p>It’s a curriculum, a community, and a complete career toolkit, all in one place.</p>
            <p>Forget the disjointed YouTube videos. Forget the app-focused tutorials that don’t understand your job.</p>
            <p>This is the only system that connects every dot: from mastering Figma's fundamentals like auto-layout and components, to building high-fidelity mockups, to handing off a flawless design that your clients—and your developer-self—will absolutely love.</p>
            <p>This entire system is delivered via a private Circle community, where you get feedback, ask questions, and learn alongside designers on the exact same path as you.</p>
        </div>
    </section>
    
    <!-- OFFER STRUCTURE -->
    <section id="offer" class="offer">
        <div class="container">
            <h2 class="fascination-headline">Get The Complete System Today & Save $200</h2>
            <div class="offer-box">
                <p>Lifetime access to everything, including all future updates:</p>
                <ul class="benefits-list">
                    <li>111 Detailed Lessons</li>
                    <li>17+ Design Challenges</li>
                    <li>3 Bonus Figma-to-WordPress Mini-Courses</li>
                    <li>Reusable Templates & Design Systems</li>
                    <li>Private Circle Community Access</li>
                    <li>Certificate of Completion</li>
                </ul>
                <p style="margin-top: 30px;">Pre-Enrollment Price:</p>
                <div>
                    <span class="price-strike">$499</span>
                    <span class="price-main">$299 USD</span>
                </div>
                <p style="font-size: 1rem; color: #b0b4c3; margin-top: 10px;">This is a one-time payment. No subscriptions.</p>
                <a href="#" class="cta-button" style="margin-top: 20px;">Claim My $200 Discount Now</a>
                <div class="guarantee-box">
                    <div class="guarantee-icon">✓</div>
                    <div class="guarantee-text">
                        <strong>Our 7-Day, No-Questions-Asked Guarantee.</strong>
                        <p>Go through the first modules. If you don't feel it's already clearing up your workflow, just let us know within 7 days for a full, prompt refund. Simple as that.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- FAQ SECTION -->
    <section class="faq">
        <div class="container">
            <h2 class="fascination-headline">Your Questions, Answered.</h2>
            <div class="faq-container">
                <div class="faq-item">
                    <div class="faq-question">Is this for beginners?</div>
                    <div class="faq-answer">
                        <p>Yes. If you're a web designer who's new to Figma or feels intimidated by it, this is the perfect starting point. We begin with the absolute fundamentals and build from there. No prior Figma expertise is needed.</p>
                    </div>
                </div>
                <div class="faq-item">
                    <div class="faq-question">I'm already using Figma. Is this still for me?</div>
                    <div class="faq-answer">
                        <p>Most likely. This course isn't just about which buttons to click. It's about a professional, repeatable workflow. If you lack a consistent process for design systems, client handoffs, and builder-specific design, you will find immense value here.</p>
                    </div>
                </div>
                <div class="faq-item">
                    <div class="faq-question">How long will it take to go through the course?</div>
                    <div class="faq-answer">
                        <p>It's a self-paced course, so you can move as quickly or as slowly as you need. With over 111 lessons, many designers spend a few weeks to a month to fully absorb the material and complete the challenges. But you have lifetime access, so there's no rush.</p>
                    </div>
                </div>
                 <div class="faq-item">
                    <div class="faq-question">What if I use a different WordPress builder?</div>
                    <div class="faq-answer">
                        <p>The core Figma workflow and design system principles taught are universal and apply to any builder. The bonus mini-courses cover Elementor, Bricks, and Breakdance specifically, but the core system will make you a better designer regardless of your final tool.</p>
                    </div>
                </div>
            </div>
            <a href="#offer" class="cta-button" style="margin-top: 50px;">Start Building Better Websites Today</a>
        </div>
    </section>

    <script>
        // Simple FAQ Accordion
        const faqItems = document.querySelectorAll('.faq-item');
        faqItems.forEach(item => {
            const question = item.querySelector('.faq-question');
            question.addEventListener('click', () => {
                const isActive = item.classList.contains('active');
                faqItems.forEach(i => i.classList.remove('active'));
                if (!isActive) {
                    item.classList.add('active');
                }
            });
        });

        // Smooth Scroll for CTA buttons
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>
