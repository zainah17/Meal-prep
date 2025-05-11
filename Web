<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Weekly Meal Picker 🍽️</title>
  <style>
    body {
      font-family: "Segoe UI", sans-serif;
      background: linear-gradient(to right, #f9e5e5, #e5f1ff);
      margin: 0;
      padding: 20px;
      color: #333;
    }

    h1 {
      text-align: center;
      font-size: 2em;
      margin-bottom: 30px;
    }

    .day-container {
      background-color: #fff;
      border-radius: 12px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
      padding: 20px;
      margin-bottom: 20px;
    }

    label {
      font-size: 1.1em;
      display: block;
      margin-bottom: 10px;
      color: #444;
    }

    select {
      width: 100%;
      padding: 10px;
      font-size: 1em;
      border-radius: 8px;
      border: 1px solid #ccc;
    }

    .footer {
      text-align: center;
      margin-top: 30px;
      font-size: 0.9em;
      color: #666;
    }

    @media (max-width: 600px) {
      body {
        padding: 10px;
      }

      h1 {
        font-size: 1.6em;
      }
    }
  </style>
</head>
<body>

  <h1>🍱 My Weekly Lunch Planner</h1>
  <div id="planner"></div>
  <div class="footer">Your choices are saved automatically 💾</div>

  <script>
    const days = ["Sunday", "Monday", "Tuesday", "Wednesday", "Thursday"];
    const meals = [
      "Chicken Biryani", "Beef Burger", "Sushi Platter", "Shawarma", "Margherita Pizza",
      "Spaghetti Bolognese", "Pad Thai", "Caesar Salad", "Mansaf", "Tandoori Chicken",
      "Koshari", "Grilled Salmon", "Tacos", "Pho", "Fried Rice",
      "Lentil Soup", "Moussaka", "Paneer Tikka", "Ramen", "Fish & Chips",
      "Fatteh", "Quesadilla", "Falafel Wrap", "BBQ Chicken", "Steak & Fries",
      "Korean Bibimbap", "Gyoza", "Chicken Alfredo", "Molokhia", "Mac & Cheese",
      "Gnocchi", "Chili con Carne", "Stuffed Grape Leaves", "Okra Stew", "Butter Chicken"
      // Add more meals up to 100 if you like!
    ];

    function createPlanner() {
      const plannerDiv = document.getElementById("planner");

      days.forEach(day => {
        const container = document.createElement("div");
        container.className = "day-container";

        const label = document.createElement("label");
        label.setAttribute("for", day);
        label.textContent = `${day}'s Lunch 🍽️`;

        const select = document.createElement("select");
        select.id = day;
        select.innerHTML = `<option value="">-- Choose a meal --</option>` +
          meals.map(meal => `<option value="${meal}">${meal}</option>`).join('');

        // Load saved selection if exists
        const savedMeal = localStorage.getItem(`meal-${day}`);
        if (savedMeal) select.value = savedMeal;

        // Save selection on change
        select.addEventListener("change", () => {
          localStorage.setItem(`meal-${day}`, select.value);
        });

        container.appendChild(label);
        container.appendChild(select);
        plannerDiv.appendChild(container);
      });
    }

    createPlanner();
  </script>
</body>
</html>
