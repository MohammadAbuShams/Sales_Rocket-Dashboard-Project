# Sales_Rocket Dashboard Project 

## 🔎 Overview
This project delivers a **proof-of-concept (POC) dashboard** for the Sales_Rocket startup to answer six management questions using the **Sample Superstore** dataset.  
The focus is on **clarity** (grayscale, minimal ink), **interactivity** (filter actions), and **traceability** (sketches + wireframe → final dashboard).

---

## 📦 Deliverables (Links)
- **Dashboard (Tableau Public):**  
  https://public.tableau.com/app/profile/mohammad.abushams/viz/Bookk1_17576026440190/Sales_RocketDashboard?publish=yes

---

## 🗂 Dataset
**Name:** Sample Superstore  
**Columns used (subset):** `Order Date, Ship Date, State, City, Category, Sub-Category, Product Name, Quantity, Sales, Profit, Segment, Region`  
**Notes:** Ensure numeric types for `Sales`, `Profit`, `Discount`; and date types for `Order Date`, `Ship Date`.

---

## ❓ Management Questions (Q1–Q6) & Visuals
1. **Most profitable city in Tennessee** → *Bar chart* (City vs **SUM(Profit)**, filter **State = Tennessee**, sorted desc).  
2. **Average annual profit for that city** → *KPI card* (**AVG** of yearly **SUM(Profit)** for the city from Q1).  
3. **Most profitable category in Iowa (on average)** → *Bar chart* (Category vs **AVG(Yearly Profit)**, filter **State = Iowa**).  
4. **Most popular product in that category (2016)** → *Bar chart* (Product Name vs **SUM(Quantity)**, filters **Year = 2016**, **Category = Q3 result**).  
5. **Most profitable month in 2018 (overall)** → *Line chart* (Month(2018) vs **SUM(Profit)**, label the peak month).  
6. **How widely monthly profits varied in 2018** → *Line chart + reference lines* (**Min/Max/Avg**; mention **Range = Max − Min**).

> Color policy: **Grayscale** only (“get it right in black & white”).

---

## 🧭 Dashboard Layout (Wireframe → Final)
- **Row 1:** Q1 (Bar: City Profit TN) | Q2 (KPI: Avg Annual Profit for city)  
- **Row 2:** Q3 (Bar: Category in Iowa) | Q4 (Bar: Popular Product 2016)  
- **Row 3:** Q5 (Line: Top Month 2018) | Q6 (Line + Ref Lines: Variation 2018)  

### Interactions (Actions)
- **Click city in Q1 → filter Q2** to that city.  
- **Click category in Q3 → filter Q4** to that category.

---

## 🛠 Reproduce in Tableau (Quick Steps)
1. **Connect data:** open `superstore-dataset-dashboarddesign.csv` in Tableau.  
2. **Data types:** set `Profit/Sales/Discount = Number (Decimal)`, `Order Date/Ship Date = Date`.  
3. **Build sheets:**
   - `Q1 - TN City Profit`: State filter = Tennessee; **City** on Columns; **SUM(Profit)** on Rows; sort desc; add labels.
   - `Q2 - Avg Annual Profit`: filter **City = Q1 winner**; **AVG(Profit)** as KPI; optional: compute average of yearly **SUM(Profit)**.
   - `Q3 - Iowa Category`: State = Iowa; Category vs **AVG(Profit)** (or **SUM**) and sort desc.
   - `Q4 - Popular Product 2016`: Year(2016); Category = Q3; Product vs **SUM(Quantity)**; sort desc; optional horizontal bars for long names.
   - `Q5 - 2018 Top Month`: Year(2018); Month vs **SUM(Profit)**; label max; optional reference line (Maximum).
   - `Q6 - 2018 Variation`: Year(2018); Month vs **SUM(Profit)**; add reference lines (**Min/Max/Avg**) and note **Range**.
4. **Dashboard:** new dashboard → size **Automatic** → place sheets per wireframe → set **grayscale** via Marks → Color.
5. **Actions:** `Dashboard → Actions → Add Action → Filter` (Q1→Q2, Q3→Q4).
6. **Publish:** `File → Save to Tableau Public` → copy the public URL.

---

## 📝 Sketches & Wireframe (What’s included)
- **Sketches:** For each Q1–Q6, 2–3 alternative chart options (e.g., Q1: vertical bar, horizontal bar, pie; Q5: line, area, columns).  
- **Wireframe:** One page layout (2×3 grid) with **Q1–Q6** boxes labeled by their final chart type.

> These images are embedded in the project template PDF per rubric: “Dashboard Link + Sketches + Wireframe in a single PDF”.

---

## ✅ Rubric Mapping
- **Dashboard:** Interactive exploration enabled (filters & actions) and answers are visually obvious.  
- **Sketches:** Multiple alternatives per question demonstrate exploration.  
- **Wireframe:** Shows overall structure before building; not a screenshot of the final dashboard.  
- **Color constraint:** Grayscale throughout (black/white shades).

---


