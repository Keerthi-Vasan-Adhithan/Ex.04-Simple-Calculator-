# Ex04 Simple Calculator - React Project
## Date:

## AIM
To  develop a Simple Calculator using React.js with clean and responsive design, ensuring a smooth user experience across different screen sizes.

## ALGORITHM
### STEP 1
Create a React App.

### STEP 2
Open a terminal and run:
  <ul><li>npx create-react-app simple-calculator</li>
  <li>cd simple-calculator</li>
  <li>npm start</li></ul>

### STEP 3
Inside the src/ folder, create a new file Calculator.js and define the basic structure.

### STEP 4
Plan the UI: Display screen, number buttons (0-9), operators (+, -, *, /), clear (C), and equal (=).

### STEP 5
Create a new file Calculator.css in src/ and add the styling.

### STEP 6
Open src/App.js and modify it.

### STEP 7
Start the development server.
  npm start

### STEP 8
Open http://localhost:3000/ in the browser.

### STEP 9
Test the calculator by entering numbers and operations.

### STEP 10
Fix styling issues and refine content placement.

### STEP 11
Deploy the website.

### STEP 12
Upload to GitHub Pages for free hosting.

## PROGRAM
### Calculator.jsx:
```jsx
import React, { useState } from 'react';
import './Calculator.css';

function Calculator() {
  const [input, setInput] = useState('');

  const handleClick = (value) => {
    if (value === '=') {
      try {
        setInput(eval(input).toString());
      } catch {
        setInput('Error');
      }
    } else if (value === 'C') {
      setInput('');
    } else {
      setInput(input + value);
    }
  };

  const buttons = [
    '7', '8', '9', '/',
    '4', '5', '6', '*',
    '1', '2', '3', '-',
    '0', 'C', '=', '+'
  ];

  return (
    <div className="calculator">
      <input className="display" type="text" value={input} disabled />
      <div className="buttons">
        {buttons.map((btn, i) => (
          <button key={i} onClick={() => handleClick(btn)}>
            {btn}
          </button>
        ))}
      </div>
      <h3 style={{"color":'white'}}>Keerthi Vasan A</h3>
      <h3 style={{"color":'white'}}>212222240048</h3>
    </div>
  );
}


export default Calculator;

```

### Calculator.css:

```css
.calculator {
    max-width: 300px;
    margin: 50px auto;
    padding: 20px;
    background: #222;
    border-radius: 10px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
  }
  
  .display {
    width: 100%;
    height: 60px;
    font-size: 24px;
    text-align: right;
    padding: 10px;
    border: none;
    border-radius: 5px;
    margin-bottom: 15px;
    background: #eee;
  }
  
  .buttons {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
  }
  
  button {
    flex: 1 0 22%;
    padding: 20px;
    font-size: 20px;
    border: none;
    border-radius: 5px;
    background: #444;
    color: white;
    cursor: pointer;
    transition: 0.3s;
  }
  
  button:hover {
    background: #666;
  }
  
  @media (max-width: 400px) {
    .calculator {
      width: 90%;
    }
  }
  

```
## OUTPUT

![Screenshot 2025-04-28 204656](https://github.com/user-attachments/assets/f6fe1187-7d82-48bb-9449-d45ad1a729d3)

## RESULT
The program for developing a simple calculator in React.js is executed successfully.
