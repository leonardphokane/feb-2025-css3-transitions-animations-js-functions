# feb-2025-css3-transitions-animations-js-functions

<!DOCTYPE html>
<html lang="en">
<head>
  <link rel="stylesheet" href="styles.css">
  <script defer src="script.js"></script>
</head>
<body>
  <header class="banner">Welcome to Travel Paradise!</header>
  <button id="openModal" class="btn">Learn More</button>
  <div id="modal" class="modal hidden">
    <div class="modal-content">
      <span id="closeModal" class="close">&times;</span>
      <p>Plan your dream vacation with us!</p>
    </div>
  </div>
</body>
</html>


CSS

/* Banner Animation */
.banner {
  background: #4caf50;
  color: white;
  padding: 20px;
  animation: slideIn 2s ease-in-out forwards;
}

@keyframes slideIn {
  0% { transform: translateX(-100%); }
  100% { transform: translateX(0); }
}

/* Button Transition */
.btn {
  padding: 10px 20px;
  font-size: 16px;
  background-color: #008cba;
  color: white;
  border: none;
  cursor: pointer;
  transition: transform 0.3s ease;
}

.btn:hover {
  transform: scale(1.1);
}

/* Modal Styling and Animation */
.modal {
  display: flex;
  justify-content: center;
  align-items: center;
  position: fixed;
  top: 0; left: 0;
  width: 100%; height: 100%;
  background: rgba(0, 0, 0, 0.5);
  animation: fadeIn 0.5s ease forwards;
}

.hidden { display: none; }

.modal-content {
  background: white;
  padding: 20px;
  border-radius: 5px;
  text-align: center;
}

@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}


JavaScript

// Toggle Modal Visibility
const openModalButton = document.getElementById("openModal");
const closeModalButton = document.getElementById("closeModal");
const modal = document.getElementById("modal");

openModalButton.addEventListener("click", () => {
  modal.classList.remove("hidden");
});

closeModalButton.addEventListener("click", () => {
  modal.classList.add("hidden");
});

// Example of a Function with Parameters and Return Value
function calculateVacationCost(days, costPerDay) {
  return days * costPerDay;
}

console.log(`Total cost: $${calculateVacationCost(7, 150)}`);
