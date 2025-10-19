<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Table Setting and Customer Service Quiz</title>
    <style>
        body {
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            margin: 0;
            padding: 0;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100%;
        }
        
        html, body {
            height: 100%;
        }
        
        .container {
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
            min-height: 100%;
            display: flex;
            flex-direction: column;
        }
        
        .card {
            background: white;
            border-radius: 15px;
            padding: 30px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
            margin-bottom: 20px;
        }
        
        .dashboard {
            background: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);
            color: white;
            text-align: center;
        }
        
        .profile-info {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
            margin-top: 20px;
        }
        
        .info-item {
            background: rgba(255,255,255,0.2);
            padding: 15px;
            border-radius: 10px;
            backdrop-filter: blur(10px);
        }
        
        .timer {
            font-size: 2em;
            font-weight: bold;
            color: #ff6b6b;
            text-align: center;
            margin: 20px 0;
            padding: 15px;
            background: #fff3cd;
            border-radius: 10px;
            border: 2px solid #ffeaa7;
        }
        
        .question-card {
            position: relative;
            overflow: hidden;
        }
        
        .question-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 25px;
            padding-bottom: 15px;
            border-bottom: 2px solid #e9ecef;
        }
        
        .question-number {
            background: #667eea;
            color: white;
            padding: 10px 20px;
            border-radius: 25px;
            font-weight: bold;
        }
        
        .question-text {
            font-size: 1.3em;
            font-weight: 600;
            margin-bottom: 25px;
            color: #2d3436;
            line-height: 1.5;
        }
        
        .choices {
            display: grid;
            gap: 15px;
        }
        
        .choice {
            padding: 18px 25px;
            border: 2px solid #e9ecef;
            border-radius: 12px;
            cursor: pointer;
            transition: all 0.3s ease;
            background: #f8f9fa;
            font-size: 1.1em;
        }
        
        .choice:hover {
            border-color: #667eea;
            background: #f0f3ff;
            transform: translateY(-2px);
        }
        
        .choice.selected {
            background: #667eea;
            color: white;
            border-color: #667eea;
        }
        
        .choice.correct {
            background: #00b894;
            border-color: #00b894;
            color: white;
        }
        
        .choice.incorrect {
            background: #e17055;
            border-color: #e17055;
            color: white;
        }
        
        .btn {
            padding: 15px 30px;
            border: none;
            border-radius: 8px;
            font-size: 1.1em;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            text-decoration: none;
            display: inline-block;
            text-align: center;
        }
        
        .btn-primary {
            background: #667eea;
            color: white;
        }
        
        .btn-primary:hover {
            background: #5a6fd8;
            transform: translateY(-2px);
        }
        
        .btn-success {
            background: #00b894;
            color: white;
        }
        
        .btn-success:hover {
            background: #00a085;
        }
        
        .btn-danger {
            background: #e17055;
            color: white;
        }
        
        .btn-danger:hover {
            background: #d63031;
        }
        
        .btn-youtube {
            background: #ff0000;
            color: white;
        }
        
        .btn-youtube:hover {
            background: #cc0000;
        }
        
        .results {
            text-align: center;
        }
        
        .score {
            font-size: 3em;
            font-weight: bold;
            margin: 20px 0;
        }
        
        .score.pass {
            color: #00b894;
        }
        
        .score.fail {
            color: #e17055;
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: #2d3436;
        }
        
        .form-group input {
            width: 100%;
            padding: 12px 15px;
            border: 2px solid #e9ecef;
            border-radius: 8px;
            font-size: 1em;
            transition: border-color 0.3s ease;
        }
        
        .form-group input:focus {
            outline: none;
            border-color: #667eea;
        }
        
        .hidden {
            display: none;
        }
        
        .progress-bar {
            width: 100%;
            height: 8px;
            background: #e9ecef;
            border-radius: 4px;
            overflow: hidden;
            margin-bottom: 20px;
        }
        
        .progress-fill {
            height: 100%;
            background: linear-gradient(90deg, #667eea, #764ba2);
            transition: width 0.3s ease;
        }
        
        .bonus-time {
            position: absolute;
            top: 20px;
            right: 20px;
            background: #00b894;
            color: white;
            padding: 10px 15px;
            border-radius: 20px;
            font-weight: bold;
            animation: bounceIn 0.5s ease;
        }
        
        @keyframes bounceIn {
            0% { transform: scale(0); }
            50% { transform: scale(1.2); }
            100% { transform: scale(1); }
        }
        
        .feedback {
            margin-top: 20px;
            padding: 15px;
            border-radius: 8px;
            font-weight: 600;
        }
        
        .feedback.correct {
            background: #d4edda;
            color: #155724;
            border: 1px solid #c3e6cb;
        }
        
        .feedback.incorrect {
            background: #f8d7da;
            color: #721c24;
            border: 1px solid #f5c6cb;
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Student Registration -->
        <div id="registration" class="card">
            <h1 style="text-align: center; color: #667eea; margin-bottom: 30px;">📚 TLE 10 FOOD SERVICE SUMMATIVE TEST 1</h1>
            <form id="studentForm">
                <div class="form-group">
                    <label for="studentName">Student Name:</label>
                    <input type="text" id="studentName" required>
                </div>
                <div class="form-group">
                    <label for="studentGrade">Grade:</label>
                    <input type="text" id="studentGrade" required>
                </div>
                <div class="form-group">
                    <label for="studentSection">Section:</label>
                    <input type="text" id="studentSection" required>
                </div>
                <button type="submit" class="btn btn-primary" style="width: 100%;">Start Quiz</button>
            </form>
        </div>

        <!-- Dashboard -->
        <div id="dashboard" class="card dashboard hidden">
            <h2>📊 Student Dashboard</h2>
            <div class="profile-info">
                <div class="info-item">
                    <strong>Name:</strong><br>
                    <span id="displayName"></span>
                </div>
                <div class="info-item">
                    <strong>Grade:</strong><br>
                    <span id="displayGrade"></span>
                </div>
                <div class="info-item">
                    <strong>Section:</strong><br>
                    <span id="displaySection"></span>
                </div>
            </div>
        </div>

        <!-- Quiz Interface -->
        <div id="quizInterface" class="hidden">
            <div class="timer" id="timer">⏰ 10:00</div>
            
            <div class="progress-bar">
                <div class="progress-fill" id="progressFill" style="width: 0%"></div>
            </div>
            
            <div class="card question-card">
                <div id="bonusTime" class="bonus-time hidden">+5 seconds! 🎉</div>
                
                <div class="question-header">
                    <div class="question-number" id="questionNumber">Question 1 of 20</div>
                    <div style="font-weight: 600; color: #667eea;">Score: <span id="currentScore">0</span>/20</div>
                </div>
                
                <div class="question-text" id="questionText"></div>
                
                <div class="choices" id="choices"></div>
                
                <div id="feedback" class="feedback hidden"></div>
                
                <button id="nextBtn" class="btn btn-primary hidden" style="margin-top: 20px; width: 100%;">Next Question</button>
            </div>
        </div>

        <!-- Results -->
        <div id="results" class="card results hidden">
            <h2>🎯 Quiz Results</h2>
            <div class="score" id="finalScore"></div>
            <div id="resultMessage"></div>
            <div id="resultActions" style="margin-top: 30px;"></div>
        </div>
    </div>

    <script>
        const questions = [
            {
                question: "What is table setting?",
                choices: ["The process of cooking food", "The proper arrangement of table implements for dining", "The decoration of a dining hall", "The serving of guests"],
                correct: 1
            },
            {
                question: "Why is table setting important?",
                choices: ["It makes the food taste better", "It reflects respect and hospitality to guests", "It makes guests serve themselves faster", "It shortens meal preparation time"],
                correct: 1
            },
            {
                question: "Which of the following is NOT a table implement?",
                choices: ["Linen", "Dinnerware", "Cookware", "Silverware"],
                correct: 2
            },
            {
                question: "What are linens used for in table setting?",
                choices: ["For serving food", "For covering chairs", "To add beauty and protect the table surface", "To clean dishes"],
                correct: 2
            },
            {
                question: "Which of the following is NOT considered silverware?",
                choices: ["Spoon", "Fork", "Knife", "Bowl"],
                correct: 3
            },
            {
                question: "How should flatware be arranged?",
                choices: ["From the inside out", "From the outside moving inward", "Randomly placed", "According to color"],
                correct: 1
            },
            {
                question: "What includes plates, bowls, and saucers?",
                choices: ["Silverware", "Dinnerware", "Glassware", "Holloware"],
                correct: 1
            },
            {
                question: "Where should glassware be placed on the table?",
                choices: ["On the left of the plate", "Below the plate", "On the upper right of the plate, above the knives", "Behind the napkin"],
                correct: 2
            },
            {
                question: "Which of the following is an example of holloware?",
                choices: ["Dessert plate", "Teapot", "Knife", "Glass"],
                correct: 1
            },
            {
                question: "What type of table setting is used for everyday meals?",
                choices: ["Informal", "Formal", "Casual-Formal", "Banquet"],
                correct: 0
            },
            {
                question: "Which of the following is TRUE about informal table setting?",
                choices: ["It uses multiple pieces of glassware", "It follows strict etiquette rules", "It is simple and practical", "It is only used for weddings"],
                correct: 2
            },
            {
                question: "What kind of occasion is a formal table setting used for?",
                choices: ["Family dinner", "Picnic", "Weddings or banquets", "School lunch"],
                correct: 2
            },
            {
                question: "Which of the following is a key aspect of excellent customer service?",
                choices: ["Ignoring complaints", "Greeting guests warmly and professionally", "Speaking loudly to customers", "Serving food without utensils"],
                correct: 1
            },
            {
                question: "Why is consistency important in customer service?",
                choices: ["It reduces the number of employees", "It ensures customers receive quality service every time", "It increases the price of meals", "It prevents employees from taking breaks"],
                correct: 1
            },
            {
                question: "What is the first impression a food service attendant should give?",
                choices: ["Strict and serious", "Warm and professional greeting", "Silent and distant attitude", "Quick and careless service"],
                correct: 1
            },
            {
                question: "What should a food service worker do when a complaint arises?",
                choices: ["Ignore it", "Argue with the customer", "Address it promptly and effectively", "Call the manager immediately every time"],
                correct: 2
            },
            {
                question: "Which law must food service attendants comply with to ensure safety?",
                choices: ["Food and Drug Act", "Occupational Safety and Health (OSH) Standards", "Environmental Act", "Labor Code"],
                correct: 1
            },
            {
                question: "What is the first rule in personal hygiene?",
                choices: ["Avoid washing hands", "Wear clean uniforms and wash hands frequently", "Eat during service", "Skip using gloves"],
                correct: 1
            },
            {
                question: "To avoid cross-contamination, food handlers should:",
                choices: ["Mix raw and cooked food", "Store raw and cooked food separately", "Use the same utensils for all food", "Ignore food temperatures"],
                correct: 1
            },
            {
                question: "What should be done to ensure workplace safety?",
                choices: ["Keep floors wet", "Report defective equipment immediately", "Leave clutter on the floor", "Ignore safety drills"],
                correct: 1
            }
        ];

        let currentQuestionIndex = 0;
        let score = 0;
        let timeLeft = 600; // 10 minutes in seconds
        let timer;
        let shuffledQuestions = [];
        let studentInfo = {};
        let answered = false;

        function shuffleArray(array) {
            const shuffled = [...array];
            for (let i = shuffled.length - 1; i > 0; i--) {
                const j = Math.floor(Math.random() * (i + 1));
                [shuffled[i], shuffled[j]] = [shuffled[j], shuffled[i]];
            }
            return shuffled;
        }

        function shuffleChoices(question) {
            const correctAnswer = question.choices[question.correct];
            const shuffledChoices = shuffleArray(question.choices);
            const newCorrectIndex = shuffledChoices.indexOf(correctAnswer);
            
            return {
                ...question,
                choices: shuffledChoices,
                correct: newCorrectIndex
            };
        }

        function initializeQuiz() {
            shuffledQuestions = shuffleArray(questions).map(shuffleChoices);
            currentQuestionIndex = 0;
            score = 0;
            timeLeft = 600;
            answered = false;
            
            document.getElementById('currentScore').textContent = score;
            updateProgress();
            displayQuestion();
            startTimer();
        }

        function startTimer() {
            timer = setInterval(() => {
                timeLeft--;
                updateTimerDisplay();
                
                if (timeLeft <= 0) {
                    clearInterval(timer);
                    endQuiz();
                }
            }, 1000);
        }

        function updateTimerDisplay() {
            const minutes = Math.floor(timeLeft / 60);
            const seconds = timeLeft % 60;
            document.getElementById('timer').textContent = `⏰ ${minutes}:${seconds.toString().padStart(2, '0')}`;
        }

        function updateProgress() {
            const progress = (currentQuestionIndex / shuffledQuestions.length) * 100;
            document.getElementById('progressFill').style.width = `${progress}%`;
        }

        function displayQuestion() {
            if (currentQuestionIndex >= shuffledQuestions.length) {
                endQuiz();
                return;
            }

            const question = shuffledQuestions[currentQuestionIndex];
            answered = false;
            
            document.getElementById('questionNumber').textContent = `Question ${currentQuestionIndex + 1} of ${shuffledQuestions.length}`;
            document.getElementById('questionText').textContent = question.question;
            
            const choicesContainer = document.getElementById('choices');
            choicesContainer.innerHTML = '';
            
            question.choices.forEach((choice, index) => {
                const choiceElement = document.createElement('div');
                choiceElement.className = 'choice';
                choiceElement.textContent = choice;
                choiceElement.onclick = () => selectAnswer(index);
                choicesContainer.appendChild(choiceElement);
            });
            
            document.getElementById('feedback').classList.add('hidden');
            document.getElementById('nextBtn').classList.add('hidden');
            document.getElementById('bonusTime').classList.add('hidden');
        }

        function selectAnswer(selectedIndex) {
            if (answered) return;
            
            answered = true;
            const question = shuffledQuestions[currentQuestionIndex];
            const choices = document.querySelectorAll('.choice');
            const feedbackElement = document.getElementById('feedback');
            
            choices[selectedIndex].classList.add('selected');
            
            if (selectedIndex === question.correct) {
                choices[selectedIndex].classList.add('correct');
                score++;
                timeLeft += 5; // Add 5 seconds bonus
                
                // Show bonus time animation
                const bonusElement = document.getElementById('bonusTime');
                bonusElement.classList.remove('hidden');
                setTimeout(() => {
                    bonusElement.classList.add('hidden');
                }, 2000);
                
                feedbackElement.textContent = '✅ Correct! Great job!';
                feedbackElement.className = 'feedback correct';
                
                document.getElementById('currentScore').textContent = score;
            } else {
                choices[selectedIndex].classList.add('incorrect');
                
                feedbackElement.textContent = `❌ Incorrect. Try again next time!`;
                feedbackElement.className = 'feedback incorrect';
            }
            
            feedbackElement.classList.remove('hidden');
            
            // Disable all choices
            choices.forEach(choice => {
                choice.style.pointerEvents = 'none';
            });
            
            setTimeout(() => {
                document.getElementById('nextBtn').classList.remove('hidden');
            }, 1500);
        }

        function nextQuestion() {
            currentQuestionIndex++;
            updateProgress();
            displayQuestion();
        }

        function endQuiz() {
            clearInterval(timer);
            
            document.getElementById('quizInterface').classList.add('hidden');
            document.getElementById('results').classList.remove('hidden');
            
            const percentage = (score / shuffledQuestions.length) * 100;
            const passed = percentage >= 80;
            
            const scoreElement = document.getElementById('finalScore');
            scoreElement.textContent = `${score}/${shuffledQuestions.length} (${percentage.toFixed(1)}%)`;
            scoreElement.className = `score ${passed ? 'pass' : 'fail'}`;
            
            const messageElement = document.getElementById('resultMessage');
            const actionsElement = document.getElementById('resultActions');
            
            if (passed) {
                messageElement.innerHTML = `
                    <h3 style="color: #00b894;">🎉 Congratulations! You Passed!</h3>
                    <p>Excellent work! You've demonstrated a solid understanding of table setting and customer service.</p>
                `;
                
                actionsElement.innerHTML = `
                    <button class="btn btn-success" onclick="sendResultsToTeacher()" style="margin-right: 15px;">
                        📧 Send Results to Teacher
                    </button>
                    <button class="btn btn-primary" onclick="retakeQuiz()">
                        🔄 Retake Quiz
                    </button>
                `;
            } else {
                messageElement.innerHTML = `
                    <h3 style="color: #e17055;">📚 Keep Learning!</h3>
                    <p>You need 80% to pass. Don't give up - practice makes perfect!</p>
                `;
                
                actionsElement.innerHTML = `
                    <a href="https://www.youtube.com/@princeyahwetv" target="_blank" rel="noopener noreferrer" class="btn btn-youtube" style="margin-right: 15px;">
                        📺 Subscribe for Study Help
                    </a>
                    <button class="btn btn-primary" onclick="retakeQuiz()">
                        🔄 Retake Quiz
                    </button>
                `;
            }
        }

        function sendResultsToTeacher() {
            const subject = encodeURIComponent(`Quiz Results - ${studentInfo.name}`);
            const body = encodeURIComponent(`
Dear Teacher,

Student Information:
- Name: ${studentInfo.name}
- Grade: ${studentInfo.grade}
- Section: ${studentInfo.section}

Quiz Results:
- Score: ${score}/${shuffledQuestions.length}
- Percentage: ${((score / shuffledQuestions.length) * 100).toFixed(1)}%
- Status: PASSED ✅

The student has successfully completed the Table Setting and Customer Service Quiz with a passing grade.

Best regards,
Quiz System
            `);
            
            window.open(`mailto:joel.rodriguez@deped.gov.ph?subject=${subject}&body=${body}`, '_blank');
        }

        function retakeQuiz() {
            document.getElementById('results').classList.add('hidden');
            document.getElementById('dashboard').classList.remove('hidden');
            document.getElementById('quizInterface').classList.remove('hidden');
            
            initializeQuiz();
        }

        // Event Listeners
        document.getElementById('studentForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            studentInfo = {
                name: document.getElementById('studentName').value,
                grade: document.getElementById('studentGrade').value,
                section: document.getElementById('studentSection').value
            };
            
            document.getElementById('displayName').textContent = studentInfo.name;
            document.getElementById('displayGrade').textContent = studentInfo.grade;
            document.getElementById('displaySection').textContent = studentInfo.section;
            
            document.getElementById('registration').classList.add('hidden');
            document.getElementById('dashboard').classList.remove('hidden');
            document.getElementById('quizInterface').classList.remove('hidden');
            
            initializeQuiz();
        });

        document.getElementById('nextBtn').addEventListener('click', nextQuestion);
    </script>
<script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'990e07455165ddc1',t:'MTc2MDg1MzM0Ni4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
