 ##🌿 Recursive Splitting — A Grasshopper Toolkit for Plot Division in Urban Design

This Grasshopper component automates **plot subdivision** using a recursive splitting algorithm, making it ideal for **urban design and planning**. It identifies the longest edge of a given quadrilateral site boundary and recursively splits the land until all plots are smaller than a user-defined size threshold. The logic incorporates **road spacing between plots**, enabling real-world urban block patterns.

![visual_exmaple](https://github.com/user-attachments/assets/b100118f-08eb-42b5-97be-b261a1cff619)

---

## 🧠 Principle

The splitting process follows a geometric and recursive approach:

1. **Longest Edge Detection**: For a given quadrilateral `site boundary`, the longest edge is identified.  
2. **Subdivision Line Generation**: A line is drawn from the midpoint of the longest edge to the midpoint of the opposite edge.  
3. **Road Spacing Adjustment**: The subdivision line is offset on both sides by a user-defined width (`S_plot`) to reserve space for internal streets.  
4. **Recursive Loop**: The process is repeated recursively for each subdivided plot **until** all resulting plots are smaller than the input `thresh` value (in square meters).  

> ⚠️ Input boundaries must be **4-sided polygons (quadrilaterals)**.

---

## 🛠️ Component Setup

Component group name: **`Recursive Splitting.gh`**  
Replace the placeholder inputs with your own data:

| Parameter       | Description                                                                 |
|-----------------|-----------------------------------------------------------------------------|
| `site boundary` | Closed 4-sided curves representing the land plots to split.                 |
| `thresh`        | Minimum plot area (m²) to stop the recursive split (e.g., 20000 or 40000).  |
| `S_plot`        | Width reserved for roads between plots (e.g., 8, 10, or 12 meters).         |



---

## 📸 Visual Examples

### 🏙️ Urban Design Case Example
<img width="1272" height="717" alt="example_city_design" src="https://github.com/user-attachments/assets/4fbeb96c-00ec-4578-8e42-e49ed1451cca" />

### 📐 Recursive Splitting Process (Threshold: 20,000 m²)

#### ⏱ Step-by-step Preview
![splitting_step_20000](https://github.com/user-attachments/assets/a6586e9d-be8e-4738-9189-051f65f37fd6)

#### 🔁 Automatic Recursion (20,000 m²)
![auto_split_20000](https://github.com/user-attachments/assets/ea636dad-21b0-4051-9859-07e80a98c68c)

#### 🔁 Automatic Recursion (40,000 m²)
![auto_split_40000](https://github.com/user-attachments/assets/15893f55-62eb-41db-b854-8eaf8eb2ba73)


---

## 🧩 Applications

- Urban block generation  
- Masterplan parcel subdivision  
- Adaptive block typologies with plot-size constraints  
- Road network embedding through geometry logic  

---

## 📎 Requirements

- Rhino + Grasshopper  
- Plugin: **Hoop snake**  

---

## 💡 Customization Tips

- You can modify the split direction logic (e.g., diagonal splits) by editing the midpoint-line generation logic in the Grasshopper definition.  
- For non-quadrilateral boundaries, additional logic must be implemented.  

---

## 📥 Getting Started

1. Load `Recursive Splitting.gh` in Grasshopper.  
2. Replace inputs with your own `site boundary`, `thresh`, and `S_plot` values.  
3. Run the definition to visualize and export resulting plots.  

---

## 📩 Contact

For suggestions or collaboration on urban geometry logic, feel free to reach out via **Issues** or **Pull Requests**.  

