# NutriGuide 🍽️  
### AI-Powered Personalized Recipe Recommendation System for Indian Cuisine  

NutriGuide is an AI-driven system designed to provide personalized, health-conscious meal recommendations based on available ingredients, dietary preferences, and caloric requirements. Built specifically with the diversity of Indian cuisine in mind, NutriGuide bridges the gap between nutritional goals and cultural eating habits using intelligent recommendation logic.  

---

## 🌟 Key Features

- **Ingredient-based search**: Input your available ingredients and receive recipe suggestions that best match them.
- **Calorie-aware recommendations**: Tailor suggestions to fit within your nutritional goals.
- **Diet filters**: Choose from options like Vegan, Diabetic-Friendly, Gluten-Free, High-Protein, and more.
- **Indian recipe focus**: Datasets and logic curated specifically for Indian meals and cooking styles.
- **Interactive frontend**: Experience a seamless and user-friendly interface built with Gradio for real-time results. (Gradio based UI that has been commented out!)

---

## 🧠 Tech Stack

| Component               | Description                                                                 |
|------------------------|-----------------------------------------------------------------------------|
| **Python**             | Core programming language                                                   |
| **spaCy**              | Used for ingredient extraction and natural language preprocessing           |
| **NLTK**               | Employed for stopword removal and text normalization                        |
| **scikit-learn (TF-IDF)** | Vectorization of ingredient data and similarity computation               |
| **Cosine Similarity**  | Determines relevance between user inputs and recipes                        |
| **Gradio**             | Web-based user interface for input and result presentation                  |
| **Pandas & NumPy**     | Data manipulation and numerical computation                                 |

---

## 🧪 How It Works

NutriGuide leverages content-based filtering using TF-IDF vectorization and cosine similarity to match the user’s input with relevant recipes from a structured dataset. The pipeline consists of:

1. **Data Preprocessing**  
   - Removal of null values  
   - Tokenization and keyword extraction using spaCy  
   - Cleaning using regular expressions and stopword filtering  

2. **Feature Engineering**  
   - Transforms ingredient lists into TF-IDF vectors  
   - Prepares user input with the same pipeline for consistency  

3. **Similarity Scoring**  
   - Cosine similarity is calculated between the input and recipe vectors  
   - Calorie alignment is factored in through a hybrid scoring mechanism:  
     - 80% weight to ingredient similarity  
     - 20% weight to calorie proximity  

4. **Recommendation Generation**  
   - Top matches are ranked and filtered based on optional dietary preference  
   - Final results displayed with name, diet type, instructions, and estimated calories  

---

## 📈 Results

NutriGuide has shown consistent accuracy in identifying and ranking recipes that match the input constraints. Sample runs demonstrate that it can return recipes that are relevant both contextually and nutritionally, while respecting cultural nuances such as Indian food preparation practices.  

---


## 🚀 Getting Started

To run the project:

- Clone the repository to your local device using:
  ```bash
  git clone https://github.com/your-username/NutriGuide.git
  cd NutriGuide
  ```
  
- Open the `jupyternotebook.ipynb` notebook directly in **Google Colab** or run it locally in a Jupyter environment. `pythonfile.py` has been added as a reference and can also be run on a local machine.

- Ensure the following Python libraries are installed:  
  `spaCy`, `scikit-learn`, `nltk`, `pandas`, `gradio`

- Use the provided CSV dataset for training the model. The dataset should contain columns such as:  
  - `TranslatedIngredients`  
  - `EstimatedCalories`  
  - `Diet`  
  - `TranslatedInstructions`  
  - `TranslatedRecipeName`

- Run the notebook cells sequentially to:
  - Preprocess the dataset
  - Vectorize the ingredients
  - Input your recipe search criteria
  - Generate and view the personalized recipe recommendations

---
Author: Anushka Srivastava
