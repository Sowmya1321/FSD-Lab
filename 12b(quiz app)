import React, { useState } from "react"; 
 
function App() { 
  const questions = [ 
    { 
      question: "What is the capital of France?", 
      options: ["Paris", "London", "Rome", "Berlin"], 
      answer: "Paris", 
    }, 
    { 
      question: "Which planet is known as the Red Planet?", 
      options: ["Earth", "Mars", "Jupiter", "Venus"], 
      answer: "Mars", 
    }, 
    { 
      question: "Which language is used for web apps?", 
      options: ["Python", "JavaScript", "C++", "Java"], 
      answer: "JavaScript", 
    }, 
  ]; 
  const [current, setCurrent] = useState(0); 
  const [score, setScore] = useState(0); 
  const [showScore, setShowScore] = useState(false); 
 
  const handleAnswer = (option) => { 
    if (option === questions[current].answer) { 
      setScore(score + 1); 
    } 
    const next = current + 1; 
    if (next < questions.length) { 
      setCurrent(next); 
    } else { 
      setShowScore(true); 
    } 
  }; 
 
  const resetQuiz = () => { 
    setCurrent(0); 
    setScore(0); 
    setShowScore(false); 
  }; 
  return ( 
    <div style={{ textAlign: "center", padding: 30, fontFamily: "system-ui" }}> 
      <h2>  Simple React Quiz App</h2> 
 
      {showScore ? ( 
        <div> 
          <h3> 
            You scored {score} out of {questions.length} 
          </h3> 
          <button 
            onClick={resetQuiz} 
            style={{ 
              padding: "8px 15px", 
              marginTop: "10px", 
              background: "#4CAF50", 
              color: "white", 
              border: "none", 
              borderRadius: "5px", 
              cursor: "pointer", 
            }} 
          > 
            Restart Quiz 
          </button> 
        </div>) :  
       ( 
        <div> 
          <h3> 
            Question {current + 1}/{questions.length} 
          </h3> 
          <p>{questions[current].question}</p> 
          <div style={{ display: "flex", flexDirection: "column", alignItems: "center" }}> 
            {questions[current].options.map((option, index) => ( 
              <button 
                key={index} 
                onClick={() => handleAnswer(option)} 
                style={{ 
                  margin: "5px", 
                  padding: "8px 15px", 
                  width: "200px", 
                  borderRadius: "5px", 
                  border: "1px solid #ccc", 
                  background: "#f5f5f5", 
                  cursor: "pointer", 
                }} > 
                {option} 
              </button> 
            ))} 
          </div> 
        </div> 
      )} 
    </div> 
  ); 
} 
 
export default App;
