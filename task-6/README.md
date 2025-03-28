# **Tabbed Video Game Characters**  

## **📌 Overview**  
This project implements a **tabbed interface** to display different video game characters using **HTML** and **CSS only** (without JavaScript). The user can switch between different tabs to view information about characters.  

## **🖼️ Output Preview**  
![Output Screenshot](output.png)  

## **📂 Files Included**  
- `index.html` → Contains the tab structure and character content.  
- `style.css` → Styles the tabs, cards, and hover effects.  
- `output.png` → Screenshot of the final output.  

## **⚡ How It Works**  
1. **Radio Buttons as Tabs**  
   ```html
   <input type="radio" id="tab1" name="tab-group" checked>
   <input type="radio" id="tab2" name="tab-group">
   <input type="radio" id="tab3" name="tab-group">
   ```
   - Each tab is controlled by a **hidden radio button**.  
   - The `checked` attribute sets the **default active tab**.  

2. **Tab Labels for Navigation**  
   ```html
   <div class="tab-labels">
       <label for="tab1">Jin Sakai</label>
       <label for="tab2">Joel Miller</label>
       <label for="tab3">Spiderman</label>
   </div>
   ```
   - Labels act as clickable tabs, linked to the radio buttons.  

3. **Content Sections (Initially Hidden)**  
   ```html
   <div class="content" id="content1"> <!-- Jin Sakai's card here --> </div>
   <div class="content" id="content2"> <!-- Joel Miller's card here --> </div>
   <div class="content" id="content3"> <!-- Spiderman's card here --> </div>
   ```
   - Each character's details are inside `div.content`, **hidden by default**.  

4. **CSS to Control Visibility**  
   ```css
   #tab1:checked ~ .tab-content #content1,
   #tab2:checked ~ .tab-content #content2,
   #tab3:checked ~ .tab-content #content3 {
       display: block;
   }
   ```
   - When a tab is **checked**, the corresponding content **appears**.  

5. **Highlight Active Tab**  
   ```css
   #tab1:checked ~ .tab-labels label[for="tab1"],
   #tab2:checked ~ .tab-labels label[for="tab2"],
   #tab3:checked ~ .tab-labels label[for="tab3"] {
       background: #007BFF;
       color: white;
       font-weight: bold;
   }
   ```
   - The active tab is **styled differently**.  

