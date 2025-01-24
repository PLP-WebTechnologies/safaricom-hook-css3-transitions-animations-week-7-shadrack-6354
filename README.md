### **Assignment: Building an Interactive and Dynamic Web Page**  

#### **Objective**  
Create a visually engaging and interactive webpage that utilizes **CSS3 transitions and animations**, **advanced JavaScript functions** (including scope, parameters, and return values), and combines **CSS animations with JavaScript** to create dynamic user interactions.  

---

### **Part 1: CSS3 Transitions and Animations**  
1. **Task**:  
   - Use **CSS transitions** to create smooth effects on hover or focus (e.g., buttons that change color or grow).  
   - Use **CSS animations** with `@keyframes` to create dynamic effects like fading, sliding, or rotating.  

2. **Requirements**:  
   - At least **two elements** must include hover or focus transitions.  
   - At least **two animations** must be created using `@keyframes` (e.g., an animated banner or an animated loading spinner).
  
   - /* Fading Box Animation */
.fade-box {
  width: 200px;
  height: 200px;
  background-color: #f39c12;
  animation: fadeAnimation 2s infinite alternate;
}

@keyframes fadeAnimation {
  0% {
    opacity: 0.2;
  }
  100% {
    opacity: 1;
  }
}

/* Spinner Animation */
.spinner {
  width: 40px;
  height: 40px;
  border: 5px solid #f39c12;
  border-top: 5px solid #3498db;
  border-radius: 50%;
  animation: spin 1s linear infinite;
}

@keyframes spin {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
 

---

### **Part 2: JavaScript Functions**  
1. **Task**:  
   - Write JavaScript functions to handle interactivity on the webpage.  
   - Utilize **parameters**, **return values**, and demonstrate an understanding of **scope**.  

2. **Requirements**:  
   - Write at least **three functions**:  
     - A function with parameters and return values (e.g., calculate a value like the area of a rectangle based on user input).  
     - A function that demonstrates the concept of scope (local vs. global variables).  
     - A function to toggle a CSS class that applies an animation (e.g., toggling a "hidden" class for a modal).
    
     - function toggleModal() {
  const modal = document.getElementById('modal');
  modal.classList.toggle('show'); // Toggle the 'show' class to display the modal
}


---

### **Part 3: Combining CSS Animations with JavaScript**  
1. **Task**:  
   - Use JavaScript to trigger or control CSS animations dynamically.  

2. **Requirements**:  
   - Create an interactive element (e.g., a button, card, or slider) that triggers an animation when clicked.  
   - Dynamically add or remove CSS classes to control the animation.  
   - Ensure that the animation resets properly when triggered multiple times.
  
   - <button onclick="triggerAnimation()" class="rotate-button">Click Me!</button>
.rotate-button {
  padding: 10px 20px;
  background-color: #e74c3c;
  color: white;
  border: none;
  cursor: pointer;
  transition: transform 0.5s ease; /* Smooth transform transition */
}

.rotate-button.animate {
  transform: rotate(360deg); /* Rotate the button */
}
function triggerAnimation() {
  const button = document.querySelector('.rotate-button');
  button.classList.add('animate'); // Trigger the animation
  
  // Reset the animation after it completes
  setTimeout(() => {
    button.classList.remove('animate');
  }, 500); // Duration of the animation (0.5s)
}


---
